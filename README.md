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

# Usage

Update employee.config and paystub.example. Then:

   ./401k-match-assistant --config employee.config paystub.example

Example output:

    Estimated End of Year Summary
            61,000  Aggregate limit (employer + employee)
            6,500   Catch up contribution limit (age 55)

            20,500  401k employee contribution (deferral) limit
            10,750  401k employee contribution
            9,749   Difference (under contribution)

            15,250  401k employer match limit
            5,750   401k employer match

            44,499  After-tax contribution limit
            15,000  After-tax contribution
            29,499  After-tax under contribution

    FAIL  Maxed out employee pre-tax contribution
    FAIL  Avoided true-up by reaching employee limit in final paycheck
    PASS  Maxed employer match by contributing at least 5% of eligible pay
