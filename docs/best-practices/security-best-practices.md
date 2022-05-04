---
sidebar_position: 2
---

# Security Best Practices

Being a system administrator for a ubuntu computer requires technical knowledge of the system and best security practices.  The following list should help you get started and is considered the bare minimum for keeping your system safe.

## Keep Your System Up To Date

Make sure to regularly update packages in your ubuntu system.  Out of date packages may contain known security vulnerabilities that a hacker could exploit.  A good practice would be to update weekly at least. To update your system, do the following:

```
sudo apt update
sudo apt upgrade
```

## DO NOT Store Your Withdrawer Key On Your Validator

Your withdrawer key gives you full access to the vote account of your validator.  It is highly sensitive information and it should not be stored on the validator itself.  Make sure you create this key on a secure computer (other than your validator computer) and that you store it somewhere safe. Ideally you should store this key in cold storage like a hardware wallet or at the very least in a password protector so that a hacker could not get access to it directly.  Again, this should never be stored on your validator at any time.

## DO NOT Run The Solana Validator as a Root User

It may be easier to get started by running your application as root, but it is a bad practice. If there is an exploit in your system, a hacker could have much more access if your solana application is running as the root user. Instead, see the setup instructions for creating a user called `sol` and running the application as the `sol` user.

## Close Ports That Are Not In Use

Your system should close all ports that do not need to be open to the outside world. A common firewall for closing ports is ufw (uncomplicated firewall).  You can find a guide to using ufw from [digital ocean](https://www.digitalocean.com/community/tutorials/ufw-essentials-common-firewall-rules-and-commands).

## Eliminate Brute Force Attacks With fail2ban

[fail2ban](https://github.com/fail2ban/fail2ban) is a network security tool that checks your logs for suspicious login attempts and bans those IP addresses after repeated attempts.  This will help mitigate brute force attacks on your serve. A default setup should work by doing the following:

```
sudo apt install fail2ban
```
