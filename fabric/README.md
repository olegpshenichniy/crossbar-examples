# CFC Client

## Authenticating and connecting

1. Register

First time the client start, it will generate a new (private) key and then register

```console
python client.py --authid="nobody@example.com"
```

This will trigger sending of an email with an activation code to the email address given.

> To force resending a (new) activation code, do `python client.py --authid="nobody@example.com" --request_new_activation_code=true`

2. Activate

The activation code received via email now needs to be provided as a command line argument

```console
python client.py --authid="nobody@example.com" --activation_code="PJGS-HYJP-UK6A"
```

3. Use

Finally, all of above for pairing only needs to be done once. After that, usage is completely transparent.

```console
python client.py
```
