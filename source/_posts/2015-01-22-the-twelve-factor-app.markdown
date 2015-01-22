---
layout: post
title: "The Twelve-Factor App"
date: 2015-01-22 15:48:34 +0800
comments: true
categories: "笔记"
---
## The Twelve-Factor App
仔细读了1，2，3，4，5感觉比较有用，再思考在iOS开发中如何应用，其余的项目看不太懂，理解不了。

1. Codebase - one codebase tracked in revision control, many deploys

git codebase deploy version

2. Dependencies - explicitly declare and isolate dependencies

CPAN for perl, Rubygems for Ruby, Explicitly

Python : Pip for declaration / Virtualenv for isolation

do NOT rely on the implicit existence of any system tools

3. Config - store config in the environment

vary between deploys, group/environments Rails : <code>deployment</code>, <code>test</code>, <code>production</code>

4. Backing Services - treat backing services as attached resources

DB, Amazon S3, OAuth API, etc

attached and detached to deploys at will, without any code changes

5. Build, release, run - strictly separate build and run stages

a release cannot be mutated once it is created, any changes must create a new release

6. Processes - execute the app as one or more stateless processes

7. Port binding - export services via port binding

8. Concurrency - scale out via the process model

9. Disposability - maximize robustness with fast startup and graceful shutdown

10. Dev / prod parity - keep development, staging, and production as similar as possible

11. Logs - treat logs as event streams

12. Admin processes - run admin/management tasks as one-off processes