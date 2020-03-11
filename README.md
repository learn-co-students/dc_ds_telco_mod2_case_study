#Churn Case Study

## Context
"Predict behavior to retain customers. You can analyze all relevant customer data and develop focused customer retention programs." [IBM Sample Data Sets]

**Client**: Telco Company in the USA offering triple play (Phone, internet and TV)

New competitor entered offering triple play, resulting in increased churn

Want better way to spot potential churning customers and suggested actions what to do

**Assignment**:

- determine how many different plans (combinations of phone, protection, online backup, tech support, etc) there are
- create an average monthly bill for each customer (hint - divide total by tenure)
- find the "distribution" of people across plans. which plan is most popular?
- Which plan makes the most money? what if you control for how many people in each plan?
- What plan should they advertise the most?
- From which plan do people leave the most (that's the variable "churn"

### Concepts:

#### Type of churn:

**Voluntary** – they left after contract was up

**Involuntary** – we fired them

**Early churn** – left early, broke contract

##### Churn is a survival problem:
We are assuming that all are Early Churn

- Predicting who will churn next month is really hard
- Predicting who may churn over next 3 months is easier

There are many reasons to churn -> **feature engineering is king**

[churn funnel]

[Actions]

### Data
```
url_link = 'https://docs.google.com/spreadsheets/d/1TAWfdKnWYiCzKUeDyGL6NzIOv7AxFt_Sfzzax464_FQ/export?format=csv&gid=882919979'

telco = pd.read_csv(url_link)
```

Each row represents a customer, each column contains customer’s attributes described on the column Metadata.

The data set includes information about:

- Customers who left within the last month – the column is called Churn
- Services that each customer has signed up for – phone, multiple lines, internet, online security, online backup, device protection, tech support, and streaming TV and movies
- Customer account information – how long they’ve been a customer, contract, payment method, paperless billing, monthly charges, and total charges
- Demographic info about customers – gender, age range, and if they have partners and dependents
- Usage - information about their usage patterns
