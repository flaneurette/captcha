
# Captcha

Very simple standalone Captcha that uses random vowels and consonants to create a human readable word and places it with a random color on a random location inside a checkerboard. 

Requirements: PHP GD Library.

![Image of Captcha](https://raw.githubusercontent.com/flaneurette/class.SecureMail/56c2a651f9bb6ef1b62d1def915772559ca4dbd8/captcha/example.png)

	echo "Prove to us you are not a robot.";
	echo '<img src="http://yourwebsite.tld/captcha/" width="190">';
	echo '<input type="text" name="captcha" value="">';
	
Then you need to read the $_SESSION['captcha_question'] , which was stored inside the image session.

Like so:

	if($_SESSION['captcha_question'] === $_POST['captcha']) {
		echo "Captcha was correct!";
	}
	
And then decide what to do next...

# Font

"Thankfully" by Creatype Studio 
https://creativemarket.com/creatype

(They said it's 100% free.)

Hint: Use another font, and make it even better.... the more randomness, the more annoyed robots.
