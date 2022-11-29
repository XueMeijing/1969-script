<h1 align=center> 1969 </h1>

<p align=center> Make your GitHub history back to 1969.(1970 actually, but in boorgarland it shows as 1969 because of the time difference) </p>

![image](https://user-images.githubusercontent.com/31113245/204480442-2f858f25-9683-4c7c-8a4a-d82d0843f867.png)

## Travel Back

Run the following script and follow the prompts
$```bash
sh -c "$(curl -fsSL https://raw.github.com/PickleNik/1969-script/master/index.sh)"
```
**Step 0:** [Create a new repo](https://github.com/new) on GitHub.

**Step 1:** Select your preferred authentication method

<img width="428" alt="Screenshot 2022-11-29 at 3 43 58 AM" src="https://user-images.githubusercontent.com/31113245/204481168-ff9ebed7-027f-4b7f-9d43-ae04c9246e00.png">

if you have SSH already setup locally, all you need is to copy your repo link and you're done :-)

<img width="420" alt="Screenshot 2022-11-29 at 3 49 15 AM" src="https://user-images.githubusercontent.com/31113245/204482278-85d1b161-9fd6-4849-8329-57a6e905884d.png">

Otherwise, if you chose HTTPS, you will need to [Generate a personal access token](https://github.com/settings/tokens/new) on GitHub and copypaste it.

Then enter you GitHub username and name of your new repository and you are done :)






## Explanations

This project works on the way `git` records commit. Whenever you commit something, `git` puts an `Unix Timestamp` on it to record when you committed it. An [`Unix Timestamp`](https://www.unixtimestamp.com/) is the way computers store the current time. An `Unix timestamp` is a `32-bit` number which stores the number of seconds that has passed from January 1st, 1970 at UTC, the `Unix Epoch`.

The script firstly creates a directory with the name of the wanted year - `mkdir $YEAR`

The script then initializes the directory as a git repository, using - `git init`

The script then stages all the files `git add .` and commits it, using the date `{YEAR}-01-01T00:00:00` or `12am, 1st January, 1970` (default of the `YEAR` variable)

This is the `ISO Date-Time format` for storing time: `YYYY-MM-DDTHH:MM:SS`.

This commit is then pushed to GitHub (provided you already have made a repository) using `git push -u origin main -f`, and the directory is removed.

GitHub recognizes the commit to have been created at `12am, 1st January, 1970` and thus registers a contribution at that moment in time. If you scroll to the first year on your profile, you will see there is a single contribution to your `1990` repository, on 1st January.
