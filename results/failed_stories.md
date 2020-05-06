## ask languages
* faq: what languages can I build assistants in?   <!-- predicted: faq: what languages can I build [assistants](use_case) in? -->
    - slot{"use_case": "assistants"}
    - respond_faq   <!-- predicted: action_default_ask_affirmation -->


## ask rasa X
* faq: what's Rasa X?   <!-- predicted: faq: what's [Rasa](company) X? -->
    - slot{"company": "Rasa"}
    - respond_faq


## greet + form + bye
* greet: Hi there
    - utter_greet   <!-- predicted: action_default_ask_affirmation -->
* contact_sales: I want to talk with the sales department
    - sales_form
    - form{"name": "sales_form"}
* faq: Tell me about rasa x
    - respond_faq
    - form{"name": null}
* thank: Thank you vey much
    - utter_noworries
* bye: Goodbye
    - utter_bye


