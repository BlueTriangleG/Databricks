
## Services provided by backend:

- authentication service (login / logout / session refresh / invitaion link)
- profile service (user info / permission)
- video file processing service (file upload / download / format check / cropping)
- project service (planned show info / submission management)  [Tip: submission = submitted project]
- brick status service (overall status / specific data / preview after uploading)   


## Reuse Plan:

- framework choice:
    - frontend: reactjs
    - backend: nodejs
    - database: to be decided

- SSO service:
    - Login/logout feature: depend on framework (can write by ourselves)
    - Session management feature: JWT
    - Invitation link: Use existing email service and authentication service, basic idea: use the authentication service to encrypt new user profile info and send it with email service
        [Link from reddit](https://www.reddit.com/r/node/comments/108c6id/email_invite_link_module_for_nodejsexpress_app/)
        [Link from Medium](https://manishbit97.medium.com/sending-email-via-node-js-with-calendar-invite-2ebf8637b22f)

- file processing service:
    - uploading file: for frontend, use reactjs's native file uploader; 
      for backend, store filename in database, store file on server

- profile service:
    - depend on backend framework, permission feature required
    - frontend features can build from scratch based on requirements

- project service:
    - frontend and backedn features can build from scratch based on requirements


## Design Concept Diagram

![[Design Concept Diagram & Reuse Plan.drawio.png]]