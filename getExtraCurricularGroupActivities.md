**getExtraCurricularGroupActivities**
----
	Returns an array of structured extra curricular group activity data for current year and semester.
    
* **Version History:**

  TASS v59.11 - New endpoint for Consent2Go integration.
  
* **Version:**

  3

* **Permission:**

  Extra Curricular > Activity Groups > View

* **Method:**

  `GET | POST`
  
*  **Params:**

   **Required:**

   none
   
   **Optional:**

   `include_students [boolean]` - Include students in activity, default = false

   `include_staff [boolean]` - Include staff allocated to activity, default = false
 
   **Conditional:**
 
   none

* **Success Response:**

    ```javascript
      {
      "data": [
        {
          "act_code": "CHO",
          "act_desc": "Choir",
          "act_level": "01",
          "act_sem": 2,
          "act_year": 2023,
          "ecgroup_desc": "Choir",
          "ecgroup_id": "5592E242-B90C-C616-6C7C808BA48240CB",
          "lev_desc": "'A' Grade",
          "med_ack_flg": "N",
          "signupstart_date": "2023-11-06 00:00:00.0",
          "signupend_date": "2023-11-10 00:00:00.0",
          "type_code": "F",
          "type_desc": "Music"
          "students": [
            {
              "year_grp_desc": 11,
              "year_grp": 11,
              "stud_code": "0009518"
            }
          ],
          "staff": [
            {
              "emp_code": 1000016
            }
          ]
        }
      ],
      "__tassversion": "01.057.11.000",
      "token": {
        "include_students": true,
        "include_staff": true,
        "timestamp":"{ts '2022-09-28 11:44:31'}"
      }
    }
    ```
 
* **Error Response:**

    none
    
* **Sample Parameters:**

  ```javascript
  { 
    "include_students": true,
    "include_staff": true
  }
  ```

* **Sample GET:** (With URL Encoded `token`)

  ```HTML
    http://api.tasscloud.com.au/tassweb/api/?method=getExtraCurricularGroupActivities&appcode=DEMO&company=10&v=3&token=l1D8owEn111IHcXLRwXTB0oU2GX6rj%2BISqa9zXA8We3J3mwgjW5pdUvFK3%2FIZ4mJ4bMyfKTmEoup%2B3tTE9GeLQ%3D%3D
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
       <input type="hidden" name="method" value="getExtraCurricularGroupActivities">
       <input type="hidden" name="appcode" value="DEMO">
       <input type="hidden" name="company" value="10">
       <input type="hidden" name="v" value="3">
       <textarea name="token">l1D8owEn111IHcXLRwXTB0oU2GX6rj+ISqa9zXA8We3J3mwgjW5pdUvFK3/IZ4mJ4bMyfKTmEoup+3tTE9GeLQ==</textarea>
    </form>
  ```
