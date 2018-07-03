# Firealarm

Notification for your git repository

## Usage

### Create `.firealarm.yml`

```yaml
version: 1.0

# Context will be inject into template
context:
    name: Yeung Yiu Hung
    date: ${SERVER_TIME}
    changes: ${CHANGELOG}
    service_name: Awesome Server

mail:
    to:
        - User 1 <user_one@example.com>
    cc:
        - User 2 <user_two@example.com>
        - User 3 <user_three@example.com>
    template: ./example.tmpl.html

slack:
    hooks:
        - https://hook1.url
        - https://hook2.url
    template: ./slack.tmpl.html
```

### Email

```sh
firealarm mail # export email
```

### Slack

```sh
firealarm slack
```
