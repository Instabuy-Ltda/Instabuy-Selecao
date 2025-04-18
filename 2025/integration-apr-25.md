
# 🧪 Python Integration Developer Test – April 2025

Hello candidate!  
At this stage, we will assess your technical skills. We recommend using clean code practices and writing well-structured, readable, and maintainable code.

---

## 📅 Deadline

**April 21, 2025 (Monday) at 23:59 BRT**

Submissions sent after the deadline **will not be accepted under any circumstances**.

---

## 🚀 What to Submit

You must send the **developed code**. You are allowed to use libraries installed via `pip`, as long as:

- They are listed in a `requirements.txt` file;
- No additional installation steps are required by the evaluator.

Your code must run using the command:

```bash
python3 your_main_file.py
```

If your code fails to run or requires manual setup, your submission may be disqualified.

**Accepted language:**
- Python 3

### Email Instructions

Send an email to **cayke@instabuy.com.br** with the **subject line**:  
**Dev Integracao APR-25**

Emails with incorrect subjects will be disregarded.

The email must include:

- Your **full name** and **contact phone number**  
- Your **resume and/or portfolio**  
- (Optional but recommended) A link to your **GitHub repository** for the project

We recommend writing all source code and comments in **English**.

---

## 🔗 The Challenge

The objective of this test is to read a CSV file containing product information and send the data to the Instabuy API.

Each line in the CSV contains data for a single product.

Your program must:

1. Read the CSV file;
2. Parse each product's data;
3. Make an authenticated `PUT` request to the Instabuy API to update the product;
4. Handle invalid or malformed lines gracefully.

If you have any questions, feel free to open an issue in the repository — our team will reply as soon as possible.

---

## 🔐 Authentication

We use an API key for authentication.

**Use the following token for this test:**

```
IGs8rlcEb0jUEgsNvzDsatF5gAvQ_8iGde-tZ-iwGFc
```

Refer to our [authentication documentation](https://docs.instabuy.com.br/admin.html#authentication) for more information.

---

## 📡 API Details

- **Base URL:** `https://api.instabuy.com.br/store/`
- **Endpoint:** `products`
- **Method:** `PUT`

Refer to the [official documentation](https://docs.instabuy.com.br/admin.html#products) to understand the request payload and required fields.

### Response Format

All responses will contain the following fields:

```json
{
  "status": "...",
  "data": "...",
  "count": ...,
  "http_status": ...
}
```

More info: [docs.instabuy.com.br – Request & Response Format](https://docs.instabuy.com.br/admin.html#request-response-format)

---

## 📄 CSV File

Download the file [here](https://github.com/Instabuy-Ltda/Instabuy-Selecao/blob/master/assets/items.csv)

---

Good luck!  
We’re excited to see your solution and hope to work together soon! 🚀  
**– Instabuy Team**
