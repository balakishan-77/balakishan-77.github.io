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

	.arch-row {
		display: grid;
		grid-template-columns: 1fr auto 1fr;
		align-items: center;
		gap: 0.5rem;
		margin-bottom: 0.45rem;
	}

	.arch-row:last-child {
		margin-bottom: 0;
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

	.arch-arrow {
		font-size: 0.88rem;
		color: #507694;
		font-weight: 700;
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

			<div class="project-links">
				<a href="http://52.140.124.205:4200/home">SpringBoot Solution</a>
			</div>
		</div>

		<div class="project-right">
			<h3>Architecture</h3>
			<div class="arch-diagram">
				<div class="arch-row">
					<div class="arch-node">Angular</div>
					<div class="arch-arrow">--&gt;</div>
					<div class="arch-node">SpringBoot API</div>
				</div>
				<div class="arch-row">
					<div class="arch-node">SpringBoot API</div>
					<div class="arch-arrow">--&gt;</div>
					<div class="arch-node">HyPE</div>
				</div>
				<div class="arch-row">
					<div class="arch-node">HyPE</div>
					<div class="arch-arrow">--&gt;</div>
					<div class="arch-node">RAG Engine</div>
				</div>
				<div class="arch-row">
					<div class="arch-node">LangGraph Orchestration</div>
					<div class="arch-arrow">--&gt;</div>
					<div class="arch-node">RAG Engine</div>
				</div>
				<div class="arch-row">
					<div class="arch-node">RAG Engine</div>
					<div class="arch-arrow">--&gt;</div>
					<div class="arch-node">Vector DB</div>
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

			<h3 style="margin-top: 0.9rem;">Porting The Solution</h3>
			<ul>
				<li>This architecture is not coupled to Python or Streamlit.</li>
				<li>The solution has been ported to SpringBoot and Angular.</li>
				<li><strong>SpringBoot</strong> takes the place of Python and leverages langgraph4j.</li>
				<li><strong>Angular</strong> takes the place of Streamlit.</li>
				<li>This can also be implemented in technologies like <strong>Golang</strong> where langgraph is supported.</li>
			</ul>
		</div>
	</article>
</section>
