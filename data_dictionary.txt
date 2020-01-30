# Data dictionary

This document describes a standardized format for sharing data related to the 2019 novel coronavirus outbreak. The initial aim is to convert all data from public reports into a standardized and easily accessible format as a comma separated values (csv) file. Any tabular or non-tabular data may be captured in this format.

## Directory conventions

Data will first be organized on the country level. For each country with data products there will be a folder containing data for that country. If data is provided on a regional level, a separate folder will be created.

For each country, there may be multiple report types of interest. Each of these types will be assigned a 'short_name' using only ASCII characters and no spaces. The country-specific folder will contain a README document with basic information ('short_name', full name, brief description, url) for all report types included in the repository for that country. The README will also include the date of the earliest report captured in the database. A final report date will be added when the report changes substantially, the report is discontinued, or there is no longer support for updating the report. 

The country-specific folder will also include folders for each report type, identified by the 'short_name'. Within that folder there will be two additional folders, one labelled 'original_reports' for the original reports in pdf format or whatever is available, and the other labeled 'data' containing csv files prepared as specified here. 

The information from any given report will be captured in three csv files: 

1.	A report data file
2.	A country place names database
3.	A country data guide

The first, a report data file will be created for each report assimilated. The latter two, the place names database and country data guide will be created for each country and will be modified to reflect new types of reports as reports are modified or new reports are added. Each is described below.

## Report data files

Each csv file should represent data from a single report, whether that report has no tables, a single table, or multiple tables. Each line in the file should represent a numerical value from that report with relevant time, location, and data type information. The name of each csv file should have the same name as the 'short_name' for the report type followed by and underscore and the 'report_date' (described below), e.g. ***OUR EXAMPLE HERE.  Original:  e.g. 'COES_Microcephaly_2016-01-03.csv'***

Across all fields, do not use any white spaces (spaces or tabs) or commas. Use only ASCII characters (not ASCII extended).

Unless otherwise noted each of the following fields is required:

**report_date**: The report date is the date that the report was published. If this date is unavailable, use the last date that the data in the report was updated. If no date can be found, use the date on which the report was first accessed. The date should be specified in standard ISO format (YYYY-MM-DD). Note that the same date should be included in every row of the file. 

    report_date: 2016-01-30

**location**: A location should be specified for each observation following the specific names specified in the country place name database. This may be any place with a 'location_type' as listed below, e.g. city, state, country, etc. It should be specified at up to three hierarchical levels in the following format: [country]-[state/province]-[county/municipality/city], always beginning with the country name. If the data is for a particular city, e.g. Wuhan, it should be specified: China-Hubei-Wuhan. Each of these levels and the full name is provided in the place name database for use in preparing the files. For standardization purposes, the place name will not contain any accents or special characters. Proper names will be included in the place name database when possible. If the 'location' is not in the place name database, open an Issue to create a new 'location'.

    location: China-Hubei

**location_type**: A location code should also be included indicating: city, district, municipality, county, state, province, or country. If there is need for an additional 'location_type', open an Issue to create a new 'location_type'.

    location_type: state

**data_field**: The data field is a short description of what data is represented in the row and is related to a specific definition defined by the report from which it comes. The complete, specific definition for each 'data_field' within each country in the country data guide. It should be accompanied by a country-specific code (see 'data_field_code'). The same terminology may be used across countries, but this is not required as country-specific definitions are likely to vary. If the exact 'data_field' and 'data_field_code' do not exist in the country data guide, open an Issue to create a new 'data_field' and corresponding 'data_field_code'.

    data_field: ***OUR EXAMPLE HERE*** original: microcephaly_under_investigation

**data_field_code**: This code is defined in the country data guide. It includes a two letter country code (ISO-3166 alpha-2, [list](https://www.iso.org/obp/ui/#search/code)), followed by a 4-digit number corresponding to a specific report type and data type. If the exact 'data_field' and 'data_field_code' do not exist in the country-specific data dictionary, open an Issue to create a new 'data_field' and corresponding 'data_field_code'.

    data_field_code: CN0001

**time_period**: Optional. If the data pertains to a specific period of time, for example an epidemiological week, that number should be indicated here and the type of time period in the 'time_period_type', otherwise it should be NA.

    time_period: 3

**time_period_type**: Required only if 'time_period' is specified. Types will also be specified in the country data guide. Otherwise should be NA. If the exact 'time_period_type' is not specified in the country data guide, open an Issue to create a new 'time_period_type'.

    time_period_type: epidemic_week

**value**: The observation indicated for the specific 'report_date', 'location', 'data_field' and when appropriate, 'time_period'.

    value: 10

**unit**: The unit of measurement for the 'data_field'. This should conform to the 'data_field' unit options as described in the country-specific data guide. If the unit required does not exist in the specific 'data_field' entry, open an Issue to add that unit. Note this should not include modifiers such as "suspected", those should be include in the data_field full description (in the country data guide).

    unit: cases

*Data dictionary replicated from Michael Johansson's zika repository:* [![DOI](https://zenodo.org/badge/51947303.svg)](https://zenodo.org/badge/latestdoi/51947303) 
