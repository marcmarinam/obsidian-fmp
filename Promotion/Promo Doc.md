**1 - You can lead confidently in tackling some of the most complex or challenging technical problems faced by your team, from design and planning to implementation.**
- I scaffolded the freemium system using the microservice generator and brought it up for production. Converted the repo into a monorepo with multiple deployed services, set up the pipelines to accommodate the new structure, created shared packages to consolidate logic between the services, helped fix issues with the microservice template and added significant instrumentation and Grafana dashboards. The freemium system allowed us to run serveral experiments such as the Cardless Free Trial and Free Hints experiments.
	- Created the Freemium API service, a TS + GraphQL API that is stitched with titan marshal.
	- Created the Freemium Rules Runner service, a Kafka consumer that deals with Reward logic, creating rewards based on user actions.
	- Created the Freemium GDPR service, which handles GDPR deletion requests.
	- Worked on the freemium architecture proposal. From creating the document to handling the proposal review meeting and creating tickets to implementing changes suggested in the review.
- Worked extensively on the free trial remake and led Phase 2 of it. The remake consisted of changing free trial logic to move from a 14-day free trial using coupons to any length free trial without coupons. This was a significant task because 14-day had been the standard for years.
	- Phase 1: Moved on from the classic 14-day free trial to a variable 3, 7 or 14 day by introducing user journeys. These user journeys had specific eligibility criteria based on our needs for the product. I added new queries to ecomm-gate that contained FT eligibility based on the user journey. I handled the migration from the old free trial eligibility to the new queries.
	- Phase 2: Stopped using Recurly coupon codes to offer free trials. In order to enable data science to analyse experiments based on different journeys a storage solution had to be introduced. I designed the tables we would need to be able to track FT purchases and modified the purchase workflows to store and retrieve the data when needed. The data would tell us where a free trial was purchased from (tree onboarding, hints, search, etc.) as well as its duration. Once Phase 2 was fully released I also handled tearing down the old logic and code throughout titan and ecomm-gate.

**2 - You are an evangelist for consistent high-quality and efficient delivery within your team.**
- I have created several hooks and utilities to help my teammates deliver code more easily and with better quality.
- I have constantly gone back to areas of the product that we have worked with and tried to improve the code. When we started having multiple free trial journeys, I gathered all the scattered logic and brought it into a common package where it would be easier to work on. I also added unit tests that would automatically test everything belonging to a journey without any extra work. It would test journey translation, copy, eligibility, etc.

**3 - You look beyond short-term deliverables, helping the team manage their long-term responsibilities.**
- During the planning of Phase 2 of the FT Remake I made sure that we would be future-proofing the work. By carefully picking what data we were storing and how, we made it so future experiments needed little to no work on the backend to enable new free trial journeys.

**4 - You're likely to have ownership of various tools/systems/processes within your team.**
- Everyone in our team maintains the freemium system, but I am usually the point of contact for big changes. These changes include setting up new services within the monorepo, working with pipelines, architectural/design changes, etc.
- Since I was the one who refactored the experimentation framework, I am the point of contact when debugging issues, consulting new needs for the framework, migrations, etc. I assisted several teams with setting up/debugging experiments. As well as the data science team when they migrated from Google Tag Manager to Snowplow tracking.

**5 - You help others to deliver more value by sharing your expertise in certain technologies/processes.**
- Sharing backend & payment expertise with less experienced teammates.
- Refactored the experimentation framework to reduce the number of LaunchDarkly variants needed by half by injecting Google Optimize experiment IDs in code instead of LD variants. This reduced release issues and simplified the experiment development tasks. I also added Grafana dashboards that tracked experiment allocation automatically for every new experiment released.

**6 - You are a trusted influencer within your team and regularly use this position to positively impact the team.**
- People often ask for my opinion when it comes to code structure, best practices and general advice.

**7 - You're supporting the growth and development of your team, and individuals inside, or outside your team.**
- I wrote the Titan experimentation guide, where I detailed all the necessary steps to get an experiment up and running. It contained steps to create the release toggles, setting up the tracking in Google Optimize, how to work with variants in the code, best practices, where to find metrics, etc. I also assisted several teams in the creation of experiments as well as debugging issues that appeared while they were running. Most notably the Goose team.
- Offered a lot of guidance to my teammates when they struggled to understand certain topics or technologies. The person I've helped the most is Morag. She joined the team as a Junior and I helped her a lot by breaking down our processes, technologies, ways of working, problem-solving, etc. Since then she has been promoted to Software Engineer.