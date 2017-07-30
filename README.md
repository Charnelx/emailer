# EMailer
Small lib for sending HTML email's with embeded (not attached!) images.

## Small example

### Preparation step
Suppose you have folder named "content" wich contains html file and two images you want to use in in this file.
In html file you should encase <img> tag with special tag <REPLACE_IMG></REPLACE_IMG>:

```html
<a href="http://example.com" target="_blank">
    <REPLACE_IMG><img src="image1.png" width="300" height="200" border="0"></REPLACE_IMG>
</a>
```

### Python script

```python
# initialize Emailer class with your account credentials
e = Emailer('example@gmail.com', 'qwerty123')
# send mail with 'subject' to the list of recipients using content in "content" folder
e.send_email('Read my message', 'path_to_folder_named_content', [bob@gmail.com, jade@gmail.com])
```

### Requirements
Python > 3.0
