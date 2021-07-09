Instructions: https://sendgrid.com/blog/sending-emails-from-python-flask-applications-with-twilio-sendgrid/

Error with module python-dotenv
In order to fix I had to deactivate, then reactive and run:
pip3 install python dot-env
then run flask shell once more..
from app import mail
from flask_mail import Message

# add variables and expressions for the markup and recipient and voila
msg = Message('Twilio SendGrid Test Email', recipients=['recipient@example.com'])
msg.body = 'This is a test email!'
msg.html = '<p>This is a test email!</p>'

# final command
mail.send(msg)

Success!
