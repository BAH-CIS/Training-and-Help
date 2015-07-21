# Using GitHub


## Purpose of this document

This document will document how we manage access and usage on public-facing services such as GitHub.com. Where possible, these policies and procedures should apply in a broad sense to any such service, not just a particular case such as GitHub. This will help us to standardize on how access requests are made and granted and how we engage with the public on such platforms.

Decisions herein are based on what we value:

 - collaboration
 - transparency and accountability
 - discipline and rigor
 - trust in our team

## Broadly applicable guidelines

### Transparency and accountability

It should be straightforward to know who is who, and with whom you're interacting. 
Seeing that CowboyMonkeyIcecream333, whose avatar is a blobfish and who has no other name, merged PR #152 is not OK. Seeing that CowboyMonkeyIcecream333 is in fact your colleague John Jacob and that he merged it is better.

### Team / access management

Access to a service should start with a request to the appropriate people. 
Ideally this is consistent, and requesting access to GitHub would go through the same channel as requesting access to, say, Mapbox.

Access requests should be responded to as quickly as possible.

Team members should expect and get the access they need to do their best work, in accordance with the values outlined above.

### Collaboration

Great work often happens when people collaborate. Peer review and constructive feedback encourage high-quality software, design, and so forth. We trust in our own skills and also in our team members' ability to help us improve. Consequently, we use practices such as Pull Requests (as opposed to direct pushes) to ensure collaboration.

### Best practice authentication

We should use the highest degree of authentication protection that the service provides.
This will likely be some form of 2-factor authentication (1 thing you know, 1 thing you have) involving a combination of password and hard- or soft-token access code.

# GitHub.com-specific guidance

## Creating a GitHub.com account

If you haven't created a GitHub account yet, do so with your personal email.
Then, in your existing or newly created GitHub account, simply add your work email to your existing account.
Do not create separate accounts for your personal and work email.
You can also set up custom email routing through the [Notifications Center](https://github.com/settings/notifications).

### Improving your account profile

#### [Activate 2-Factor Authentication](https://github.com/blog/1614-two-factor-authentication)


All team users are *required* to employ 2-factor for their GitHub access.
While you're at it, it's a *very, very* good idea to do this for your
[Gmail account](http://lifehacker.com/5932700/please-turn-on-two-factor-authentication/all)
and [elsewhere](http://lifehacker.com/5938565/heres-everywhere-you-should-enable-two-factor-authentication-right-now/all).
GitHub access _will not_ be provided if 2FA is turned off.

#### Add your name to your account

This makes it a lot easier for your teammates to know who's account it is and to administer the teams,
but most of all it helps a lot with autocomplete in a bunch of situations.

Go to [your settings page](https://github.com/settings/profile) and make sure your name (first and last) is filled in.


#### Add a profile picture

It only takes a moment to go to [your settings page](https://github.com/settings/profile) and upload a profile picture.

This simple courtesy makes team projects all the more social and fun and helps foster engagement with external contributors.
We are not dogmatic that it be a headshot, but please make it unique.

![Profile Page](https://cloud.githubusercontent.com/assets/633088/2552255/4a323746-b697-11e3-9340-8e215376e85a.png)

#### Publicize your membership

We encourage you to make your membership in this organization public.

Go to the organization's [team page](https://github.com/orgs/cfpb/people) and click (Make Public).

![image](https://cloud.githubusercontent.com/assets/633088/2619076/716a3d34-bc2a-11e3-9772-27df7ed4f6ec.png)

## Teams

All write- or admin-level access to repositories in the organization is controlled via [Teams](https://help.github.com/articles/permission-levels-for-an-organization-repository). Policies and procedures for access requests are described below.

Organization membership is granted to Bureau employees and contractors. 
We expect exceptions to this to be rare, but temporary membership may be extended on an as-needed basis. 
Such cases may include former employees or external collaborators who contribute heavily to a project or whose expertise warrants membership.

Contractors or external collaborators should only be added to teams with scoped write permissions to the repos they're working on.
They should never have admin level rights.
To separate these permissions, create a team with admin permissions in the format of `projectname-admins` for staff and a team with write permissions in the format of `projectname-contributors` for all other collaborators.

Access to private repositories will be granted on an as-needed basis.

Request team membership / repository access by filing an issue in our internal issue tracker, 
where it will be reviewed and acted upon.
We aim to complete these requests in under a few hours. 
This helps us keep a record of team membership activities and demonstrates responsible access control.
Wherever possible, this same mechanism for requesting access to a service should be used.

Even if you don't have write access into a repo, we strongly encourage the submission of pull requests for improvements or fixes.

### Removing team members

The default for a team member leaving the CFPB is to have admin **and** write privileges removed. We'd retain write privileges for some temporary amount of time in special cases. Is there any good reason for this person to retain write privileges? If not, remove them.

If it _is_ decided that write privileges should be removed from a departing teammate, they should also be removed from the CFPB organization as a whole. Their legacy will live on in the commit history.

**Note**: Activities such as adding and removing team members [are logged](https://github.com/blog/1872-improved-audit-log).

## Contributing code

Except in rare cases, all contributions should be done via Pull Requests. 
This includes commits from team members with admin and write permissions. 
We strongly encourage meaningful code review in pull requests.
Contributions are held to the same high standards for team members and external collaborators alike.

## Separate Organizations

Currently, we keep our software under the single `CFPB` organization.
We can revisit this when warranted, for example in a case where a project reaches the enviable position of taking on a [life of its own](https://github.com/twbs/bootstrap).
Any organization created for the purpose of open-sourcing CFPB-created software will follow this guidance document.

## Tips and tricks

* [GitHub + IFTTT = all kinds of possibilities](https://ifttt.com/github)



***

This document is based on work started by Noah Kunin