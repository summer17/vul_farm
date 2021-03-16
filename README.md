# vul_farm
This is a run-time fuzz tool used to find vulnerabilities in open source web software. 
It can help researchers find many types of vulnerabilities, including SQL injection, XXE, SSRF, XSS, command execution, etc. It can detect java and php languages.

When researchers try to use Vulnerability_Farm to find security vulnerabilities in web software, the following steps will be required:

1.When testing software written in php language, Vulnerability_Farm provides a “.so”file to import into the php environment. When testing software written in java language, Vulnerability_Farm provides a “.jar” file to import into the java environment.

2. The researchers has normal access to the various interfaces of the web software, and Vulnerability_Farm will display the degree of path coverage.

3.Vulnerability_Farm will record url objects, url parameters, parameter transfer paths, and function call stacks

4. Vulnerability_Farm will construct fuzzing test data and detect sensitive function parameters

5. If a security vulnerability is detected, Vulnerability_Farm will display the test data and parameter transfer path.

Note:
When testing open source network software in php language, the researcher needs to enable pdo, pcre, and json functions in the php environment.
When testing open source web software in java language, the researcher needs to build a tomcat environment.

More:
There are already a large number of fuzz software for web software, such as sqlmap and so on. They found vulnerabilities by examining the page results after processing the crafted parameters. However, these fuzz software cannot detect vulnerabilities that are not echoed, nor can they show attack paths. 
Compared with these software, Vulnerability_Farm can increase the path coverage rate and reduce the false alarm rate through the runtime detection method, and it can find more complicated vulnerabilities.

