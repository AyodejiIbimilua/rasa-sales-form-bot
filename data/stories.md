## thank
* thank
  - utter_noworries

## goodbye
* bye
  - utter_bye

## some questions to FAQ
* faq
  - respond_faq

## greet + sales form
* contact_sales
  - sales_form
  - form{"name": "sales_form"}
  - form{"name": null}

## just sales, continue
* contact_sales
    - sales_form
    - form{"name": "sales_form"}
* faq
    - respond_faq
    - sales_form
    - form{"name": null}

## explain email
* contact_sales
    - sales_form
    - form{"name": "sales_form"}
    - slot{"requested_slot": "business_email"}
* explain
    - utter_explain_why_email
    - sales_form
    - form{"name": null}

## explain budget
* contact_sales
    - sales_form
    - form{"name": "sales_form"}
    - slot{"requested_slot": "budget"}
* explain
    - utter_explain_why_budget
    - sales_form
    - form{"name": null}

## sales form
* contact_sales
    - sales_form                   
    - form{"name": "sales_form"} 
    - form{"name": null}

## out of scope
* out_of_scope
    - utter_out_of_scope
* out_of_scope
    - utter_out_of_scope

## interactive_story_1
* contact_sales
    - sales_form
    - form{"name": "sales_form"}
    - slot{"requested_slot": "budget"}
* form: inform
    - form: sales_form
    - slot{"budget": "400K"}
    - slot{"requested_slot": "use_case"}
* form: inform{"use_case": "news bot"}
    - slot{"use_case": "news bot"}
    - form: sales_form
    - slot{"use_case": "news bot"}
    - slot{"requested_slot": "job_function"}
* form: inform{"job_function": "marketer"}
    - slot{"job_function": "marketer"}
    - form: sales_form
    - slot{"job_function": "marketer"}
    - slot{"requested_slot": "person_name"}
* form: inform{"person_name": "Makinde Pelumi"}
    - slot{"person_name": "Makinde Pelumi"}
    - form: sales_form
    - slot{"person_name": "Makinde Pelumi"}
    - slot{"requested_slot": "business_email"}
* form: inform{"business_email": "okanlawon@yahoo.com"}
    - slot{"business_email": "okanlawon@yahoo.com"}
    - form: sales_form
    - slot{"business_email": "okanlawon@yahoo.com"}
    - slot{"requested_slot": "company"}
* form: inform{"company": "the vanguard"}
    - slot{"company": "the vanguard"}
    - form: sales_form
    - slot{"company": "the vanguard"}
    - form{"name": null}
    - slot{"requested_slot": null}
* thank
    - utter_noworries
