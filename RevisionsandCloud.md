# Git Tutorial

## Version Control
>sytem that allows you to revisit various versions of a file by recording changes. Allows users to revert a file or project to a previous version, track modifications, and modifying individuals, and compare changes.

**Local Version Control**- entails one database on your hard disk that stores changes to files.
**Centralized Version Control**- entails a single server storing all changesand file versions, which can be accessed by various clients. Allowed programmers to have more knowledge of team member activitiesand gave administrators more control over divvying up revision priveleges.
**Distributed Version Control**- allows clients to create mirrored repositories which can be easily placed on a server to replace lost information. Multiple mirrored repositories enable the use of various simultaneous workflows

## What is Git

**Snapshots**Commi
Git is a Distributed Version Control System that stored data in a file system made up of snapshots which are taken whenever you save a changed version of your project, and a reference of them is stored.

**Local Operations**
Git mostly relies on local operations because most necessary information can be found in local resources. This allows for process expediency because a project's history resides on the local disk eliminating the need to fetch history information from the server, and allowing one to continue work on a project even when not online or on a VPN.

**Tracking Changes**
Every single change applied to any file or directoryis tracked by Git which will always detect file corruption or loss of information in transit

**Loss of Data**
Git makes it extremely difficult for a snapshotof your file that is committed to be lost

**States**
Files in Git reside in three main states: commited, modified, staged. 

**Committed***
data is securely stored in a local database

**modified**
File has been changed but not committed

**Staged**
change to be committed in the next snapshot
