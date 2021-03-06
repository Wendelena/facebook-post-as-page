# Post to Facebook as Page

This is a Python script to post to Facebook as Page.

1. First, create a Facebook application. Go to https://developers.facebook.com/apps/ and click on **Add a New App**.

2. After creating the application, go to its dashboard. You will see the **App ID** and **App Secret**. Do not give these values to anyone. You will use these two in the Python script.

3. Click on **Settings** > **Advanced** in the left menu and associate *App Page* with the Facebook Page that you own.

4. Create your *access token* by going to https://developers.facebook.com/docs/facebook-login/access-tokens/#pagetokens and creating a *Page Access Token*. You will use it in the Python script.

5. Copy the script `post_to_facebook.py` to a directory of your choice. Mine is copied to `/home/aruljohn/scripts/post_to_facebook.py`.

6. Edit `post_to_facebook.py` and replace the three values from above.

7. You will need to have the *facebook* and *requests* Python modules installed. Run these commands to install them.

```
pip install requests
pip install facebook-sdk
```

8. Run the script:

```
python /home/aruljohn/scripts/post_to_facebook.py`
```

9. To set a cronjob to run this script and tweet your Internet speed every 3 hours, you can use this line:

```
# Run every 3 hours
5 0-23/3 * * * /usr/bin/python /home/aruljohn/scripts/post_to_facebook.py >> /tmp/facebookpost.log
```
