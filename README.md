# CoWIN Dashboard

A responsive and dynamic React-based dashboard to visualize COVID-19 vaccination statistics using charts from the `recharts` library. This project displays the latest data for:

- **Vaccination Coverage (Last 7 Days)**
- **Vaccination by Gender**
- **Vaccination by Age Group**

### Live Demo

Check out the live application here: [CoWIN Dashboard](https://chiragcowin.ccbp.tech/)

---

## Repository Information

This project is developed using the following technologies:
- **JavaScript** (62.5%)
- **HTML** (20.2%)
- **CSS** (17.3%)

It provides real-time vaccination data fetched from the API: `https://apis.ccbp.in/covid-vaccination-data`. It features a bar chart for last 7 days' vaccinations, pie charts for vaccinations categorized by gender and age, as well as a failure view for API errors.

---

### Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/chiragSahani/cowinDashboard.git
   cd cowinDashboard
2.Install dependencies

```bash
npm install
```

Start the application

```bash

npm start
```
## Features

- Fetches real-time vaccination data from the API: `https://apis.ccbp.in/covid-vaccination-data`
- Displays:
  - Bar chart for last 7 days’ dose-wise vaccinations
  - Pie charts for vaccinations categorized by **gender** and **age**
- Loader animation during API request
- Graceful error handling with a failure view on network/API failure

---

## Component Structure

<div align="center">
  <img src="https://assets.ccbp.in/frontend/content/react-js/cowin-dashbaord-component-structure-breakdown.png" alt="component-structure" width="100%" />
</div>

---

## API Response Structure

```json
{
  "last_7_days_vaccination": [
    {
      "vaccine_date": "30th Jul",
      "dose_1": 3757930,
      "dose_2": 1817805
    }
  ],
  "vaccination_by_age": [
    {
      "age": "18-44",
      "count": 482792375
    }
  ],
  "vaccination_by_gender": [
    {
      "count": 4809680,
      "gender": "Male"
    }
  ]
}
```

---

## Assets Used

- Logo: [cowin-logo.png](https://assets.ccbp.in/frontend/react-js/cowin-logo.png)
- Failure View: [api-failure-view.png](https://assets.ccbp.in/frontend/react-js/api-failure-view.png)

---

## Styling & Design

- **Fonts**: Roboto
- **Colors**:  
  `#161625`, `#2cc6c6`, `#cbd5e1`, `#1c1c2b`, `#2d87bb`, `#a3df9f`, `#64c2a6`, `#94a3b8`, `#f54394`, `#5a8dee`

---

## Folder Structure

```
src/
│
├── components/
│   ├── CowinDashboard/
│   ├── VaccinationCoverage/
│   ├── VaccinationByGender/
│   └── VaccinationByAge/
│
├── App.js
└── index.js
```

---

## License

This project is for educational and demonstration purposes.

--- 

Let me know if you'd like to add badges, deployment links, or contributor info too.
<br/>
<div style="text-align: center;">
    <img src="https://assets.ccbp.in/frontend/content/react-js/cowin-dashbaord-output.gif" alt="" style="max-width:70%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
</div>
<br/>

**Failure View**

<br/>
<div style="text-align: center;">
    <img src="https://assets.ccbp.in/frontend/content/react-js/cowin-dashbaord-failure-view-output.gif" alt="cowin-dashboard-failure-view-output" style="max-width:70%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
</div>
<br/>

### Design Files

<details>
<summary>Click to view</summary>

- [Extra Large Devices (Size >= 1200px) - Success View](https://assets.ccbp.in/frontend/content/react-js/cowin-dashboard-xl-output.png)
- [Extra Large Devices (Size >= 1200px) - Failure View](https://assets.ccbp.in/frontend/content/react-js/cowin-dashbaord-xl-failure-view-output.png)

</details>

### Set Up Instructions

<details>
<summary>Click to view</summary>

- Download dependencies by running `npm install`
- Start up the app using `npm start`
</details>

### Completion Instructions

<details>
<summary>Functionality to be added</summary>
<br/>

The app must have the following functionalities

- When the page is opened,
  - An HTTP GET request should be made to **covidVaccinationDataApiUrl**
  - **_loader_** should be displayed while the HTTP request is fetching the data
  - After the data is fetched successfully, the response received should be displayed using different charts from `recharts`
  - The last 7 days vaccination data should be displayed using the `BarChart` component from `recharts`
  - The data for vaccination by gender and vaccination by age should be displayed as two different pie charts using the `PieChart` component from `recharts`
  - If the HTTP GET request made is unsuccessful, then the [FailureView](https://assets.ccbp.in/frontend/react-js/api-failure-view.png) should be displayed

</details>

<details>

<summary>API Requests & Responses</summary>
<br/>

**covidVaccinationDataApiUrl**

#### API: `https://apis.ccbp.in/covid-vaccination-data`

#### Method: `GET`

#### Description:

Returns a response containing the list of Products

#### Success Response

```json
{
  "last_7_days_vaccination": [
    {
      "vaccine_date": "30th Jul",
      "dose_1": 3757930,
      "dose_2": 1817805
    },
    ...
  ],
  "vaccination_by_age": [
    {
      "age": "18-44",
      "count": 482792375
    },
    ...
  ],
  "vaccination_by_gender": [
    {
      "count": 4809680,
      "gender": "Male"
    },
    ...
  ]
}
```

</details>

<details>
<summary>Components Structure</summary>

<br/>
<div style="text-align: center;">
    <img src="https://assets.ccbp.in/frontend/content/react-js/cowin-dashbaord-component-structure-breakdown.png" alt="component-breakdown-structure" style="max-width:100%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
</div>
<br/>

</details>

<details>
<summary>Implementation Files</summary>
<br/>

Use these files to complete the implementation:

- `src/components/CowinDashboard/index.js`
- `src/components/CowinDashboard/index.css`
- `src/components/VaccinationCoverage/index.js`
- `src/components/VaccinationCoverage/index.css`
- `src/components/VaccinationByGender/index.js`
- `src/components/VaccinationByGender/index.css`
- `src/components/VaccinationByAge/index.js`
- `src/components/VaccinationByAge/index.css`

</details>

### Important Note

<details>
<summary>Click to view</summary>

<br/>

**The following instructions are required for the tests to pass**

- Wrap the Loader component with an HTML container element and add the `data-testid` attribute value as `loader` to it

  ```jsx
  <div data-testid="loader">
    <Loader type="ThreeDots" color="#ffffff" height={80} width={80} />
  </div>
  ```

- Provide `width` and `height` to the respective chart component to make the charts visible on the page <br> For example:

  ```jsx
  <BarChart width={1000} height={300} />
  ```

  - Provide `width` and `height` as **number**

  - Achieve this CoWIN Dashboard on desktop devices. You can try different charts provided by the `recharts` package with customized data

</details>

### Resources

<details>
<summary>Image URLs</summary>

- [https://assets.ccbp.in/frontend/react-js/api-failure-view.png](https://assets.ccbp.in/frontend/react-js/api-failure-view.png) alt should be **failure view**
- [https://assets.ccbp.in/frontend/react-js/cowin-logo.png](https://assets.ccbp.in/frontend/react-js/cowin-logo.png) alt should be **website logo**

</details>

<details>
<summary>Colors</summary>

<br/>

<div style="background-color: #161625; width: 150px; padding: 10px; color: white">Hex: #161625</div>
<div style="background-color: #2cc6c6; width: 150px; padding: 10px; color: black">Hex: #2cc6c6</div>
<div style="background-color: #cbd5e1; width: 150px; padding: 10px; color: black">Hex: #cbd5e1</div>
<div style="background-color: #ffffff; width: 150px; padding: 10px; color: black">Hex: #ffffff</div>
<div style="background-color: #1c1c2b; width: 150px; padding: 10px; color: white">Hex: #1c1c2b</div>
<div style="background-color: #2d87bb; width: 150px; padding: 10px; color: black">Hex: #2d87bb</div>
<div style="background-color: #a3df9f; width: 150px; padding: 10px; color: black">Hex: #a3df9f</div>
<div style="background-color: #64c2a6; width: 150px; padding: 10px; color: black">Hex: #64c2a6</div>
<div style="background-color: #94a3b8; width: 150px; padding: 10px; color: black">Hex: #94a3b8</div>
<div style="background-color: #f54394; width: 150px; padding: 10px; color: black">Hex: #f54394</div>
<div style="background-color: #5a8dee; width: 150px; padding: 10px; color: black">Hex: #5a8dee</div>
<div style="background-color: #2cc6c6; width: 150px; padding: 10px; color: black">Hex: #2cc6c6</div>
<div style="background-color: #6c757d; width: 150px; padding: 10px; color: black">Hex: #6c757d</div>
<div style="background-color: #5a8dee; width: 150px; padding: 10px; color: black">Hex: #5a8dee</div>

</details>

<details>
<summary>Font-families</summary>

- Roboto

</details>

> ### _Things to Keep in Mind_
>
> - All components you implement should go in the `src/components` directory.
> - Don't change the component folder names as those are the files being imported into the tests.
> - **Do not remove the pre-filled code**.
> - Want to quickly review some of the concepts you’ve been learning? Take a look at the Cheat Sheets.
