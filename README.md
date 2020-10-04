# MelbDatathon19 Backend
Backend for Melbourne Datathon 2019

## Two functions
### 1. Estimate sugarcane yield from a selected region
```http
POST https://sugeromelbdata.com:5000/yield_estimation
```

| Parameter | Type | Description |
| :--- | :--- | :--- |
| `ratoonStartDate` | `string` | **Required**. Sugarcane ratoon date since last harvest. |
| `harvestStartDate` | `string` | **Required**. The date when starting to harvest sugarcane. |
| `latlonlist` | `list of float` | **Required**. The sugarcane region. |

This will return the estimated yield for a given sugarcane region. 

### 2. Forecast future sugarcane NDVI
```http
POST https://sugeromelbdata.com:5000/forecast
```

| Parameter | Type | Description |
| :--- | :--- | :--- |
| `futureDate` | `string` | **Required**. A date in the future. |
| `drought` | `boolean` | **Required**. Whether there would be drought. |

The timeseries machine learning model utilises a technique called sliding window. 

This will return the predicted sugarcane NDVI value for the given area (Proserpine).
