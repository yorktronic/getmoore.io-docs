# Amazon Web Services (AWS) #

## On-Demand ##

## Spot ##

### Overview ###

Discounted pricing for when AWS' data-center utilization is low. AWS issues pricing 
offers that are structured similarly to on-demand pricing. As with on-demand, the 
prices are listed per VM instance type, with identical descriptive information. The 
difference lies in how the instance is reserved. With on-demand, a user creates a VM at 
an agreed-upon hourly price that is effective for as long as that instance is alive. 
In the case of spot pricing, the user sets an upper limit that they are willing to 
pay for the instance, like bidding on a product on eBay. If their upper limit is above 
the current spot price, then the instance is created, otherwise the instance is created later 
once the spot price falls below the user's uper limit. Once the spot price rises 
above the user's upper limit, the instance is terminated.

See [Amazon EC2 Spot Instances Pricing](https://aws.amazon.com/ec2/spot/pricing/) for more information.

### Data Structure ###
**Source:** [AWS CLI](https://aws.amazon.com/cli/) [describe-spot-price-history](http://docs.aws.amazon.com/cli/latest/reference/ec2/describe-spot-price-history.html)  
**Format:** JSON  
**Structure:**
```json
{
  "SpotPriceHistory": [
          {
              "Timestamp": "2014-01-06T07:10:55.000Z",
              "ProductDescription": "SUSE Linux",
              "InstanceType": "m1.xlarge",
              "SpotPrice": "0.087000",
              "AvailabilityZone": "us-west-1b"
          }]
}
```
	
## Reserved ##
**Source:** Pricing can be found within the AmazonEC2 offer file provided via the 
[AWS Price List API](http://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/price-changes.html#download-offers)  
Example: `https://pricing.us-east-1.amazonaws.com/offers/v1.0/aws/AmazonEC2/current/index.json
`    
**Format:** JSON or CSV
**Structure:** TBD

# Google Cloud Platform #

## On-Demand ##

## Preemptible ##
Same concept as AWS' "Spot" pricing

## Reserved ## 