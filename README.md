Ti.LinkedIn
===========

This is a module for getting some infos from LinkedInportal. With it you can also share to profile.
Oauth2.0 is included. You need appId and appSecret. Both must be added to tiapp.xml as String property

Thanks to @andreav ![](https://avatars.slack-edge.com/2015-07-04/7233019188_622d59713626a983b56b_72.jpg) for help.
If you need some extends, please free and contact me ![](https://avatars.slack-edge.com/2016-06-02/47624811367_cad17b312a9a5aa65338_72.jpg).

If the sponsor paid  the support I will open the sources.

Similar module is [Ti.SignInWith](https://github.com/AppWerft/Ti.SignInWith). With t his module you have a generic adapter for login to identity providers.

Usage
-----

It is a very simple API:

~~~

var LinkedIn = require('de.appwerft.linkedin');
LinkedIn.getProfile('me', function(_e) {
    alert(_e.data);
});
~~~

You will get a result like this: 


![](https://raw.githubusercontent.com/AppWerft/Ti.LinkedIn/master/documentation/res.png)

More getter are: getPositionById(), getCompanyById, postShare(), getProfileWithContacts();

For all request you need scopes (see documentation). As allowed redirect_uri you must add  'https://upload.wikimedia.org/wikipedia/en/b/b1/Portrait_placeholder.png'. This is dirty workeround, because LinkedIn doesn't support oob.

These are entry in you tiapp.xml:

~~~
<property name="linkedin_id" type="string">7798****xfs</property>
<property name="linkedin_secret" type="string">wqApS***54G8Ky</property>

/* optional*/
<property name="linkedin_redirecturl" type="string">https://upload.wikimedia.org/wikipedia/en/b/b1/Portrait_placeholder.png</property>

~~~

You need these entries:

![](https://raw.githubusercontent.com/AppWerft/Ti.LinkedIn/master/documentation/screen.png)