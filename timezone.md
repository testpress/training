# Time & Timezone

We need an application which will show the current time on the page and also the city to which the time belongs.

The default city can be taken from settings.py TIME_ZONE

## Models
There should be no models for this project. No database.

## Design mockup
![timezone](https://user-images.githubusercontent.com/328112/211003080-e0761252-adba-480b-928f-ef907572b7ef.png)

## Change city
There should be an option to change the city in the following url

```python
http://127.0.0.1:8000/cities/change/
```

On visiting the above URL, there should be a dropdown with the list of all cities (Area/Location) and timezone as a dropdown.

We should be able to change the city from that dropdown.


Once the city is changed and we submit the form, it should redirect to the homepage.

The city and time should be changed to the city we selected in the above dropdown.

After closing the browser and opening the URL again, the landing page should retain the newly selected city from the previous step.

If i clear the cookies from the browser, then the landing page should show the default city from settings.py TIME_ZONE

## Hint
- The changed city should be stored in the session.
- You should use middleware to change the timezone on every request
