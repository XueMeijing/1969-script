<h1 align=center> 1969 </h1>

<p align=center> Make your GitHub history back to 1969. <br /> (1970 actually, but in boorgarland it shows as 1969 because of the time difference) </p>

![image](https://user-images.githubusercontent.com/31113245/204480442-2f858f25-9683-4c7c-8a4a-d82d0843f867.png)

## Travel Back

Copy index.sh content to your local, and run the shell (Time zone related, current is Beijing Time)

```
sh index.sh
```

**Step 0:** [Create a new repo](https://github.com/new) on GitHub.

**Step 1:** Select your preferred authentication method

<img width="428" alt="Screenshot 2022-11-29 at 3 43 58 AM" src="https://user-images.githubusercontent.com/31113245/204481168-ff9ebed7-027f-4b7f-9d43-ae04c9246e00.png">

if you have SSH already setup locally, all you need is to copy your repo link and you're done :-)

<img width="420" alt="Screenshot 2022-11-29 at 3 49 15 AM" src="https://user-images.githubusercontent.com/31113245/204482278-85d1b161-9fd6-4849-8329-57a6e905884d.png">

Otherwise, if you chose HTTPS, you will need to [Generate a personal access token](https://github.com/settings/tokens/new) on GitHub and copypaste it.

Then enter you GitHub username and name of your new repository and you are done :)

## Q&A:

**1. Error occured: badDateOverflow: invalid author/committer line - date causes integer overflow**
  - Make sure your time exceeds Unix time 1970-01-01T00:00:00Z
  - Change index.sh content GIT_AUTHOR_DATE and GIT_COMMITTER_DATE to your local zone, for example Beijing time zone is +0800, so GIT_AUTHOR_DATE is "${YEAR}-01-01T08:00:00"

**2. Commit succeeded but gitHub history didn't change**
  - Your local Git commit email isn't connected to your github account, you must add the email address to your account on GitHub.
  - Commit was made less than 24 hours ago
  - More infomation here  [Common reasons that contributions are not counted](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-profile/managing-contribution-settings-on-your-profile/why-are-my-contributions-not-showing-up-on-my-profile)

**3. GitHub history changed but display unexpected when scroll**
  - Select Activity overview mode then it will display smoothly when scroll ![image](https://user-images.githubusercontent.com/35559153/230754120-e5687f95-b3f7-48ca-aa2b-94601e2dac31.png)