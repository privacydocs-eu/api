# API
[PrivacyDocs](https://privacydocs.eu) API usage examples.

# Fetch Current View

The current data shown in the Web front-end can be accessed with the following JavaScript or NodeJS request:

```
    const response = await fetch(`httsp://app.privacydocs.eu/api/view`, {
        method: 'GET',
        headers: {
            'Content-Type': 'text/html; charset=utf-8',
            'PDAuthorization': 'Bearer ' + key
        }
    })
```

The returned JSON will contain the data.

# Fetch Report

[PrivacyDocs report](https://privacydocs.eu/en/docs.html#accordion_reports) or [policy documents](https://privacydocs.eu/en/generate_policy_documents.html) can be generated with the following JavaScript or NodeJS request:

```
    const response = await fetch(`httsp://app.privacydocs.eu/api/report?template=${template}&table_ref=${table_ref}&row_ref=${row_ref}`, {
        method: 'GET',
        headers: {
            'Content-Type': 'text/html; charset=utf-8',
            'PDAuthorization': 'Bearer ' + key
        }
    })
```

Here `template` may take values `policy` or `row`; `table_ref` is 1 for the main records of processing activities (controller) table, `row_ref` is the internal identifier for the row in the table.

