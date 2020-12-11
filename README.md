# shobhit-bishnoi
Reports developer -Shobhit Bishnoi
Section 1 - Queries
Consider the following employee data in relational tables and write queries for questions below the data:
1.	Write a query to print the number of employees per department in the organization

SELECT DEPARTMENT, COUNT(*)
  FROM Employee
  GROUP BY DEPARTMENT;



2.	Write an SQL query to find the name of the top-level manager of each department

SELECT DEPARTMENT,MAX(SALARY) MAXSALARY FROM EMPLOYEE GROUP BY DEPARTMENT ORDER BY MAXSALARY ASC;


3.	Write a query to find the total incentive received by a given employee in a given month.

SELECT DEPARTMENT,(SELECT IFNULL (MAX(INCENTIVE_AMOUNT),0) FROM INCENTIVES WHERE EMPLOYEE_REF_ID=EMPLOYEE_ID) MAX_INCENTIVE FROM EMPLOYEE;


4.	Write a query to find the month where employees got maximum incentive

SELECT FIRST_NAME,INCENTIVE_AMOUNT,DENSE_RANK() OVER (PARTITION BY INCENTIVE_DATE ORDER BY  INCENTIVE_AMOUNT DESC) AS RANK FROM EMPLOYEE A, INCENTIVES B WHERE A.EMPLOYEE_ID = B.EMPLOYEE_REF_ID;



Section 2: Please read through the problems/questions and write down your answer. 
5. You have two sand timers, which can show 4 minutes and 7 minutes respectively. Use both the sand timers (at a time or one after other or any other combination) and measure a time of 9 minutes.

Start both the timers at a time.
Filp over 4 m timer twise & so that when 7m timer is over , flip it .
There is sand remaining in 4m timer for one minute.
Start 7m timer and when one minute sand in 4m timer is over mark that point on 7m timer.
We will get one minute marking on 7m timer.
Now start 4m timer and then flip it over so that we get 4+ 4 = 8m and then start 7m timer up to one minute mark , we will get:
4+4+1 = 9 minutes.


6. John and Mary are a married couple. They have two kids, one of them is a girl. Assume safely that the probability of each gender is 1/2. What is the probability that the other kid is also a girl?

Probability of each gender = ½

Probability of other child is totally independent of gender of first child so we can say that 
Probability of other kid also a girl is= ½ 







7.  The following appeared as part of a campaign to sell advertising time on a local radio station to local businesses. 
Ron’s Cafe began advertising on our local radio station this year and was delighted to see its business increase by 10 percent over last year's totals. Their success shows you how you can use radio advertising to make your business more profitable. 
Discuss how well reasoned you find this argument. In your discussion be sure to analyze the line of reasoning and the use of evidence in the argument. For example, you may need to consider what questionable assumptions underline the thinking and what alternative explanations or counterexamples might weaken the conclusion. You can also discuss what sort of evidence would strengthen or refute the argument, what changes in the argument would make it more logically sound and what, if anything, would help you better evaluate in conclusion.



The author in the argument concludes that as the Ron’s cafe increased its business by 10 percent over the last year by advertising in the local radio station, so other businesses should follow suit and advertise their businesses on the local radio to make their business more profitable. However, the argument is flawed because it fails to supply sufficient support in favor of the argument.

First, we are told that for Ron’s Cafe increased its business by 10 percent over the last year by advertising in the local radio, but it has not been mentioned that whether the increase in the business was offset by the amount of money spent on advertisement in the radio channel. If the previous scenario holds true, then companies actually might not be increasing their profits.
Second, Even if we consider that the business for Ron’s Cafe increased after it advertised in the local radio, we cannot be sure that this will happen for other businesses. It could well be the case that many people who listen to the radio might be coffee consumers, but might not be interested in other products. Therefore, the generalization that the author makes based on a single case might not hold true for other scenarios or businesses.
Finally, there could be other alternate reasons that could have contributed to the success of the cafe business such as opening of a new outlet or better management of the cafe resources or introduction of a new product in the cafe outlet that sold well. Any of these reasons could account for the increase in the business. Therefore, advertising in the local radio might not be the only contributor for the increase in the cafe business. the above the argument is flawed and it can be strengthened if the above concerns are addressed.
