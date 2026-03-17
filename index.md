---
layout: default
hide_sidebar: true
---

<style>
	body {
		padding: 28px;
	}

	.wrapper {
		width: min(1120px, 100%);
		margin: 0 auto;
	}

	section {
		width: auto;
		float: none;
		padding-bottom: 24px;
	}

	.ai-projects-banner {
		margin: 0 0 1.5rem;
		padding: 1.2rem 1.4rem;
		border-left: 6px solid #2f79b7;
		background: linear-gradient(120deg, #eef6fc 0%, #f7fbff 100%);
		border-radius: 8px;
		display: flex;
		align-items: center;
		gap: 1rem;
	}

	.ai-projects-banner img {
		width: 120px;
		height: 120px;
		object-fit: cover;
		border-radius: 8px;
		border: 1px solid #bcd3e7;
		box-shadow: 0 2px 8px rgba(18, 44, 68, 0.12);
		flex-shrink: 0;
	}

	.ai-projects-banner h1 {
		margin: 0 0 0.35rem;
		color: #185a92;
		font-size: 2rem;
		line-height: 1.2;
	}

	.ai-projects-banner p {
		margin: 0;
		color: #315974;
		font-size: 1.02rem;
	}

	.projects-list {
		display: flex;
		flex-direction: column;
		gap: 1rem;
	}

	.project-row {
		border: 1px solid #d7e4f1;
		border-radius: 10px;
		background: #ffffff;
		box-shadow: 0 1px 6px rgba(18, 44, 68, 0.07);
		padding: 1.1rem 1.2rem;
		min-height: 42vh;
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 1rem;
	}

	.project-left h2 {
		margin-top: 0;
		margin-bottom: 0.45rem;
		color: #16334b;
	}

	.project-left p {
		margin-top: 0;
		margin-bottom: 0.7rem;
	}

	.project-right h3 {
		margin-top: 0;
		margin-bottom: 0.45rem;
		color: #204564;
		font-size: 1.1rem;
	}

	.arch-diagram {
		border: 1px solid #d3e3f1;
		border-radius: 8px;
		padding: 0.65rem;
		background: #f9fcff;
		margin-bottom: 0.9rem;
	}

	.arch-diagram-compact {
		max-width: 380px;
		padding: 0.45rem;
		margin-top: 0.7rem;
		margin-bottom: 0;
	}

	.arch-layer {
		padding: 0.38rem 0.6rem;
		border-radius: 5px;
		margin-bottom: 0.28rem;
		font-size: 0.88rem;
		font-weight: 600;
		color: #16334b;
		text-align: center;
	}

	.arch-layer:last-child {
		margin-bottom: 0;
	}

	.arch-layer:nth-child(odd) {
		background: #ddeeff;
		border: 1px solid #a8c8e4;
	}

	.arch-layer:nth-child(even) {
		background: #f0f8ff;
		border: 1px solid #c5d9ea;
	}

	.arch-diagram-compact .arch-layer {
		padding: 0.28rem 0.45rem;
		font-size: 0.8rem;
		margin-bottom: 0.2rem;
	}

	.project-right ul {
		margin: 0;
		padding-left: 1.1rem;
	}

	.project-links {
		margin-top: 0.9rem;
		display: flex;
		flex-wrap: wrap;
		gap: 0.8rem;
	}

	.project-shot {
		margin-top: 0.75rem;
		margin-bottom: 0.9rem;
	}

	.project-shot img {
		width: 100%;
		max-width: 460px;
		height: auto;
		border: 1px solid #c9dced;
		border-radius: 8px;
		box-shadow: 0 2px 8px rgba(18, 44, 68, 0.12);
	}

	.project-row-architecture-right .project-left {
		order: 0;
	}

	.project-row-architecture-right .project-right {
		order: 1;
	}

	@media (max-width: 900px) {
		body {
			padding: 16px;
		}

		.ai-projects-banner {
			flex-direction: column;
			align-items: flex-start;
		}

		.ai-projects-banner img {
			width: 96px;
			height: 96px;
		}

		.project-row {
			min-height: auto;
			grid-template-columns: 1fr;
		}
	}
</style>

<section class="ai-projects-banner">
	<img src="{{ site.logo | relative_url }}" alt="AI at Work" />
	<div>
		<h1>AI Projects</h1>
		<p>
			This page showcases my AI projects, including architecture, tools, and implementation details.
		</p>
	</div>
</section>

<section class="projects-list">
	<article class="project-row">
		<div class="project-left">
			<h2>Neutrino Assistant</h2>
			<p>
				Neutrino is a nutrition assistant based on <strong>RAG</strong>,
				<strong>reflection</strong> and the <strong>langgraph</strong> agentic framework. The
				assistant generates responses by taking <strong>historical</strong> interactions into
				account and asks <strong>clarifications</strong> when needed. It leverages an agentic
				<strong>RAG</strong> tool for generating accurate <strong>content</strong>.
			</p>

			<div class="project-shot">
				<img src="{{ '/assets/img/neutrino-chatbot-screenshot.png' | relative_url }}" alt="Neutrino chatbot screenshot" onerror="this.style.display='none'" />
			</div>

			<div class="project-links">
				<a href="http://52.140.124.205:4200/home" target="_blank" rel="noopener noreferrer">SpringBoot Solution</a>
			</div>
		</div>

		<div class="project-right">
			<p>
				The <strong>Presentation layer</strong> is based Angular
				to capture user input and render responses while connecting to Spring Boot based Backend REST API layer. 

                The <strong>RAG engine layer</strong> combines HyPE technique, React agent, Open API to coordinate retrieval and answer generation workflows.                              

			</p>

			<h3>RAG Tool</h3>
			<ul>
				<li>
					Generates hypothetical questions based on HyPE technique from the user query and retrieves <strong>context</strong> from the <strong>vector store</strong>.
				</li>
				<li>
					Sends the user query, retrieved context to the <strong>LLM</strong> for response generation.
				</li>
				<li>
					Calculates groundedness and precision <strong>scores</strong> of the response. Repeats the process up to a predefined <strong>max</strong> iteration count when scores are low.
				</li>
			</ul>   


			<div class="arch-diagram arch-diagram-compact">
				<div class="arch-layer">Angular</div>
				<div class="arch-layer">Spring Boot</div>
				<div class="arch-layer">RAG - LangGraph&nbsp;·&nbsp;HyPE &nbsp;·&nbsp; Open API &nbsp;·&nbsp; React</div>
				<div class="arch-layer">Vector Database - Chroma DB</div>
			</div>
		
            <p>
                LamaParse has been used as part of chunking strategy to generated semantic chunks and ingest the resulting embeddings into  Chroma DB. LLM has been used to generate HyPE questions.
            </p>
        </div>
        
	</article>

	<article class="project-row project-row-architecture-right">
		<div class="project-left">
			<h3>Architecture</h3>
			<div class="arch-diagram">
				<div class="arch-layer">React / Web Chat</div>
				<div class="arch-layer">RASA NLU</div>
				<div class="arch-layer">RASA Core</div>
				<div class="arch-layer">OTP Auth &nbsp;·&nbsp; Session Management</div>
				<div class="arch-layer">Custom Actions API &nbsp;·&nbsp; Appointment DB</div>
			</div>

			<div class="project-shot" style="margin-top:0.9rem;">
				<img src="{{ '/assets/img/appointment-bot-screenshot.png' | relative_url }}" alt="Appointment Bot screenshot" onerror="this.style.display='none'" />
			</div>
		</div>

		<div class="project-right">
			<h2 style="margin-top:0;">RASA Appointment Bot</h2>
			<p>
				A conversational appointment management assistant built with <strong>RASAPRO</strong>. Users
				 authenticate via <strong>OTP</strong>, view their profile, browse available doctors,
				and book, view, or cancel appointments — all through a natural language interface.
			</p>

			<h3>Key Features</h3>
			<ul>
				<li>OTP-based email authentication with session management.</li>
                <li>Configurable dialog flows which guide user's converation</li>
				<li>RAG based search for doctor speciality
                <li>MCP server to integrate with external system for appointment booking with available doctors by specialty.</li>
				<li>Persistent session context across the conversation.</li>
			</ul>
		</div>
	</article>
</section>
