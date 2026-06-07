# The-3-CTF-Formats-That-Still-Work-in-an-AI-Dominated-World
<img width="1508" height="848" alt="image" src="https://github.com/user-attachments/assets/184e564e-07b6-4311-8f53-91aac2525a0c" />

The jeopardy-style CTF had a good run. For nearly three decades, it was the default format for cybersecurity competitions. Participants solve isolated challenges across categories like web, crypto, forensics, and binary exploitation, submit flags, and climb a leaderboard. It was clean, scalable, and effective.

Then AI agents showed up and solved everything. At [BSidesSF 2026](https://bsidessf.org/), autonomous systems cleared all 52 challenges, many within minutes of release. CTFAgent outperformed 88% of human teams on [PicoCTF](https://picoctf.org/) in fully automated mode. [CryptoPilot](https://cryptopilot.ai/) achieved a 100% solve rate on the [InterCode-CTF](https://intercode-benchmark.github.io/) benchmark. A research team built D-CIPHER, a multi-agent framework where specialized planner and executor agents coordinate to handle every [challenge category](https://www.simulationslabs.com/scenarios). And at [CSAW](https://www.csaw.io/), [NYU](https://www.nyu.edu/) now runs an entire competition track dedicated to building autonomous CTF-solving agents, acknowledging that AI-driven solving is the new reality.

The format isn't dead for learning. But as a measure of professional skill, it's been fundamentally compromised. So what works instead? Three formats have proven resistant to AI automation, and each one tests skills that matter more in professional cybersecurity than puzzle-solving ever did.



# Format 1: Attack and Defense

In an attack-and-defense CTF, teams simultaneously defend their own infrastructure while attacking other teams' systems. There's no static flag hidden in a file. Instead, flags rotate periodically, services have to stay online, and points come from both offensive and defensive actions.



[DEF CON CTF](https://defcon.org/), the most prestigious competition in the field, uses this format for its finals. The competition runs in ticks of one to five minutes, and teams earn points three ways: capturing opponents' flags, defending their own services, and keeping services operational. The DEF CON 2025 finals also featured King of the Hill and LiveCTF components alongside the core attack-and-defense format, creating a multi-layered competition that no single AI system could optimize across. Traffic analysis plays a central role in attack-and-defense. Teams use tools like Tulip to monitor inbound requests and can often observe and replay other competitors' exploits as well as discover vulnerabilities they haven't yet found themselves.

[saarCTF](https://ctf.saarland/), which earned a weight of 97.22 on [CTFtime](https://ctftime.org/), stands out as one of the few online attack-defense competitions. The format closely simulates real-world security operations, making it particularly valuable for teams preparing for professional roles. The International Cybersecurity Challenge in Tokyo 2025 featured attack-and-defense on Day 2 of competition, and organizers described it as a rarity even among global CTF events precisely because it demands both offensive and defensive expertise simultaneously.

This format is AI-resistant for a straightforward reason: the environment never stops changing. Other human teams are actively modifying their systems, patching vulnerabilities you just found, and launching attacks you haven't seen before. An AI agent that solves a static puzzle in three minutes has no advantage when the puzzle reshapes itself every thirty seconds based on what seven other teams are doing simultaneously. Attack-and-defense also tests defensive security, a skill set that jeopardy completely ignores but that most cybersecurity professionals spend their time actually doing.

The challenge for organizers is infrastructure. Attack-and-defense requires dedicated networks, service monitoring, and careful scoring systems. But platforms that provide managed infrastructure have made this format accessible to organizations that couldn't have hosted it five years ago.

# Format 2: King of the Hill

King of the Hill sits between jeopardy and attack-and-defense. Teams compete to gain and maintain control of shared systems. You might exploit a vulnerability to gain access, plant your team's flag, then defend that position while other teams try to take it from you.

[DEF CON CTF](https://defcon.org/) finals incorporated King of the Hill as a dedicated component alongside attack-and-defense in 2025. In their implementation, KotH challenges are jeopardy-style tasks played in rounds spanning several hours, where the objective is to develop the most effective solution for each round. After every round, the challenge changes, forcing teams to adapt continuously. For example, a KotH task might involve writing the shortest possible shellcode to read a flag, with each new round banning additional bytes, requiring teams to continually refine their approach. Virginia Tech's [SummitCTF](https://summitctf.org/) 2025 also used attack-defense for its in-person event while keeping jeopardy for the virtual track, showing how organizers are increasingly moving competitive in-person events away from pure jeopardy formats.



What makes this format AI-resistant is persistence under adversarial pressure. It's not enough to find an exploit. You have to maintain access while others are actively trying to remove you. This requires reading the environment, adapting your tactics in real time, and making strategic decisions about where to invest effort. Do you defend your current position or go after a higher-value target? Do you patch the vulnerability you used so nobody else can exploit it, or leave it open as a backup entry point?

These are judgment calls that depend on context, timing, and reading your opponents. AI can reason about these in theory, but the real-time, competitive, multi-party nature of King of the Hill creates a decision space that's fundamentally different from solving a static challenge. The information is incomplete, the environment is adversarial, and the optimal strategy depends on what everyone else is doing right now.

# Format 3: Cyber Drills and Full-Scale Simulations

Cyber drills go further than any [competitive CTF](https://www.simulationslabs.com/host-ctf) format by simulating actual security incidents from start to finish. Teams don't just find and exploit vulnerabilities. They detect threats, investigate incidents, coordinate their response, communicate with leadership, and manage the aftermath.



[NATO's Locked Shields](https://ccdcoe.org/locked-shields/) is the gold standard. The 2026 iteration brought together approximately 4,000 participants from 40 nations in a realistic, large-scale live-fire cyber conflict. It tests technical, operational, and strategic capabilities alongside decision-making under pressure, and incorporates legal and communication considerations. Teams protect vital services and critical infrastructure that modern societies depend on. All systems reflect authentic risks and [real-life scenarios](https://www.simulationslabs.com/scenarios). This is about as far from a jeopardy CTF as [cybersecurity training](https://www.simulationslabs.com/student-training) gets.

The trend is accelerating at the regulatory level, too. The U.S. Coast Guard's cybersecurity rule, effective July 2025, mandates that maritime facilities and vessel operators conduct two cyber drills and one full-scale exercise annually. Cyber Management Alliance, which has facilitated drills for over 400 organizations globally, reports that in 2026, cyber drills are no longer a nice-to-have but a regulatory expectation and a board-level priority. Their [scenarios](https://www.simulationslabs.com/scenarios) go beyond simple phishing simulations to challenge security teams and cross-functional stakeholders in realistic, complex ways, including ransomware with simultaneous data leak, business email compromise, and supply chain attacks.

This is the most AI-resistant format because it tests everything AI is worst at. There's no single right answer. Success depends on team communication, prioritization under stress, cross-functional coordination, and decision-making with incomplete information. A [SOC analyst](https://www.simulationslabs.com/blogs/How_to_use_Simulations_Labs_to_assess_SOC_Analysts_-_Simulations_Labs) has to decide which alerts matter. A team lead has to brief a simulated CISO. Someone has to make the call on whether to shut down a system or keep it running while investigating.

[Cyber drills](https://www.simulationslabs.com/blogs/Why_Conduct_Cyberattack_Cyber_Drill_Simulations_for_Your_Organization-SimulationsLabs) also operate on a timescale that matters. A jeopardy CTF challenge might take thirty minutes. A drill runs for hours or days. This tests stamina, handoff procedures, shift management, and the kind of sustained focus that actual incident response requires. These are organizational skills as much as technical ones, and they're skills that separate effective security teams from collections of individually talented people.

# What This Means Going Forward

The three formats share a common thread. They all test skills that require human judgment, real-time adaptation, and team coordination. These are the skills that define effective cybersecurity professionals, and they're the skills that AI is furthest from replicating.

This doesn't mean [jeopardy-style CTF](https://www.simulationslabs.com/host-ctf)s are worthless. They remain excellent for learning fundamentals, building community, and introducing people to cybersecurity. But for skill assessment, hiring decisions, and organizational readiness evaluation, the industry needs to move toward formats that test what actually matters. When DEF CON structures its finals around attack-and-defense rather than jeopardy, when NATO runs 4,000-person live-fire simulations, and when regulators mandate annual cyber drills, the direction is clear.

The good news is that these formats are becoming more accessible. Managed platforms now handle the infrastructure complexity that used to limit attack-and-defense and simulation-based exercises to well-resourced organizations. What used to require a dedicated DevOps team and weeks of setup can now be launched in hours. The barrier isn't technology anymore. It's a mindset. The question for every [cybersecurity training](https://www.simulationslabs.com/student-training) program, every hiring manager, and every team lead is simple: are you still measuring skills that AI already does better, or are you building toward the skills that will matter for the next decade?

[**Simulations Labs**](http://simulationslabs.com/) is a cybersecurity simulations platform for hosting [CTFs](https://www.simulationslabs.com/host-ctf), [cyber ranges](https://www.simulationslabs.com/cyber-range), and cyber drills.

[Get Started Now For Free](https://app.simulationslabs.com/register/tenant)

# FAQ

# Why are traditional jeopardy-style CTFs becoming less effective?

Traditional jeopardy-style CTFs focus on solving isolated, static challenges with clear success criteria. Modern AI agents can now solve many of these challenges automatically and at scale, reducing their value as a measure of real-world cybersecurity skill.

# What are the three CTF formats that still work in an AI-dominated world?

The three formats highlighted are:

1. Attack and Defense
2. King of the Hill (KotH)
3. Cyber Drills and Full-Scale Simulations

These formats emphasize adaptability, teamwork, and decision-making instead of static puzzle-solving.

# What makes Attack and Defense CTFs resistant to AI?

Attack-and-defense environments constantly change. Teams must defend their own infrastructure while attacking others in real time. Since human teams continuously patch systems and change tactics, there is no fixed puzzle for AI to optimize against.

# What skills do Attack and Defense competitions test?

These competitions test:

* Offensive security
* Defensive security
* Service availability management
* Real-time monitoring
* Incident response
* Strategic adaptation under pressure

They better reflect real-world security operations than static CTFs.

# What is King of the Hill (KotH) in cybersecurity competitions?

King of the Hill challenges require teams to gain and maintain control of systems while competing teams attempt to take control away. Teams must continuously adapt their strategies as the environment changes.

# Why is King of the Hill difficult for AI systems?

KotH requires persistence, strategic decision-making, and adaptation to incomplete information in a competitive environment. Success depends heavily on timing, judgment, and reacting to human opponents in real time.

# What are cyber drills and full-scale simulations?

Cyber drills simulate real-world cybersecurity incidents from detection through response and recovery. Teams handle technical investigations, communication, leadership coordination, and operational decision-making during realistic crisis scenarios.

# Why are cyber drills considered highly AI-resistant?

Cyber drills involve ambiguous situations with no single correct answer. They require:

* Team communication
* Leadership coordination
* Prioritization under pressure
* Cross-functional collaboration
* Long-duration operational management

These are areas where human judgment remains critical.

# What is NATO Locked Shields?

Locked Shields is a large-scale live-fire cyber defense exercise organized by NATO. It simulates realistic cyber conflict scenarios involving thousands of participants and tests technical, operational, legal, and strategic capabilities.

# Are jeopardy-style CTFs still useful?

Yes. They remain valuable for:

* Learning cybersecurity fundamentals
* Practicing technical concepts
* Building communities
* Introducing newcomers to cybersecurity

However, organizations should not rely on them alone for hiring or readiness assessments.

# What should organizations focus on moving forward?

Organizations should prioritize training and assessments that evaluate:

* Strategic thinking
* Real-time adaptation
* Team collaboration
* Communication under stress
* Operational decision-making

These are the skills most relevant to modern cybersecurity roles and hardest for AI to replace.
