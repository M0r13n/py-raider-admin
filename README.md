# py-raider-reporter


#### Raider Admin Interface for Python. Simply manage payouts from Python. Used in pair with [Raider](https://github.com/valeriansaliou/raider), the Affiliates Tracker Page.


## Who uses it?

<table>
<tr>
<td align="center"><a href="https://smartphoniker.shop/"><img src="https://smartphoniker.shop/static/images/smartphoniker-logo.svg" height="64" /></a></td>
</tr>
<tr>
<td align="center">Smartphoniker</td>
</tr>
</table>



# How to install
You need to expose your raider database in order to use this lib. It is recommended that you create a special remote user for that purpose.

Install with pip:

```sh
$ pip install py-raider-admin
```


# How to use
`raider-admin` can be instantiated as such:

```py
conf = {
    'host':'localhost',
    'database':'raider',
    'user':'some_user',
    'password':'some_pass'
}
admin = RaiderAdmin.from_config(conf)

# get the newest 100 open payouts
admin.get_open_payouts()

# get all payouts ever
admin.get_all_payouts(limit=100000)

# get account information for account id 345
admin.get_account_data(345)

# change status of payout with id 34 to processed
admin.set_status(34, PayoutStatus.Processed)
```


# What is Raider?
ℹ️ **Wondering what Raider is?** Check out **[valeriansaliou/raider](https://github.com/valeriansaliou/raider)**.