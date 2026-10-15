# Decision log

| Date | Decision | Rationale | Follow-up |
| --- | --- | --- | --- |
| 2026-10-15 | Retain as a legacy Java comparison lab, not a duplicate. | It provides a distinct JSP/JPA/Hibernate/Tomcat perspective on the helpdesk domain. | Link alongside, rather than replace, the modern XpeedOPR project. |
| 2026-10-15 | Treat tracked database credentials as a remediation blocker. | Credentials do not belong in tracked configuration for shared or deployed use. | Schedule rotation, removal, and history-scope review separately. |
| 2026-10-15 | Keep the repository out of production claims. | Important functionality and modern operational controls remain incomplete. | Reassess after a dedicated modernization effort. |
