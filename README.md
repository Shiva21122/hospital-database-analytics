# Hospital Database Analytics

Full database-to-dashboard project: a hospital relational database designed in SQL, transformed into a star schema, and analyzed in Power BI.

## 1. Business Question

How efficiently is the hospital operating — appointment load by department, repeat visits, room utilization, billing status, common diagnoses, and top prescribed medicines — and where are the bottlenecks?

## 2. Research

- Designed a hospital OLTP schema (patients, doctors, staff, departments, appointments, prescriptions, medical records, billing) in SQL Server — `SQL/Hospital_Database_Script.sql`
- Transformed operational tables into an analytical star schema (Fact/Dim CSV extracts)

## 3. Data Types

Relational entities with keys (IDs), datetimes (appointments, records), categorical (department, diagnosis, room type, billing status), numeric aggregates (visit counts, stats).

## 4. Data Cleaning

- Referential integrity enforced at the database level (PK/FK design)
- SQL views/queries to derive Dim/Fact extracts: `DimCommonDiagnosis`, `DimDeptAppointmentStats`, `DimPatientBillingStatus`, `DimRepeatedVisits`, `DimRooms`, `DimTopPrescribedMedicines`, plus Fact tables for departments, doctors, staff, prescriptions, and medical records

## 5. Results

- Power BI dashboard: `Dashboards/Hospital_Dashboard.pbix` — department workload, repeat-visit patterns, billing status breakdown, top diagnoses and medicines
- Documentation: `Reports/Technical_Report_Hospital.pdf` and final presentation

## Project Structure

```
hospital-database-analytics/
├── SQL/Hospital_Database_Script.sql   # Full database DDL + queries
├── Data/                              # Star-schema Fact/Dim CSV extracts + source xlsx
├── Dashboards/Hospital_Dashboard.pbix
├── Reports/                           # Technical report + presentation
└── Archive/                           # Earlier dashboard versions
```

## How to Run

Run `SQL/Hospital_Database_Script.sql` in SQL Server Management Studio to build the database, or connect Power BI directly to the CSVs in `Data/`.

**Tools:** SQL Server (DDL, joins, aggregation), star-schema modeling, Power BI
