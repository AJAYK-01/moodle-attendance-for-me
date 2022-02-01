## Note: This is a fork of https://github.com/aldrinjenson/moodle-automation

### Deploy to Heroku (dont forget to add cron job as mentioned in below steps)

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/AJAYK-01/moodle-attendance-for-me/tree/master)

# Moodle Attendance Automation

- nodeJs script to automate the attendance marking in Moodle and get updates in Telegram.
  Useful if you attend classes but forgets to mark attendance on Moodle for the subject every hour.

## Steps to Run

- Create a `.env` file similar to the example file in the root directory which contains your credentials
- Update the subjectLinks.js file with the names and urls for your course subjects
- Install dependencies using `npm install`
- run server using `npm start`
- Host the server on heroku or any other platform of your choice and set up a cron job using [cron-job.org](https://cron-job.org/) to ping the `<HEROKU_BASE_URL>/scrape` url every 30 minutes from morning till evening
- Get notified on Telegram for every succesfull marking or in case some error occurred.
