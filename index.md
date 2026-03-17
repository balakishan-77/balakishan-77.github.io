---
layout: default
---

<style>
	.ai-projects-banner {
		margin: 0 0 1.5rem;
		padding: 1.2rem 1.4rem;
		border-left: 6px solid #2f79b7;
		background: linear-gradient(120deg, #eef6fc 0%, #f7fbff 100%);
		border-radius: 8px;
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
		.project-row {
			min-height: auto;
			grid-template-columns: 1fr;
		}
	}
</style>

<section class="ai-projects-banner">
	<h1>AI Projects</h1>
	<p>
		This page showcases my AI projects, including architecture, tools, and implementation details.
	</p>
</section>

<section class="projects-list">
	<article class="project-row">
		<div class="project-left">
			<h2>Neutrino</h2>
			<p>
				Neutrino is a nutrition assistant based on <strong>RAG</strong>,
				<strong>reflection</strong> and the <strong>langgraph</strong> agentic framework.
			</p>

			<h3>Assistant</h3>
			<p>
				The assistant generates responses by taking <strong>historical</strong> interactions
				into account and asks <strong>clarifications</strong> when needed. It leverages an
				agentic <strong>RAG</strong> tool for generating accurate <strong>content</strong>.
			</p>

			<div class="project-links">
				<a href="https://huggingface.co/spaces/balakishan77/hf">Hugging Face Space</a>
				<a href="http://52.140.124.205:4200/home">SpringBoot Solution</a>
			</div>
		</div>

		<div class="project-right">
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
