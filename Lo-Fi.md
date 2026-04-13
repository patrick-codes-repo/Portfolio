# Scenario
This is a beginner friendly directory traversal exercise. The goal is find the flag stored in the root directory of the application’s host machine.

# Tools Used
N/A

# Execution
1. Visit the target web application.

![Home Page](https://github.com/patrick-codes-repo/Portfolio/blob/main/Resources/Lo-Fi/home_page.png?raw=true)

3. Nothing stands out immediately so I will explore the different pages of the application.

![Page](https://github.com/patrick-codes-repo/Portfolio/blob/main/Resources/Lo-Fi/page.png?raw=true)

After visiting one of the links under “Discography” the page parameter appears in the URL. It may be possible to exploit this.

3. Test the parameter by searching for a known file, /etc/passwd.

![Absolute Path](https://github.com/patrick-codes-repo/Portfolio/blob/main/Resources/Lo-Fi/absolute_path.png?raw=true)

4. That did not work. Now to try with with a relative file path, ../../../etc/passwd.

![Passwd](https://github.com/patrick-codes-repo/Portfolio/blob/main/Resources/Lo-Fi/passwd.png?raw=true)

5. The relative file path worked. Now I’ll try to grab the flag in the root directory, ../../../flag.txt.

![Flag](https://github.com/patrick-codes-repo/Portfolio/blob/main/Resources/Lo-Fi/flag.png?raw=true)

I found the flag!

# Lessons learned
1. Start directory traversals attempts using relative paths to save time. Applications are likely to route / to the root directory of the application instead of the root directory of the host.
