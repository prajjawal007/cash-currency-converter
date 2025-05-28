# 💱 Cash Currency Converter

**`cash-currency-converter`** is a lightweight and easy-to-use Node.js utility for converting currency values in real-time using up-to-date exchange rates. It's ideal for web apps, financial dashboards, CLI tools, or any application that needs reliable currency conversion.

---

## 📦 Installation

Install via **NPM**:

```bash
npm install cash-currency-converter
```

Or using **Yarn**:

```bash
yarn add cash-currency-converter
```

---

## ⚙️ Usage

```js
const convertCurrency = require('cash-currency-converter');

(async () => {
  const result = await convertCurrency({
    amount: 100,
    from: 'USD',
    to: 'INR'
  });

  console.log(result);
})();
```

---

## 📌 Parameters

| Parameter | Type   | Required | Description                              |
| --------- | ------ | -------- | ---------------------------------------- |
| `amount`  | number | ✅ Yes    | The amount of money to convert           |
| `from`    | string | ✅ Yes    | The source currency code (e.g., `'USD'`) |
| `to`      | string | ✅ Yes    | The target currency code (e.g., `'INR'`) |

> Currency codes must follow [ISO 4217](https://en.wikipedia.org/wiki/ISO_4217) standards (e.g., `USD`, `EUR`, `JPY`, etc.).

---

## 🔍 Example Output

```json
{
  "amount": 100,
  "converted": 8312.55,
  "from": "USD",
  "to": "INR",
  "rate": 83.1255
}
```

---

## 🌐 Supported Currencies

Includes most major global currencies:

* 🇺🇸 USD – US Dollar
* 🇪🇺 EUR – Euro
* 🇬🇧 GBP – British Pound
* 🇮🇳 INR – Indian Rupee
* 🇯🇵 JPY – Japanese Yen
* 🇨🇦 CAD – Canadian Dollar
* 🇦🇺 AUD – Australian Dollar
* 🇨🇳 CNY – Chinese Yuan

---

## 📡 How It Works

The module fetches the latest exchange rates from public APIs like [Frankfurter](https://www.frankfurter.app/) or [ExchangeRate-API](https://www.exchangerate-api.com/), and calculates the conversion using the formula:

```
converted = amount × exchange_rate
```

---

## 🧪 Development

Clone the repository and install dependencies:

```bash
git clone https://github.com/your-username/cash-currency-converter.git
cd cash-currency-converter
npm install
```

Run the module locally:

```bash
node index.js
```

---

## 🔧 API Configuration

For paid or limited APIs, set your API key in an `.env` file or directly in the code. Example with `fetch`:

```js
fetch(`https://api.exchangerate-api.com/v4/latest/${from}?apikey=YOUR_KEY`)
```

---

## 🔩 Customization Ideas

You can extend the utility with features like:

* 🔁 **Caching** – to reduce API requests
* 💻 **CLI Support** – run directly from the terminal
* 🌍 **Locale Formatting** – format output using `Intl.NumberFormat`
* 📦 **Offline Support** – fallback with static rates

---

## 📥 Contributing

We welcome contributions!

1. Fork the repository
2. Create your branch: `git checkout -b feature/your-feature`
3. Make changes and commit: `git commit -m "Add your feature"`
4. Push: `git push origin feature/your-feature`
5. Open a Pull Request

---

## 📄 License

Licensed under the [MIT License](LICENSE).

---

## 🙌 Acknowledgments

Thanks to:

* [ExchangeRate-API](https://www.exchangerate-api.com/)
* [Frankfurter API](https://www.frankfurter.app/)
* [Node.js](https://nodejs.org/)

---

## ✨ Author

**Your Name**
GitHub: [@prajjawal007](https://github.com/prajjawal007)
NPM: [cash-currency-converter](https://www.npmjs.com/package/cash-currency-converter)

> ⭐️ Star this repo if you find it useful!
