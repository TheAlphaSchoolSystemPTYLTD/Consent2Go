**getClassDetailsWithStudents**
----
	Returns an array of structured class data containing students in that class for current year and semester.
    
* **Version History:**

  TASS v59.10 - New endpoint for Consent2Go integration.
  
* **Version:**

  3

* **Permission:**

  Student Records > Class Lists > View

* **Method:**

  `GET | POST`
  
*  **Params:**

   **Required:**

   none
   
   **Optional:**

   none
 
   **Conditional:**
 
   none

* **Success Response:**

    ```javascript
      {
      "data": [
        {
          "class_desc": "English, DD, A",
          "sub_code": "0001",
          "year_grp_desc": "DD",
          "year_grp": -5,
          "semester": 2,
          "sub_long": "English",
          "class": "A",
          "year_study": 2023,
          "teachers": [],
          "sub_desc": "English",
          "students": [
            {
              "stud_code": "0009479"
            }
          ]
        }
      ],
      "__tassversion": "01.057.11.000",
      "token": {
        "timestamp":"{ts '2022-09-28 11:44:31'}"
      }
    }
    ```
 
* **Error Response:**

    none

* **Sample GET:** (With URL Encoded `token`)

  ```HTML
    http://api.tasscloud.com.au/tassweb/api/?method=getClassDetailsWithStudents&appcode=DEMO&company=10&v=3&token=l1D8owEn111IHcXLRwXTB0oU2GX6rj%2BISqa9zXA8We3J3mwgjW5pdUvFK3%2FIZ4mJ4bMyfKTmEoup%2B3tTE9GeLQ%3D%3D
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
       <input type="hidden" name="method" value="getClassDetailsWithStudents">
       <input type="hidden" name="appcode" value="DEMO">
       <input type="hidden" name="company" value="10">
       <input type="hidden" name="v" value="3">
       <textarea name="token">l1D8owEn111IHcXLRwXTB0oU2GX6rj+ISqa9zXA8We3J3mwgjW5pdUvFK3/IZ4mJ4bMyfKTmEoup+3tTE9GeLQ==</textarea>
    </form>
  ```
