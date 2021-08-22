---
layout: post
title: "When in doubt, make a CLI"
tags: ruby gem

---

## what

I just made a [gem](https://rubygems.org/profiles/tuang3142) to convert between crypto and fiat currencies.

```
❯ bit
Commands:
  bit convert AMOUNT FROM TO  # Converts between fiat and cypto currencies
  bit help [COMMAND]          # Describe available commands or one specific command
  bit ping                    # pong!
  bit rate FROM TO            # Get exchange rate between fiat and crypto currencies


❯ bit convert 1 btc usd
48,915.81

❯ bit convert 3142 btc doge
470,805,076.12

❯ bit rate BTC JPY
5,377,686.09
```

## why

> The perk of being an engineer is that when some problem arises to pain your butt cheek, you just built a tool to solve it.  
> *me, 2021*

I have been working at (probably) [the largest crypto trading platform](https://remitano.com) in my country, so, naturally, I care about the market. However, it's a real hassle to google every once in a while. Typing too much can ironically end my career. Also, the web is slowed down by ads and it makes my potato of a mac burn hotly. A CLI should be a convenient solution since (a) I basically live in my iterm2 10 hours every day, (b) it's fast, and (c) it's a worthwhile engineer challenge for me.


## how

The calculation part turns out to be pretty easy. Coinbase provides an endpoint so convenient. I just need to get the rate of a currency in USD only.

```ruby
def convert(from_currency, to_currenty)
  usd_rate(to_currenty) / usd_rate(from_currency)
end
```

The fun part is to create a cli out of it. You just need:

- [`thor`](https://github.com/wycats/thor): for the interface
- `bundler`: to publish the package
- [`aruba`](https://github.com/cucumber/aruba/): heck you can even cucumber test the cli, just like this:

  ```
  Feature: Ping
    As a CLI
    I want to test if the program works

    Scenario: It works
      When I run `bit ping`
      Then the output should contain "pong!"
  ```

This [guide](https://bundler.io/guides/creating_gem.html) has everything you need to build your gem.


## lessons learned

> When in doubt, make a CLI  
> *me, probably*

I can believe there are already 1000 people who downloaded my gems.

![rubygem-profile](https://user-images.githubusercontent.com/20739693/130351898-e5501788-8834-4eb9-983b-d1985c4b9809.png)

Never before had I felt so much responsible for my code. I did put a great effort into writing tests but those gems were experimentally lack of features. Sorry for the clickbaity description, but thanks for the motivation to make better software.
