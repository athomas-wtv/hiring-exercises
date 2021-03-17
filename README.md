# Interview Project: Full Stack, Investor Site

# Welcome!

Hello! If you are reading this then we're likely in the process chatting with you about a technical role at [Pure](https://purepm.co). If so, congratulations :tada: !

In order to move forward, we'd like to know a little about how you work. To that end, this repository contains a **short, time-boxed** (approximately 1h 30m max) that you can use demonstrate your skills and abilities.

These are **NOT** *coding exercises*. The goal of these exercises is to give you an asynchronous medium for demonstrating how you would work through a set of user stories. There is no grading or scoring, nor is it pass-fail, rather these are meant to serve a sample of your reductive thought processes as an engineer.

## First, a few words on asynchronous/take-home exercises

We know that the technical hiring processes in our industry are generally broken. We also know that there are mixed opinions on take-home exercises in general. The primary reasons we ask candidates of *all* levels to complete these exercises are as follows.

*  We're a fully-remote team, currently all based within continental US, but spread across multiple time zones. Async exercises allow you to show off your skills at a time/place that works for you.

*  Take-home exercises allow you to work at your own pace. We intentionally structure these to take around 1h 30m in time and ask that you limit your investment to no more than the suggested time, however you are free to break this into as many sessions as you wish.

* It matches the nature of our work. Most of being an engineer on a remote team is self-directed exploration of a problem, followed by period(s) of cyclic work/edit/review, followed by submittal for review and approval by your peers. Async exercises allow you to do the same.

* It eliminates the performance anxiety of forced-pairing with someone whom you've just met.

## General Instructions

1. We would like you to work through the following User Stories below, adding the relevant functionality to the application.

2. When you are comfortable with your changes, submit a pull request against the the repository. We will review it withn 48 hours and respond back to you in a timely manner.

3. Complete as much of the exercise as you can in 1h 30m or less. Don't worry if you don't complete the exercise; we're more interested in how you structure your code, your approach to testing and the readability of the code.

## Tech setup

1. Clone a copy of the repository
2. Install the relevant tools in each of the `frontend` and `service` folders with `npm i`
3. Spin up the backend service (see details on Tech Setup below).

The back-end service uses dockerized services, to save having to install each component on your machine locally. There's a good [Getting Started](https://www.docker.com/get-started) tutorial if you're not familiar with docker yet.

## Questions

Drop us a line at careers@purepm.co and we'll be happy to elaborate on anything here.

## User Stories

#### Login failure isn't handled gracefully

**As an** Investor
**I want** to know if I input incorrect credentials
**So that** I can check my input

#### Investor Should be able to see Amount of Deposit/Withdrawal

**As an** Investor
**I want** to view the amount of transactions
**So that** I can easily track the balance

#### Investor Should be able to see Interest Deposits

**As an** Investor
**I want** to view my initial investment
**So that** I can calculate returns
