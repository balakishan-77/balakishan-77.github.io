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

	.arch-layer {
		display: grid;
		grid-template-columns: 130px 1fr;
		gap: 0.55rem;
		align-items: center;
		margin-bottom: 0.5rem;
	}

	.arch-layer:last-child {
		margin-bottom: 0;
	}

	.arch-label {
		font-size: 0.79rem;
		font-weight: 700;
		color: #315974;
		text-transform: uppercase;
		letter-spacing: 0.03em;
	}

	.arch-node {
		padding: 0.32rem 0.48rem;
		border: 1px solid #b9d2e7;
		border-radius: 6px;
		background: #ffffff;
		color: #16334b;
		font-size: 0.9rem;
		font-weight: 600;
		text-align: center;
	}

	.arch-node-main {
		background: #edf6ff;
	}

	.arch-node-sub {
		margin-top: 0.32rem;
		font-size: 0.83rem;
		font-weight: 600;
		color: #315974;
		text-align: center;
	}

	@media (max-width: 1100px) {
		.arch-layer {
			grid-template-columns: 1fr;
			gap: 0.3rem;
		}

		.arch-label {
			font-size: 0.75rem;
		}
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

	.project-row-reversed {
		grid-template-columns: 1fr 1fr;
	}

	.project-row-reversed .project-left {
		order: 1;
	}

	.project-row-reversed .project-right {
		order: 0;
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
			<h3>Architecture</h3>
			<div class="arch-diagram">
				<div class="arch-layer">
					<div class="arch-label">Layer 1: UI</div>
					<div class="arch-node arch-node-main">Angular</div>
				</div>
				<div class="arch-layer">
					<div class="arch-label">Layer 2: REST API</div>
					<div class="arch-node arch-node-main">Spring Boot</div>
				</div>
				<div class="arch-layer">
					<div class="arch-label">Layer 3: RAG Engine</div>
					<div>
						<div class="arch-node arch-node-main">LangGraph Orchestration</div>
						<div class="arch-node-sub">HyPE</div>
						<div class="arch-node-sub">Open API</div>
						<div class="arch-node-sub">React Agent</div>
					</div>
				</div>
				<div class="arch-layer">
					<div class="arch-label">Layer 4: Vector DB</div>
					<div class="arch-node arch-node-main">Chroma DB</div>
				</div>
			</div>

			<h3>RAG Tool</h3>
			<ul>
				<li>
					Generates hypothetical questions from the user query and retrieves
					<strong>context</strong> from a <strong>vector store</strong>.
				</li>
				<li>
					Sends the user query and retrieved context to the <strong>LLM</strong> for response generation.
				</li>
				<li>
					Calculates groundedness and precision <strong>scores</strong> for the response.
				</li>
				<li>
					Repeats the process up to a predefined <strong>max</strong> iteration count when scores are low.
				</li>
				<li>
					Uses langgraph for <strong>reflective</strong> agent execution to improve response quality.
				</li>
			</ul>

			<h3 style="margin-top: 0.9rem;">Architecture Description</h3>
			<p>
				The architecture is organized in four layers. The <strong>UI layer</strong> uses Angular
				to capture user input and render responses. The <strong>REST API layer</strong> uses Spring
				Boot to handle requests and orchestrate backend processing. The <strong>RAG engine layer</strong>
				combines LangGraph orchestration, HyPE, Open API, and a React agent to coordinate retrieval
				and answer generation workflows. The <strong>Vector DB layer</strong> uses Chroma DB to store
				and retrieve semantic context for grounding responses.
			</p>
		</div>
	</article>

	<article class="project-row project-row-reversed">
		<div class="project-left">
			<h3>Architecture</h3>
			<div class="arch-diagram">
				<div class="arch-layer">
					<div class="arch-label">Layer 1: UI</div>
					<div class="arch-node arch-node-main">React / Web Chat</div>
				</div>
				<div class="arch-layer">
					<div class="arch-label">Layer 2: NLU</div>
					<div class="arch-node arch-node-main">RASA NLU</div>
				</div>
				<div class="arch-layer">
					<div class="arch-label">Layer 3: Dialogue</div>
					<div>
						<div class="arch-node arch-node-main">RASA Core</div>
						<div class="arch-node-sub">OTP Auth</div>
						<div class="arch-node-sub">Session Management</div>
					</div>
				</div>
				<div class="arch-layer">
					<div class="arch-label">Layer 4: Backend</div>
					<div>
						<div class="arch-node arch-node-main">Custom Actions API</div>
						<div class="arch-node-sub">Appointment DB</div>
					</div>
				</div>
			</div>

			<div class="project-shot" style="margin-top:0.9rem;">
				<img src="{{ '/assets/img/appointment-bot-screenshot.png' | relative_url }}" alt="Appointment Bot screenshot" onerror="this.style.display='none'" />
			</div>
		</div>

		<div class="project-right">
			<h2 style="margin-top:0;">RASA Appointment Bot</h2>
			<p>
				A conversational appointment management assistant built with <strong>RASA</strong>. Users
				can authenticate via <strong>OTP</strong>, view their profile, browse available doctors,
				and book, view, or cancel appointments — all through a natural language interface.
			</p>

			<h3>Key Features</h3>
			<ul>
				<li>OTP-based email authentication with session management.</li>
				<li>Books appointments with available doctors by specialty.</li>
				<li>View and cancel existing appointments.</li>
				<li>Quick command shortcuts for common actions.</li>
				<li>Persistent session context across the conversation.</li>
			</ul>
		</div>
	</article>
</section>
