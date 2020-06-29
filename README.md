# empatpuluh

OpenFortiVPN wrapper with automatic OTP retrieval from IMAP address.

# Why?

Just scratching my own itch.

I use multiple FortiVPN profiles at work which send OTP via corporate email instead of shared key. Automating the copy-paste process can ease the context switching. 

# Getting started

Sample config (`$HOME/.empatpuluh.yml`). You can use YAML anchor to reduce repetitive configs.

```yaml
profiles:
- name: production
  vpn_config: /home/johndoe/vpn/production.cfg
  otp_prompt: "Two-factor authentication token:"
  search_delay: 2s
  search_sender: vpn@company.com
  search_mailbox: OTP
  search_within: 60s
  search_field: subject
  search_regex: 'AuthCode: (\d+)'
  imap:
    host: imap.gmail.com
    port: 993
    username: johndoe@company.com
    password: abcdefgghijklmnopqrstuvwxyz
```

Then you can connect by running `sudo empatpuluh connect production`.
