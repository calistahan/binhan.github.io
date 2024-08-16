---
title: "Active Directory Domain Services"
layout: post
date: 2024-08-16
feature_image: images/
tags: [ad, activedirectory, networking]
---

! NOTICE! Due to the nature of github pages, this page remains a draft until 9/01/24. 

*Writeup summarizing my learning experience with Active Directory.*

<!--more-->

<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

## Table of Contents

1. [AD Overview](#ad-overview)

<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### AD Overview
✧. ┊ ⁭ [tbd](#ೃ⁀-tbd) ✧ [tbd](#ೃ⁀-tbd) ✧ [tbd](#ೃ⁀-tbd) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ What is Active Directory?
Active Directory is a Microsoft database tool that allows companies to manage their IT infrastructure and can manage users, objects, domains, devices, and groups. AD DS allows for a hierarchical directory and a way for network admins to apply configuration and security settings for user accounts easily. 

<br>
####  ೃ⁀➷ Schema
Definitions of object types and attributes for objects

<br>
####  ೃ⁀➷ Domain
Contains objects like users and computers.

<br>
####  ೃ⁀➷ Domain Tree
Collection of domains that have a root and DNS namespace (hierarchical tree)

<br>
####  ೃ⁀➷ Forest
A collection of 1+ domains that have the same root, schema, and global catalog

<br>
####  ೃ⁀➷ OU
Container object that holds users, groups, and computers. Links GPOs (Group Policy Objects)

<br>
####  ೃ⁀➷ Container
Object for organization. Can not link GPOs. OUs cannot be created within a container.

<br>
####  ೃ⁀➷ User Account
All users that need access to network resources should have a user account which can authenticate to the AD DS domain in order to access the resources. User accounts have a username, password, and groups. User objects can be created or managed with the AD Administrative Center, AD Users and Computers, Windows Admin Center, PowerShell, or dsadd.

<br>
####  ೃ⁀➷ Managed Service Accounts
Services that run at startup or other events and don't require user interaction can use a service account to start up and authenticate. 

<br>
####  ೃ⁀➷ Groups
Group users together to easily assign permissions and rights. Security groups are security enabled. Distribution groups are not security enabled, and can be used for email applications. Groups also have a scope such as local (local workstation), domain-local (all workstations in local domain), global (for a department or specific geographic location), and universal (assign anywhere in forest). 

<br>
####  ೃ⁀➷ Objects
Contains objects like users and computers.


└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘


<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>



#### Sources & References
