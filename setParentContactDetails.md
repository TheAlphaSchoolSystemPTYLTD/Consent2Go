**setParentContactDetails**
----
	Returns "success" or error message for failed update.
  
* **Version History:**

    Version | Description
    --- | --- |
    TASS v59.10 | New endpoint for Consent2Go integration.

* **Version:**

  3

* **Permission:**

  Parent Accounts > Edit

* **Method:**

  `GET | POST`
  
*  **Params:**

   **Required:**
 
   `par_code [string]` - parent code.
 
   `add_num [string]` - address number.

   **Optional:**
 
   `e_mail1 [string]` - email for person 1.

   `e_mail2 [string]` - email for person 2.
   
   `home_phone [string]` - home phone number.
   
   `bus_phone [string]` - business phone number.
   
   `mobile_phone1 [string]` - mobile phone number for person 1.
   
   `mobile_phone2 [string]` - mobile phone number for person 2.

   **Conditional:**

   None

* **Success Response:**

    ```javascript
    {
      "success":"You successfully saved parent contact details.",
      "__tassversion":"01.054.4.000",
      "token":{
        "par_code": "0009130",
        "add_num": "1",
        "e_mail1": "xyz1@test.com",
        "e_mail2": "xyz2@test.com",
        "home_phone": "5555 5555",
        "bus_phone": "5555 5555",
        "mobile_phone1": "0499 999 999",
        "mobile_phone2": "0499 999 999",
        "timestamp":"{ts '2022-06-27 12:14:04'}"
      }
    }
    ```

* **Error Response:**

  `par_code` not supplied
  ```javascript
  __invalid: {
    "__msg": "par_code' IS REQUIRED."
  }
  ```

  `add_num` not supplied
  ```javascript
  __invalid: {
    "__msg": "add_num' IS REQUIRED."
  }
  ```
    
* **Sample Parameters:**

  ```javascript
  {
    "par_code": "000004  ",
    "add_num": "1",
    "e_mail1": "xyz1@test.com",
    "e_mail2": "xyz2@test.com",
    "home_phone": "5555 5555",
    "bus_phone": "5555 5555",
    "mobile_phone1": "0499 999 999",
    "mobile_phone2": "0499 999 999",
  }
  ```

* **Sample GET:** (With URL Encoded `token`)

  ```HTML
    http://api.tasscloud.com.au/tassweb/api/?method=setParentContactDetails&appcode=DEMO&company=10&v=3&token=l1D8owEn111IHcXLRwXTB0oU2GX6rj%2BISqa9zXA8We3J3mwgjW5pdUvFK3%2FIZ4mJ4bMyfKTmEoup%2B3tTE9GeLQ%3D%3D
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
       <input type="hidden" name="method" value="setParentContactDetails">
       <input type="hidden" name="appcode" value="DEMO">
       <input type="hidden" name="company" value="10">
       <input type="hidden" name="v" value="3">
       <textarea name="token">l1D8owEn111IHcXLRwXTB0oU2GX6rj+ISqa9zXA8We3J3mwgjW5pdUvFK3/IZ4mJ4bMyfKTmEoup+3tTE9GeLQ==</textarea>
    </form>
  ```
