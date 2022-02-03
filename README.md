# 401k Match Assistant

A Python script to assist employees in maximizing their 401(k) contributions,
including employer matching and after-tax (mega backdoor roth) contributions.

The script currently handles the following cases:

* IRS limits for 2021 and 2022 tax years
* Catchup contributions for ages 50 and older
* Warns on under contribution for employee deferral (regular 401(k) contributions)
* Warns on under contribution resulting in loss of employer match
* Warns on non-optimal contributions requiring a "true up" (employer
  contribution adjustment in following tax year to meet matching obligation)
* Warns on over-contribution for after-tax (mega backdoor roth) contributions
  (employers do not automatically cap out after-tax contributions)
