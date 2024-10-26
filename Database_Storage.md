# Title
Database Storage System of *Dotify*

## Status
The status of this ADR is *accepted*

## Context
In our application, whether we use a local or remote database will impact the safety of our app. Especially if we implement the GPS utility.

## Decision
As a group, we have decided that remote database storage is a better way of storing data as well as it is more effective.

**Reasoning**:
1. As stated previously, it is safer for users to store their information like profiles, playlists and other related information as it will stored on an isolated server. This will also allow users to be able to access their profiles on many different devices, such as a computer or tablet.
2. As for who and how the information will be available, there will only be select administrators that have access to the information allowing for more security. The data will be encrypted as it is sent to then make it even more secure.

## Consequences

1. Allowing users to have access to their information from remote servers, and giving the option of signing into their account from different devices enhances the user experience and the user engagement to the app.
2. Encrypting the data while transferring encourages safety and security of user information as it protects from unauthorized access of this data. With this said, having select administrators have access to the information will allow them to perform routine checks to make sure that all the standards are up to date.