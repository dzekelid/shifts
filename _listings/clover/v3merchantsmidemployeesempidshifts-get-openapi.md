---
swagger: "2.0"
x-collection-name: Clover
x-complete: 0
info:
  title: Clover Get all shifts for an employee
  version: 1.0.0
  description: Get all shifts for an employee.
host: /merchants
basePath: https://api.clover.com
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/merchants/{mId}/shifts:
    get:
      summary: Get all shifts
      description: Get all shifts.
      operationId: GetAllShifts
      x-api-path-slug: v3merchantsmidshifts-get
      parameters:
      - in: query
        name: expand
        description: 'Expandable fields: [employee, overrideInEmployee, overrideOutEmployee]'
      - in: query
        name: filter
        description: 'Filter fields: [id, employee'
      - in: path
        name: mId
        description: Merchant Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Shifts
  /v3/merchants/{mId}/shifts/{shiftId}:
    get:
      summary: Get a single shift
      description: Get a single shift.
      operationId: GetShift
      x-api-path-slug: v3merchantsmidshiftsshiftid-get
      parameters:
      - in: query
        name: expand
        description: 'Expandable fields: [employee, overrideInEmployee, overrideOutEmployee]'
      - in: path
        name: mId
        description: Merchant Id
      - in: path
        name: shiftId
        description: Employee Shift Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Shifts
      - ShiftId
  /v3/merchants/{mId}/shifts.csv:
    get:
      summary: Get .csv of all shifts
      description: Get .csv of all shifts.
      operationId: GetAllShiftsCSV
      x-api-path-slug: v3merchantsmidshifts-csv-get
      parameters:
      - in: query
        name: filter
        description: 'Filter fields: [id, employee'
      - in: path
        name: mId
        description: Merchant Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Shifts
      - Csv
  /v3/merchants/{mId}/employees/{empId}/shifts:
    get:
      summary: Get all shifts for an employee
      description: Get all shifts for an employee.
      operationId: GetEmployeeShifts
      x-api-path-slug: v3merchantsmidemployeesempidshifts-get
      parameters:
      - in: path
        name: empId
        description: Employee Id
      - in: query
        name: expand
        description: 'Expandable fields: [employee, overrideInEmployee, overrideOutEmployee]'
      - in: query
        name: filter
        description: 'Filter fields: [id, employee'
      - in: path
        name: mId
        description: Merchant Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Employees
      - EmpId
      - Shifts
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---