# google-developer-group-praxis-2.0
APPROACH
My project is not just a website; it is a Decision Support System (DSS). It moves beyond static text to dynamic simulation.

Pilot-First Methodology: Instead of simulating the whole country (too complex), you focus on 10 Key Metro Cities (Delhi, Mumbai, Bengaluru, etc.) as a representative sample.

Hybrid Analysis: You combine Quantitative Data (hard numbers: cost, voter turnout, security forces) with Qualitative Insights (AI-driven constitutional & social impact analysis).

User-Centric Simulation: The user acts as a policy-maker. They can "toggle" simultaneous elections to see the immediate difference in cost vs. the potential risk to federalism.

ARCHITECTURE
Architecture
This is a decoupled Client-Server Architecture designed for scalability and clear separation of concerns.

| Layer        | Technology        | Role                                                                                                                       |
| ------------ | ----------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Frontend     | React.js          | Interactive dashboard. Sends JSON queries to backend; renders charts (Recharts/Chart.js) and Markdown responses.           |
| Backend      | Node.js + Express | The "Brain." Validates requests, routes traffic, and orchestrates the simulation logic.                                    |
| Intelligence | Google Gemini API | The "Analyst." Processes natural language queries (e.g., "Impact on regional parties?") and generates qualitative reports. |
| Data Store   | JSON / MySQL      | Stores static city data (Population, 2024 Election Turnout, Security Deployment stats).                                    |

ASSUMPTIONS
3. Assumptions
These are critical for my simulation logic.

A. Financial Assumptions
Cost Synergy: We assume a 30-50% reduction in recurring election costs if held simultaneously (based on NITI Aayog & ECI estimates).

EVM Lifespan: We assume EVMs have a 15-year life; thus, ONOE requires a massive one-time upfront cost (approx. ₹10,000 Cr+) for new machines, which amortizes over 3 cycles.

Security Deployment: We assume security costs drop by 40% due to reduced movement of CAPF (Central Armed Police Forces) troops.

B. Operational Assumptions
The "One Voter" Rule: We assume the same voter list is used for both Lok Sabha and Vidhan Sabha (currently, they often differ).

Linear Scaling: We assume election costs scale linearly with population growth in your 10 metro cities.

C. Behavioral Assumptions (The "AI" Variable)
Voter Alignment: We assume a "National Effect": evidence suggests that in simultaneous elections, voters tend to vote for the same party at both levels (approx. 77% probability per IDFC Institute studies). Your AI should flag this as a risk to regional parties.

We use a Node.js backend to calculate financial savings based on NITI Aayog formulas, while our Gemini AI agent analyzes the qualitative impact on federalism and voter behavior in real-time. We assume a 30% cost reduction but highlight the risk of 'national wave' voting overshadowing local issues.
