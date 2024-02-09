# Project: ETL-Weather-Analysis

## Overview

This project aims to create an automated Extract, Transform, Load (ETL) process to extract daily weather forecast and observed weather data and load it into a live report for further analysis by the analytics team. As part of a larger prediction modeling project, the team wants to use the report to monitor and measure the historical accuracy of temperature forecasts by source and station.

As a proof-of-concept (POC), the initial scope involves performing these tasks for a single station and one data source. For each day at noon (local time), the project will gather both the actual temperature and the temperature forecasted for noon on the following day for Okinawa, Japan.

At a later stage, the team anticipates extending the report to include lists of locations, different forecasting sources, different update frequencies, and other weather metrics such as wind speed and direction, precipitation, and visibility.

## Data Source

For this practice project, the weather data package provided by the open-source project wttr.in will be used. Wttr.in is a web service that provides weather forecast information in a simple and text-based format. For further information, you can read more about the service on its [GitHub Repo](https://github.com/chubin/wttr.in).

To access weather data for Okinawa, Japan, you can use the following command:

```bash
curl wttr.in/okinawa

## Objectives

**Download raw weather data:**
- Set up a process to fetch raw weather data from the wttr.in service.

**Extract data of interest from the raw data:**
- Identify and extract relevant information, including actual and forecasted temperatures.

**Transform the data as required:**
- Perform any necessary data transformations, conversions, or calculations.

**Load the data into a log file using a tabular format:**
- Store the processed data in a structured format for easy analysis.

**Schedule the entire process to run automatically at a set time daily:**
- Automate the ETL process to ensure regular and timely updates.

## Weather Reporting

Extract and store the following data every day at noon, local time, for Okinawa, Japan:

| Year | Month | Day | Obs_Temp | Fc_Temp |
|------|-------|-----|----------|---------|
| 2024 | 1     | 1   | 20       | 19      |
| 2024 | 1     | 2   | 23       | 22      |
| 2024 | 1     | 3   | 19       | 20      |
| ...  | ..    | ..  | ..       | ..      |

Here, `Obs_Temp` represents the actual temperature (in degrees Celsius), and `Fc_Temp` represents the forecasted temperature (in degrees Celsius) for the following day at noon.
