## greet + goodbye
* greet: Hi!
  - utter_greet
* bye: Bye
  - utter_bye

## greet + thanks
* greet: Hello there
  - utter_greet
* thank: thanks a bunch
  - utter_noworries

## greet + thanks + goodbye
* greet: Hey
  - utter_greet
* thank: thank you
  - utter_noworries
* bye: bye bye
  - utter_bye

## ask channels
* faq: what messaging channels does rasa support?
 - respond_faq

## ask languages
* faq: what languages can I build assistants in?
 - respond_faq

## ask rasa X
* faq: what's Rasa X?
 - respond_faq

## greet + form + bye
* greet: Hi there
 - utter_greet
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
