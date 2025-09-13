# New software workflows in an LLM world
> Faisal Memon 13th September 2025.

![Workflows](./llm_workflows.png)

I find myself writing code in a different way nowadays. I'd like to share my recent experiences with LLMs that up-turn some of the orthodoxy in software engineering practices that have been considered best practice.

The following experiences stem from some hobby work I've been doing lately (an AI driven app for problem solving) as it gives me a chance to work differently than the agreed way of working we find ourselves conforming to in corporate software engineering settings.

## I don't write tests, I only collect logs

I've been working on the server for my hobby project (it is python server using Fast API for REST calls, and pydantic for LLM integrations).

One early decision was to make it log everything as I developed the server. Then I started piecing together the server API endpoints and writing the code. I am primarily a front-end developer so I hit newbie errors and had to do my share of research to get it done.

The reason why I kept logs was that once I had 90% of the functionality done, I asked an LLM to write my unit test cases, using the logs for insight on the scenarios and problems it should test for. The test cases ended up pretty good. When the test cases injected data, it was real, or realistic looking, data.

To be fair, some extra prodding was needed to complete the job. It was mostly me describing the behavior I was concerned about (in a BDD way of thinking) and then the LLM just cranked out the test cases.

Whilst it wasn't my explicit goal, I ended up with 100% coverage (not claiming that is the optimal state of affairs as the state space is more nuanced than a mere coverage number).

The corollary for me is that TDD is not that helpful anymore. Better to focus on the problem domain and do a clean simpleminded solution. The LLM can take to from this hand off point to a testable, tested solution.

## Using LLM difficulty as a proxy for value generation

There are lot of things a software engineer can do that makes them feel good. One is a juicy refactor. Another is to write lots of simple tests for trivial logic or tautological tests that wouldn't ever fail. They are just like eating a candy bar - a sugar rush. Some people call it green bar syndrome because you see all your tests passing with pleasant green bars of success on the screen.

What I am questioning is whether I am creating true value. Am I solving the meaningful problems and actually moving things forwards.

A proxy measurement for whether I am creating value, for me, is to ask an LLM to do a task. If it truly fails and struggles, it means it is an essential problem. Something for a human to work on. If the LLM can kick off a solution with no sweat, like a refactor or generating test cases, that says to me it is low complexity work. I shouldn't be involved there. Either don't bother doing it, or let the AI do it.

<p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/faisalmemon/articles/blob/main/New_software_workflows_in_an_LLM_world.md">New software workflows in an LLM world</a> by <span property="cc:attributionName">Faisal Memon</span> is licensed under <a href="https://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt=""></a></p>
