## DoorDash Marketing Analyses and the Case of a Suspicious Customer.

**Introduction:** I am doing this project to understand better what kind of #data we can pull out from a Marketing campaign in a Food delivery business.

I am playing a role as the #data Analyst that will summarize the information, so can be more easily understandable.

Overall, the company wants to improve it's marketing & wants to see who has purchased following a marketing campaign.

### I learned that:

- Investigating and building a dashboard is not enough, it’s necessary to know how to explain the data.

- It’s important to understand from where the Data comes from.

- Data is really interesting and I enjoy working with the several aspects of it.

###  The Data

This project was modified from an iFood job interview case study, the Brazilian equivalent of DoorDash.

The data is 98% real, but slightly modified for educational purposes. 

<img src="images/1671479605588.png?raw=true"/>

I am from Brazil and I believe I can read some trends, dates and customer behaviors, so keep in mind that we actually are analyzing Ifood from Brazil.


<img src="images/1671479674361.jpg?raw=true"/>

###  Analyses

Once the data was all cleaned up the objective was to understand the data and summarize it in to answer some questions from my “Marketing Manager”.

I started adding a new column to give a unique ID for each entry. Then analyzing campaign number 6 using filtered rows we can see by the graph below that 333 customers bought in campaign 6, but the 2nd campaign was a fiasco, with only 30 customers.


A total of 1601 customers did not buy from campaigns, which means 73% of total customers.


Did we learn from our mistakes and got better, or did we use different approaches in each campaign?


<img src="images/1671479947875.png?raw=true"/>

Based on this information I would recommend to find out what was the type of campaign (tools used, advertising, type of discounts, targets) used in the 2nd vs the 6th, for comparison.

With data aggregation formulas I could deliver the following information:

<img src="images/1671480085486.png?raw=true"/>

- How many customers were there? (still for campaign 6)(=SUBTOTAL(2,Main!A2:A2205) 

- How old is the oldest customer? (=MAX(Main!Z2:Z2205)

- What is the average amount spent by each customer in this segment? (=AVERAGE(Main[MntTotal])

- What's the total amount spent by customers? (=SUM(Main!C2:C2205)

- Who is the most recently acquired customer? (=MIN(Main[Customer_Days]))

Next, I added a new column named PCTIncome that represents the percentage of customers income that was spent with this company:

<img src="images/1671480211950.png?raw=true"/>

Here is the suspicious customer I mentioned in the beginning.

Customer number 21 spent 70.66% of he/she total income, only in food delivery? 🤷

So, I went to review the data to see if the cleaning and all the process of preparation was all right.

Assuming is from a secure source, “our database”, we can see it is a suspicious behavior. That is the first red flag about this particular client.👀

<img src="images/1671480323824.gif?raw=true"/>

I added a column with Age Group using the aggregation formula below, to separate in more specific groups the clientele.

=IF(AND(Z5 < 36, Z5>23), "24-35",IF(AND(Z5 < 51, Z5>35), "26-50",IF(AND(Z5 < 66, Z5>50), "51-65",IF(Z5>65, "66+", "?"))))

<img src="images/1671480424660.png?raw=true"/>

Since the age group between 24-35 was the one that spent less, maybe we could think how to increase the spend for the younger audience.

By filtering, I found out that customer 21 is 41 years old.

###  Scatter Plot.

With the scatter plot visual we can see amount spent vs Income.

No surprise here, we can see a general trend (dotted line) that more someone makes, the more they spend at the store.

The R-squared value is a measure of well we could "predict" how much a customer would spend, given we know their income.

Which means that the marketing team, try to target higher-income customers as they tend to spend more with us.

<img src="images/1671480577769.png?raw=true"/>

Again, we can spot what I probably think is Customer 21 and another fella as both outliers.

One has a very high income but doesn't spend much with the store. The other, has a low income, but spends quite a bit with the store.

It would be interesting to dive deeper on these two customers and see what's going on. In a real case scenario, we should be asking: Do we have the correct income for them? Do we have the correct spent? Is the Data correct?

###  Histogram.

The Histogram visual shows a right skewed distribution. It explains that with more frequency the amount spent is between $4 -$419.

<img src="images/1671480424660.png?raw=true"/>

With the graph below we can view better how many customer joined the store by month:

<img src="images/1671483132209.png?raw=true"/>


January is a success and I believe it's because of the new year. In Brazil people travel a lot in this vacation and summer period. Also, in December they received the mandated bonus from previous year and are willing to pumper their selves a little more.


Usually February and March are the months of Brazilian carnival, people travel, celebrate and party more.

August is a huge success between the ages of 51-56 and I think it is because it is the same month of father's day. Meat would be a huge success for BBQ.

Here I can see that mysterious 21 joined in May and spent $1725 only in meat Products. May is the month of mother's day in Brazil.

With the visual below we have an idea of marital status of people that bought within all campaigns.

<img src="images/1671484277886.png?raw=true"/>

At this point I found out that our fella 21 is married and did not buy in any campaign.

A total of 1601 customers did not buy from campaigns, which means 73% of total customers.

###  My thoughts on customer 21?

Let's recapitulate:

$1725 spend only in meat products when it's income is $2447.

28 purchases made trough the catalogue, and 15 made with discount. 1 kid at home and married.

<img src="images/1671484565591.jpg?raw=true"/>

Possibilities:

1. Cloned credit card.
Another person stole the credit card information from our client and made the purchases. In this case, is it a intern security issue in our system? or is is a fake customer with a stolen credit card?
21 is lying:

2. Customer 21 is a rich individual that is used to cheat tax declarations. So, when subscribing to our services he/she puts a lower income exactly the same way he/she does it when filling the taxes form.
Probably the person is making more money than declared and so it has the means to spent a lot more. But from where it comes the money? Well, criminals also need to eat.🍕

3. Client 21 is a person that buys for a company.
So, in his/her records there are personal information, but in fact the purchase is to a 3rd party, I assume a company or boss. In that case, the person benefits receiving credit points, or special discounts! If the boss or company allows, it's just fine. We will never know.

###  Conclusion

We know for example that married customers at age group 51-56 were the populations that spent more during the campaigns.

Should we focus on retaining those clients or use another approach to reach the other age groups?


Now it's time to plan further for the next case.


With this project I would like to show that I taking seriously the exercise in read and interpret data. I also find fascinating to find anomalies and just make possible assumptions so we can dive more into the investigation.


My final Dashboard is the one below, with tons of possibilities to interpret Data, thanks to the interactive slicers.


Let me know what you think about Customer 21, do you have a new assumption?
or
What would you do for the next campaign?

<img src="images/1671485411500.png?raw=true"/>



