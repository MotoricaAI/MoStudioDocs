# Generation Credit System Guide

## Introduction
Motorica generations utilize a credit system. Animation generation costs credits and is simply calculated on a per second of generated animation basis, or CHS for short.

This guide walk through all details around credits as well as the user interface today.

## Generation Costs
The current plan equates **1 CHS (Generated Character Second) to 1 credit**.

This calculation is done anytime a generation takes place, with the duration of the output being the determining factor for how many credits is charged.

Examples:

- Generating a 2 second animation using your style = 2 credits
- Altering some parameter of the above 2 second generation and generating again = 2 credits
- Generating the same 2 second animation using the “random seed button” = 2 credits
- Changing parameters (i.e. acceleration speed) and then generating = 2 credits
- Extending original animation to 3 seconds (all else the same) = 3 credits

!!! note
    PDC generations will consume **1 credit per CHS** for the entire set. Therefore if the entire set is 100 seconds in total, then it will cost 100 credits to generate.

## Credit Management
As part of the February 12, 2025 update, you will now be able to view and manage your credits.
### Credit Usage History
#### Access
To access and see how many credits have been consumed historically:

1. Log into [app.staging.motorica.ai](https://app.staging.motorica.ai/)
2. Click on your account email in the upper right
3. Click on Settings

![](../assets/images/cred_mgmt/cred_view_owa.png)

#### Explanation
This view currently shows credit available for your entire Organization.

!!! info
    This view and placement is temporary, we will migrate this to our new wep app framework soon

The credit expense feed shows the additional details about each generation, such as:

* Date and time of the generation
* Style used for the generation
* Frames
* Credits consumed
* UserID

![](../assets/images/cred_mgmt/transactions_owa.png)

!!! info
    We intend to show emails instead UserID's soon

### Credit Management View
The Credit Plan view is already accessible in our new web app framework.

!!! info
    Depending account type, your view will vary slightly due to permission to alter credit plan

![](../assets/images/cred_mgmt/creds_view.png)

#### Account Types
For now, there are two account types for an organization. You may be an Owner or a Member.

**Owners** are the only account types allowed to adjust the credit plan. Members may still view credits remaining as well the current plan.

#### Accessing the Credit Management View
For all accounts access it by:

1. Logging into [motorica-beta-staging.web.app](https://motorica-beta-staging.web.app/)
2. Clicking on your email nameplate in the upper right corner
3. Clicking on "Credit management"

![](../assets/images/cred_mgmt/access_creds_nwa.png)

**Usable credits**: How many credits are left this month.
**Monthly credits**: How many credits your plan refreshes per month.

Credit plans are charge at the end of the billing period.
!!! warning
    Monthly credits do not roll over!

#### Adjusting your Credit Plan
Credit plans may only be adjusted at any time by an organization's Owner.

Credit plan adjustments happen at 1000 credit intervals.

**Upgrading** the credit plan will immediately:

1. Increase the existing available credits for the remainder of the billing period.
2. Add the updated credit plan cost to the next billing cycle.

![](../assets/images/cred_mgmt/upgrade_creds.png)

**Downgrading** your credit plan will immediately ensure:

1. The next billing period reflects the lower credit amount (billing adjusted accordingly)

![](../assets/images/cred_mgmt/downgrade_creds.png)

Downgrades will have no immediate effect on your usable credits for the current billing cycle.

#### Future Plans
We have many ideas to improve the overall credit management system. In no particular order they are:

* Unifying all credit related experiences takes place on our new web app framework
* Allowing more than one qualified user to adjust credits
* Improving the credit usage view to be more intuitive

We appreciate your use of our tools and for any feedback, please reach out on slack or use the "Feedback" button at the bottom right!