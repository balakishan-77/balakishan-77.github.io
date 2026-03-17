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
				Neutrino is a <strong>RAG</strong> based <strong>Agentic</strong> AI system which provides nutrition assistance and generates responses by taking <strong>historical</strong> interactions into
				account. The system asks for <strong>clarifications</strong> when needed. 
			</p>

			<div class="project-shot">
				<img src="{{ '/assets/img/neutrino-chatbot-screenshot.png' | relative_url }}" alt="Neutrino chatbot screenshot" onerror="this.style.display='none'" />
			</div>
            <h4>AI Techniques</h4>
            <p>
                <strong>RAG</strong> technique along with <strong>React</strong> technique and <strong>Semantic Chunking</strong> for generating accurate and relevant <strong>content</strong>.
            </p>
			<div class="project-links">
            Hosted Link: 
				<a href="http://52.140.124.205:4200/home" target="_blank" rel="noopener noreferrer">SpringBoot Solution</a>
			</div>
		</div>

		<div class="project-right">
            <h4>Key Metrics</h4>             
            <p>
                Groundedness score, precision <strong>score</strong> to validate response.  
            </p>               
            <h4>Chunking Strategy</h4>
            <p>
            LamaParse is used to generate chunks as part of chunking strategy.
            </p>        
			<h4>RAG Flow</h4>
			<ul>
				<li>
					For a given user query, the system generates HyPE questions. It uses these questions to identify relevant <strong>context</strong> from the <strong>vector store</strong>.
				</li>
				<li>
					The system sends the user query along with retrieved context to Open AI <strong>LLM</strong> for response generation.
				</li>
			</ul>  

			<h4>Arch Overview</h4>

            <div class="arch-diagram arch-diagram-compact">
                <div class="arch-layer">Angular</div>
                <div class="arch-layer">Spring Boot</div>
                <div class="arch-layer">RAG Layer - LangGraph&nbsp;·&nbsp;HyPE &nbsp;·&nbsp; Open API &nbsp;·&nbsp; React</div>
                <div class="arch-layer">Chroma Vector DB</div>
            </div>

            <p>
                The <strong>RAG layer</strong> combines Prompt Engineering, RAG, HyPE technique, React, Open API, and LangGraph Orchestration framework which coordinates retrieval and answer generation. 
            </p>  


  
        </div>
        
	</article>

	<article class="project-row">
		<div class="project-left">
			<h2>RASA Appointment Bot</h2>
			<p>
				A conversational appointment management assistant built with <strong>RASAPRO</strong>. 
			</p>
            Users authenticate via <strong>OTP</strong>, view their profile, browse available doctors,
			and book, view, or cancel appointments through a natural language interface.

			<div class="project-shot" style="margin-top:0.9rem;">
				<img src="{{ '/assets/img/appointment-bot-screenshot.png' | relative_url }}" alt="Appointment Bot screenshot" onerror="this.style.display='none'" />
			</div>
		</div>

		<div class="project-right">
			<h4>Key Features</h4>
			<ul>
				<li>OTP-based email authentication with session management.</li>
				<li>Configurable dialog flows that guide user conversations.</li>
				<li>RAG-based search for doctor specialties.</li>
                <li>MCP server to integrate with external system for appointment booking with available doctors by specialty.</li>
				<li>Persistent session context across the conversation.</li>
			</ul>

			<h4>Architecture Overview</h4>
			<div class="arch-diagram arch-diagram-compact">
				<div class="arch-layer">StreamLit</div>
				<div class="arch-layer">RASA Server</div>
				<div class="arch-layer">RASA PRO (CALM)</div>
                <div class="arch-layer">Custom Actions &nbsp;·&nbsp; OTP Auth &nbsp;·&nbsp;Session Management</div>
				<div class="arch-layer">MCP Server &nbsp;·&nbsp; API Integration</div>
                <div class="arch-layer">MCP Server &nbsp;·&nbsp; RAG Search</div>
			</div>
		</div>
	</article>
</section>
