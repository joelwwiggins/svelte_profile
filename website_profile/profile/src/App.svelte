<script>
	// GitHub repositories to showcase (only pinned repositories)
	const repositories = [
		{
			name: "math_game",
			description: "An interactive mathematics game designed to improve arithmetic skills through engaging challenges.",
			url: "https://github.com/joelwwiggins/math_game",
			skills: ["Python", "Game Development", "Education"]
		},
		{
			name: "big_data",
			description: "Analysis of large datasets using big data technologies and techniques.",
			url: "https://github.com/joelwwiggins/big_data",
			skills: ["Python", "Data Science", "Big Data"]
		},
		{
			name: "sql",
			description: "A collection of SQL scripts and database solutions for data management and analysis.",
			url: "https://github.com/joelwwiggins/sql",
			skills: ["SQL", "Database", "Data Analysis"]
		}
	];
</script>

<main>
	<header>
		<h1>Joel W. Wiggins</h1>
		<p class="subtitle">Data Simulation and Visualization Engineer</p>
	</header>
	
	<section class="about">
		<h2>About Me</h2>
		<p>
			I'm a chemical engineer with expertise in simulation with 1st priciples models, website deployment, 
			and machine learning. My portfolio showcases projects in deep learning , 
			application deployment, and scripting for work process improvment and profitability.
		</p>
	</section>
	
	<section class="projects">
		<h2>Featured Projects</h2>
		
		<div class="project-grid">
			{#each repositories as repo}
				<div class="project-card">
					<h3>{repo.name}</h3>
					<p>{repo.description}</p>
					<div class="skills">
						{#each repo.skills as skill}
							<span class="skill-tag">{skill}</span>
						{/each}
					</div>
					<a href={repo.url} target="_blank" rel="noopener noreferrer" class="view-project">View on GitHub</a>
				</div>
			{/each}
		</div>
	</section>
	
	<footer>
		<p>© {new Date().getFullYear()} Joel W. Wiggins • <a href="https://github.com/joelwwiggins" target="_blank">GitHub</a></p>
	</footer>
</main>

<style>
	:global(body) {
		background-color: #f9f9f9;
		font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
		line-height: 1.6;
		color: #333;
		margin: 0;
		padding: 0;
	}
	
	main {
		max-width: 1200px;
		margin: 0 auto;
		padding: 2rem;
	}
	
	header {
		text-align: center;
		margin-bottom: 3rem;
		padding: 2rem 0;
		border-bottom: 1px solid #eaeaea;
	}
	
	h1 {
		color: #333;
		font-size: 3rem;
		margin-bottom: 0.5rem;
		font-weight: 600;
	}
	
	.subtitle {
		font-size: 1.5rem;
		color: #555;
		margin-top: 0;
	}
	
	h2 {
		color: #444;
		font-size: 2rem;
		margin: 2rem 0 1rem;
		border-bottom: 2px solid #ff3e00;
		display: inline-block;
		padding-bottom: 0.5rem;
	}
	
	section {
		margin-bottom: 3rem;
	}
	
	.project-grid {
		display: grid;
		grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
		gap: 2rem;
	}
	
	.project-card {
		background-color: white;
		border-radius: 8px;
		box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
		padding: 1.5rem;
		transition: transform 0.3s ease, box-shadow 0.3s ease;
		height: 100%;
		display: flex;
		flex-direction: column;
	}
	
	.project-card:hover {
		transform: translateY(-5px);
		box-shadow: 0 10px 20px rgba(0, 0, 0, 0.12);
	}
	
	.project-card h3 {
		color: #ff3e00;
		margin-top: 0;
		font-size: 1.5rem;
	}
	
	.skills {
		display: flex;
		flex-wrap: wrap;
		margin: 1rem 0;
		gap: 0.5rem;
		margin-top: auto;
	}
	
	.skill-tag {
		background-color: #f1f1f1;
		color: #555;
		border-radius: 20px;
		padding: 0.3rem 0.8rem;
		font-size: 0.85rem;
		font-weight: 500;
	}
	
	.view-project {
		display: inline-block;
		background-color: #ff3e00;
		color: white;
		text-decoration: none;
		padding: 0.6rem 1.2rem;
		border-radius: 4px;
		font-weight: 500;
		margin-top: 1rem;
		transition: background-color 0.2s ease;
		text-align: center;
	}
	
	.view-project:hover {
		background-color: #e63600;
		text-decoration: none;
	}
	
	footer {
		text-align: center;
		margin-top: 3rem;
		padding-top: 2rem;
		border-top: 1px solid #eaeaea;
		color: #666;
	}
	
	footer a {
		color: #ff3e00;
		text-decoration: none;
	}
	
	footer a:hover {
		text-decoration: underline;
	}
	
	@media (max-width: 768px) {
		main {
			padding: 1rem;
		}
		
		.project-grid {
			grid-template-columns: 1fr;
		}
	}
</style>