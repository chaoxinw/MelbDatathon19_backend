# MelbDatathon19_backend
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
