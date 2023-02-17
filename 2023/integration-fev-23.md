# Python Integration Developer February 2023 #

Hello candidate, at this stage you will have your knowledge tested.
We recommend that you use good programming practices and develop well-structured code.

## Delivery time ##
**March 01, 2023, Wednesday, until 23:59.**

Under no circumstances will tests be accepted after the deadline.


## What to send ##

The candidate must send the **code** that was developed. The use of frameworks that require installation by the evaluator will not be allowed.
You can use libraries (pip) as long as no additional steps are needed for the evaluator to carry out the project and the library must be listened on **requirements.txt** file.
Projects that do not run when running python3.7 your_main_file.py will be disregarded.
Accepted codes:
- Python 3.7

The candidate must send an email to **cayke@instabuy.com.br** by the deadline specified above. In the email the subject should be **"Dev Integracao Fev-23"**.
Emails with another subject will be disregarded.
In the email, state your **name and contact telephone number**.
It is also necessary to send your **resume and/or portfolio**.
It is recommended that you send the github link of the project, and not the files itself.
We recommend that all of the project code is developed in english.

Instabuy wishes everyone good luck. We look forward to working together!!!


# Integration Test #

The test consists of updating products infos from an CSV file.
You will have to read the file, parse the infos and make requests to the Instabuy API.


## Authentication ##
We use api-key to authenticate your request.
Please use the token below for this test.

```
kUs5p-K-sIOMT_hfg2FOYFie7iqRD2pn47jfvPQElLQ
```

For more infos check: https://docs.instabuy.com.br/admin.html#authentication


## Request ##

```
- BASE URL: https://api.instabuy.com.br/store/
- ENDPOINT: products
- METHOD: PUT
```

Relevant request data must be consulted in the our official documentation:
https://docs.instabuy.com.br/admin.html#products


## Response ##

All responses have 4 fields: status, data, count, http_status.

Relevant request data must be consulted in the our official documentation:
https://docs.instabuy.com.br/admin.html#request-response-format


## CSV File ##
Download the file [here](https://github.com/Instabuy-Ltda/Instabuy-Selecao/blob/master/assets/items.csv). 
