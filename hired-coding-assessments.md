# Hired Coding Assessments

Recently I stumbled on to Hired.com, and it was fairly straightforward to sign up so I figured why not? They offer various coding/skills assessments, of which I took 4  (general coding, debugging, devops, backend). Of those 4, the first 2 I found very straightforward/easy, while the other 2 were harder. Interestingly though they weren't harder because the coding questions were harder, those 2 assessments contained multiple choice questions, some of which I had no idea on. I took the devops assessment 3 times, and the backend twice, but I don't remember exactly which questions were from which assessments as the topics definitely overlapped.

## General Areas I Didn't Know

- Docker (or related technologies)
- DNS specifics
- Pros/Cons of various architectures (server less, micro services etc.)
- Specific software used for various devops type purposes (AWS CloudFormation, Azure Resource Manager, Terraform)

## Questions I Didn't Know (at all)

- mean of HTTP status code 503
  - service unavailable
- syntax to delete a SQL table
  - DROP TABLE table-name;
- syntax for SQL pattern matching (i.e. match all `gmail.com` email addresses)
  - ??
- check installed version of package using apt
  - `apt-list <package-name>`

## Questions I knew but wasn't confident

- default ssh port
  - 22
- default directory for Linux log files
  - `/var/log`
- bash for loop over the elements of an array
  - for f in $files

## Python syntax needed to look up during code questions

- how to get ascii value from character
  - `ord()`
- how to initialize a list of 0s of a specific length
  - list_var = [0] * 26
- whether or not python had the equivalent of Integer.MAX_VALUE
  - python 2: `sys.maxint`
  - python 3: `sys.maxsize` : max value representable by a signed word (also size of largest list or in-memory sequence)
    - realistically I ended up using: `float('inf')`
    - looking back, I could have actually used the length of the list as the max number I was looking for
