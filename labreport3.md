# Lab Report 3
## Researching Commands: `grep`
### 4 Interesting Ways to Use `grep`
**1. `grep -c`**

The `-c` (count) option for `grep` shows how many lines in a file match the specified pattern.
```
$ grep -c "terminal" technical/911report/chapter-1.txt
5
```
In this example, `grep` searches chapter-1.txt for lines containing "terminal". The output is 5, meaning there are 5 lines that contain "terminal" in that file.
```
$ grep -c "weight" technical/biomed/1468-6708-3-1.txt
54
```
In this example, `grep` searches each line in 1468-6708-3-1.txt and sees if the line contains "weight". The output means that there are 54 lines containing the word "weight" in the file.


**2. `grep -n`**

The `-n` modifier prints the line number and corresponding line that matches the specified pattern.
```
$ grep -n "terminal" technical/911report/chapter-1.txt
18:    Atta and Omari arrived in Boston at 6:45. Seven minutes later, Atta apparently took a call from Marwan al Shehhi, a longtime colleague who was at another terminal at Logan Airport. They spoke for three minutes.
24:    In another Logan terminal, Shehhi, joined by Fayez Banihammad, Mohand al Shehri, Ahmed al Ghamdi, and Hamza al Ghamdi, checked in for United Airlines Flight 175, also bound for Los Angeles. A couple of Shehhi's colleagues were obviously unused to travel; according to the United ticket agent, they had trouble understanding the standard security questions, and she had to go over them slowly until they gave the routine, reassuring answers.
28:    The security checkpoints through which passengers, including Atta and his colleagues, gained access to the American 11 gate were operated by Globe Security under a contract with American Airlines. In a different terminal, the single checkpoint through which passengers for United 175 passed was controlled by United Airlines, which had contracted with Huntleigh USA to perform the screening.
340:    While the Command Center was told about this "other aircraft" at 9:01, New York Center contacted New York terminal approach control and asked for help in locating United 175.
406:    The Command Center kept looking for American 77. At 9:21, it advised the Dulles terminal control facility, and Dulles urged its controllers to look for primary targets. At 9:32, they found one. Several of the Dulles controllers "observed a primary radar target tracking eastbound at a high rate of speed" and notified Reagan National Airport. FAA personnel at both Reagan National and Dulles airports notified the Secret Service. The aircraft's identity or type was unknown.
```
In the first example, `grep` counted 5 lines in chapter-1.txt that contained the word "terminal". Using the same example but with `-n`, we can see that the output now prints each line number followed by the line contents. This matches the first example as we can see that there are indeed 5 lines printed.
```
$ grep -n "alcohol problem" technical/government/Alcohol_Problems/Session2-PDF.txt
29:certainly be considered an "alcohol problem." The blood or breath
98:would address both current and lifetime alcohol problems. Current
141:diagnosis, but clinical impressions concerning alcohol problems can
145:patients with alcohol problems. Unfortunately, the majority of
155:a sensitivity of 29% for alcohol problems in the ED.7
271:indicate an alcohol problem. While a very high BAC in an unimpaired
377:rates. EDs have reported high case rates of alcohol problems,
450:7. Cherpitel C. Screening for alcohol problems in the emergency
459:alcohol problems in the emergency department, part 1: improving
547:instruments for alcohol problems in the emergency room. J Stud
```
Here `grep` searched through Session2-PDF.txt for lines containing the pattern "alcohol problem", and printed the line numbers and lines that matched.

**3. `grep -v`**

Somewhat like the opposite of the traditional `grep` function, the `-v` option finds lines in a file that *do not* match the specified pattern.
```
$ grep -v "e" technical/911report/preface.txt



            PREFACE
                27, 2002).
                accountability.


```
Here, `grep` found and printed all of the lines that did not contain "e". Since `grep` in this form is case-sensitive, "PREFACE" is still printed because it contains an upper-case E. It also prints all of the blank lines since they do not contain "e".
```
$ grep -v " " technical/government/Post_Rate_Comm/WolakSpeech_usps.txt





increase

1996


trends?
consumption.
sector
communication
services


demand?


Services
expenditures.
residence.
sampled
these

1994
1994
percent


attributes
household.
i
substitution.
household-level

function


i
demand.
household's


function.

-1.27.
household-level
services.
services,


Estimates
increases.
increase.
constant.
0.25.


Caveats
trends
http://www-leland.stanford.edu/~wolak





```
For this output, `grep -v` found all of the lines that did not include " " (space).

**4. `grep -A`**
The `-A` modifier is used to display a certain number of lines that follow a matched line.
```
$ grep -A 3 "Draft Recommendations" technical/government/Alcohol_Problems/DraftRecom-PDF.txt
Draft Recommendations

Daniel Hungerford opened the final session of the conference by
outlining the group's ultimate task-to create research
```
In this example, `grep` prints the matched line containing "Draft Recommendations", and the next 3 lines in the file after that matched line.
```
$ grep -A 1 "DECLARATION OF WAR" technical/911report/chapter-2.txt
            A DECLARATION OF WAR
            In February 1998, the 40-year-old Saudi exile Usama Bin Ladin and a fugitive Egyptian
```
For this output, `grep` found one line containing the specific pattern and printed the next line that follows in the file.

## Sources
All commands were found through this link: www.cyberciti.biz/faq/howto-use-grep-command-in-linux-unix/
