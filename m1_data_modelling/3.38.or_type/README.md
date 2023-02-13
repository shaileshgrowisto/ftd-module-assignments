Create a FTD file with the name `or-type.ftd`.

In this file, you have to create a or-type with name as lead having two records.
a. individual
b. company

This two records will work as optional record(s).
If the `individual` record is used, it will access it fields.

If the `company` record is used, it will access it fields.

1. start your `or-type` with a name as `lead`. This name will be use to create `or-type` instances

2. Inside `or-type` block, you have to create record with name as `individual` with 2 fields as:
   a. `caption` string data type with field name as `name`
   b. `string` data type with field name as `phone`

3. Add one more record inside the `or-type` with below fields:
   a. `caption` string data type with field name as `name`
   b. `string` data type with field name as `contact`
   c. `string` data type with field name as `fax`

Follow below code to define an `or-type` with `records`:

```
-- or-type lead:

-- record individual:
caption name:
string phone:

-- record company:
caption name:
string contact:
string fax:

-- end: lead

```

4. Follow below code to create instance of the `or-type` based on records fields

Follow below code to create instances:

```
-- lead.individual john: Johnny Bravo
phone: 7208689008

-- lead.company acme: Acme Inc.
contact: John Doe
fax: +1-234-567890

```

Note: Right now, FTD only supports `or-type` declaration and instances with assignments. The major use of `or-type` is with `match` statement which will be released soon in the newer version of FTD.
