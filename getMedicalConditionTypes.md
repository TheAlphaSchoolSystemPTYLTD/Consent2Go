**getMedicalConditionTypes**
----
	Returns a structured array of medical condition types data in JSON format.
  
* **Version History:**

    Version | Description
    --- | --- |
    TASS v59.11 | New endpoint for Consent2Go integration.

* **Version:**

  3

* **Permission:**

  Medical Records > Medical Setup > Conditions > View

* **Method:**

  `GET | POST`
  
*  **Params:**

   **Required:**
 
   None

   **Optional:**

   None

   **Conditional:**

   None

* **Success Response:**

    ```javascript
    {
    "data": [
        {
            "MCUD4_DESC": "",
            "MCUD1_DESC": "Whick Leg ?",
            "MCUD8_DESC": "",
            "MCFORM_FLG": "N",
            "VALUE": "ASL",
            "DESC": "A Sore Leg",
            "MCUD3_DESC": "",
            "CODE": "ASL",
            "ISR_FLG": "",
            "MCUD6_DESC": "",
            "MCUD10_DESC": "",
            "MCOND_AFLG": "N",
            "MCUD9_DESC": "",
            "MCUD5_DESC": "",
            "LABEL": "A Sore Leg",
            "ACTIVE_FLG": "N",
            "MCUD2_DESC": "Above the Knee ?",
            "ISR_COMMENT": "",
            "MCUD7_DESC": "",
            "MCOND_PLFLG": "Y",
            "ISR_SORT": ""
        }
    ]
    ```
 
* **Sample GET:** (With URL Encoded `token`)

  ```HTML
    http://api.tasscloud.com.au/tassweb/api/?method=getMedicalConditionTypes&appcode=DEMO&company=10&v=3&token=l1D8owEn111IHcXLRwXTB0oU2GX6rj%2BISqa9zXA8We3J3mwgjW5pdUvFK3%2FIZ4mJ4bMyfKTmEoup%2B3tTE9GeLQ%3D%3D
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
       <input type="hidden" name="method" value="getMedicalConditionTypes">
       <input type="hidden" name="appcode" value="DEMO">
       <input type="hidden" name="company" value="10">
       <input type="hidden" name="v" value="3">
       <textarea name="token">l1D8owEn111IHcXLRwXTB0oU2GX6rj+ISqa9zXA8We3J3mwgjW5pdUvFK3/IZ4mJ4bMyfKTmEoup+3tTE9GeLQ==</textarea>
    </form>
  ```
