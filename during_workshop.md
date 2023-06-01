# During the Workshop

Before starting make sure you have addressed the prerequisites in the [README.md](README.md)

## Part 1 OAuth

This part of the workshop is in covered in [Part 1](./part_1.md).

## Part 2 Threat Modelling

In the second part of today's workshop you will be conducting a security review of an organisation's IT systems. [The details of this system can be found here](./Scenarios/Alpha_Organisation/description.md). Threat modelling can be an open ended process, so your trainers will probably time box each section of the exercise.

### Identify Threats

The first thing we need to do is to try to identify the possible threats the system could face. This is not an easy task: there are lots of possible attack vectors and many different sorts of threats.

Use the **STRIDE** topics as guidance and work your way through the systems methodically, perhaps system by system. At the end of this process you should have a list of potential threats grouped by topic and system. (You will probably find it helpful to record these in a spreadsheet - feel free to use your own, or [this example](https://docs.google.com/spreadsheets/d/1BWj_jrJ2HiHTRaoW6_pPVgN1W0zAnvOM0v7WUYG9lw8/edit?usp=sharing).)

#### STRIDE

A reminder from the reading material.

- **Spoofing** - impersonating another user or application
- **Tampering** - modifying input to execute an attack (e.g. the injection attacks from previous chapters)
- **Repudiation** - performing an action that cannot definitively be traced to the attacker
- **Information disclosure** - leak of sensitive data, a data breach
- **Denial of service** - rendering the application unavailable
- **Elevation of privilege** - gaining access to resources that would otherwise be protected

### Assessing Likelihood and Severity

Once you have assembled your list of potential threats it is time to assess how risky they are. For each threat you should estimate its **likelihood**, the chance of it happening; and its **severity**, how bad it would be. There are many ways to do this, perhaps the simplest is to assign one of three categories for each axis, e.g. low, medium, or high. Once done you will be able to combine likelihood and severity to determine which threats you should prioritise.

Suggested prioritisation matrix:

|                   | Low Impact | Medium Impact | High Impact |
| ----------------- | ---------- | ------------- | ----------- |
| Low Likelihood    | LOW        | LOW           | MEDIUM      |
| Medium Likelihood | LOW        | MEDIUM        | HIGH        |
| High Likelihood   | MEDIUM     | HIGH          | HIGH        |

### Mitigating Risks

Finally, work through the prioritised list of threats and suggest ways to mitigate those risks. These don't have to be technical solutions; it can be cheaper **and** more effective to put a non-technical control in place instead.

## Part 3 Vulnerable Docker Box

The "Damn Vulnerable Web Application" will let you see some concrete examples of exploits. It is a deliberately vulnerable web application to let you safely and _legally_ explore breaking into a system. To make it easy to run locally there is a Docker image provided - quick start instructions below. It is largely self-explanatory but for more detailed instructions go to [README.md](https://github.com/opsxcq/docker-vulnerable-dvwa/blob/master/README.md).

### Quick Start Instructions

Run the following docker command

```bash
    docker run --rm -it -p 5000:80 vulnerables/web-dvwa
```

Visit `localhost` on your machine, click to `Create / Reset database` and authenticate with `Username: admin` and `Password: password`.

## Part 4 XSS Training (Optional)

XSS bugs are extremely common. Google have developed a game that helps demonstrate how some of these work.

You can find the game [here](https://xss-game.appspot.com/) and work through it.
