# ErrorList
Returns a list of error codes and text that the API may return.

* __Path:__ ``/eve/ErrorList.xml.aspx``
* __Cache timer:__ 1 hour
* __Access mask:__ none
* __Parameters:__ none

### Sample Response

```xml
<result>
    <rowset name="errors" key="errorCode" columns="errorCode,errorText">
        <row errorCode="100" errorText="Expected before ref/trans ID = 0: wallet not previously loaded."/>
        <row errorCode="101" errorText="Wallet exhausted: retry after {0}."/>
        <row errorCode="102" errorText="Expected before ref/trans ID [{0}] but supplied [{1}]: wallet previously loaded."/>
        <row errorCode="103" errorText="Already returned one week of data: retry after {0}."/>
        <row errorCode="105" errorText="Invalid characterID."/>
        <row errorCode="106" errorText="Must provide userID or keyID parameter for authentication."/>
        <row errorCode="107" errorText="Invalid beforeRefID provided."/>
        <row errorCode="108" errorText="Invalid accountKey provided."/>
        <row errorCode="109" errorText="Invalid accountKey: must be in the range 1000 to 1006 for EVE wallets or 10000 for the DUST wallet."/>
        <row errorCode="110" errorText="Invalid beforeTransID provided."/>
        <row errorCode="111" errorText="'{0}' is not a valid integer."/>
        <row errorCode="112" errorText="Version mismatch."/>
        <row errorCode="113" errorText="Version escalation is not allowed at this time."/>
        <row errorCode="114" errorText="Invalid itemID provided."/>
        <row errorCode="115" errorText="Assets already downloaded: retry after {0}."/>
        <row errorCode="116" errorText="Industry jobs already downloaded: retry after {0}."/>
        <row errorCode="117" errorText="Market orders already downloaded: retry after {0}."/>
    </rowset>
</result>
```

### Result Data

<table border="1">
    <tbody>
        <tr>
            <th>Name</th>
            <th>Data type</th>
            <th>Description</th>
        </tr>
        <tr>
            <td>errorCode</td>
            <td>int</td>
            <td>The ID of the error code.</td>
        </tr>
        <tr>
            <td>errorText</td>
            <td>string</td>
            <td>Textual description of the error.</td>
        </tr>
    </tbody>
</table>

### Error Code Types

* 1xx - User Input
* 2xx - Authentication
* 5xx - Server
* 9xx - Miscellaneous
