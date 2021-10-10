# learn-jenkins

## What is Jenkins ?

Jenkins is a self-contained, open source automation server which can be used to automate all sorts of tasks related to `building`, `testing`, and `delivering` or `deploying` software.

Jenkins can be installed through native `system packages`, `Docker`, or even run `standalone` by any machine with a Java Runtime Environment (JRE) installed.

Originally developed for continuous integration (CI), today Jenkins orchestrates the entire software delivery pipeline – Continuos Integration / Continuos Delivery (CI/CD).

## Q&A

<details>

  <summary> 1. How to download Jenkins for Docker ? </summary>

  <p>

There are many ways to install Jenkins. In this tutorial we are going to use Docker.

```console
// To use the latest LTS
docker pull jenkins/jenkins:lts-jdk11
// To use the latest weekly
docker pull jenkins/jenkins:jdk11
```

Docker hub official site - `https://hub.docker.com/r/jenkins/jenkins`

  </p>

</details>

---

<details>

  <summary> 2. How to setup a Jenkins using docker compose ? </summary>

  <p>

1. Run the docker compose file

```YAML
version: '3.4'
services:
  jenkins:
    image: jenkins/jenkins:lts-jdk11
    ports:
      - '8000:8080'
    volumes:
      - jenkins-data:/var/jenkins_home # using named volumes, so that we don't lose data on restart/next start
    networks:
      - jenkins
networks:
  jenkins:
volumes:
  jenkins-data:
```

2. Collect the password from the log

```TEXT
Jenkins initial setup is required. An admin user has been created and a password generated.
Please use the following password to proceed to installation:
c5d1d3cde1244d6f981774e73eb0c499
```

3. Complete the setup

Head to `http://localhost:8000/` and enter the password. And complete the setup by creating an user.

  </p>

</details>

---

<details>

  <summary> 3. How to get started with Jenkins freestyle project ? </summary>

  <p>

  </p>

</details>

---

<details>

  <summary> </summary>

  <p>

  </p>

</details>

---

<details>

  <summary> </summary>

  <p>

  </p>

</details>

---

<details>

  <summary> </summary>

  <p>

  </p>

</details>

---

<details>

  <summary> </summary>

  <p>

  </p>

</details>

---

<details>

  <summary> </summary>

  <p>

  </p>

</details>

---

<details>

  <summary> </summary>

  <p>

  </p>

</details>

---

### Resources

- [Jenkins Official docs](https://www.jenkins.io/doc/book/)

- [Jenkins - Udemy](https://www.udemy.com/course/jenkins-from-zero-to-hero/)

- [CI with Jenkins - Pluralsight](https://www.pluralsight.com/paths/continuous-integration-with-jenkins)
