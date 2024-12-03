<script>
	let message = 'Welcome to my SvelteKit page!';
</script>

<main>
	<h1>{message}</h1>
	<div class="content">
		<h2>Q1: How did you install SvelteKit?</h2>
		<p>
			To create this page, I used SvelteKit, a modern framework for building fast and scalable web
			apps. Here's how I installed it:
		</p>
		<pre><code>
1. Install Node.js:
   I installed Node.js from the official website: https://nodejs.org/ (version 18.0).

2. Create a new SvelteKit project:
   I ran the following command to create a new SvelteKit project:
   npm create svelte@latest partc

   I chose the "Skeleton project" template for minimal setup.

3. Install dependencies:
   I navigated into the project folder and installed the necessary dependencies:
   cd partc
   npm install

4. Run the development server:
   To start the local server, I ran:
   npm run dev

   The server was accessible at http://localhost:5173.
    </code></pre>

		<h2>Q2: How did you build the page?</h2>
		<p>
			The page was built by modifying the <code>src/routes/+page.svelte</code> file. Below is the structure
			of the page:
		</p>
		<pre><code>
&lt;script&gt;
  let message = "Welcome to my SvelteKit page!";
&lt;/script&gt;

&lt;style&gt;
  {'body {\n    background-color: #121212;\n     color: white;\n     margin: 0;\n     padding: 0; \n  }\n\
  h1 {\n     text-align: center;\n     margin-top: 50px;\n  }\n\
  p {\n     text-align: center;\n     font-size: 18px;\n  }\n\
  .content {\n     padding: 20px;\n     background-color: #333;\n     border-radius: 10px;\n     transition: background-color 0.3s ease;\n }\n\
  .content:hover {\n     background-color: #444; \n  }'}
&lt;/style&gt;

&lt;main&gt;
  &lt;h1&gt;{message}&lt;/h1&gt;
  &lt;div class="content"&gt;
    &lt;p&gt;Content goes here.&lt;/p&gt;
  &lt;/div&gt;
&lt;/main&gt;
    </code></pre>

		<h2>Q3: How does the dark theme and transitions work?</h2>
		<p>
			The page uses a dark theme for styling, with a smooth transition effect applied when the user
			hovers over the content section. The background color of the content changes to a lighter
			shade when hovered, providing an interactive feel.
		</p>

		<h2>Q4: What challenges did you encounter and how did you solve them?</h2>
		<h3>Development Server Not Accessible Remotely</h3>
		<p>
			The development server was initially accessible only on localhost. To fix this, I modified the
			<code>package.json</code>
			file to make it accessible on all network interfaces by running the server with the
			<code>--host</code> flag:
		</p>
		<pre><code>
     "scripts": {'{ "dev": "vite --host" }'}
    </code></pre>
	</div>
</main>

<style>
	h1,
	h2,
	h3 {
		text-align: center;
		margin-top: 50px;
	}
	p {
		text-align: center;
		font-size: 18px;
	}
	.content {
		padding: 20px;
		background-color: #333;
		border-radius: 10px;
		transition: background-color 0.3s ease;
	}
	.content:hover {
		background-color: #444;
	}
	pre {
		background-color: #1e1e1e;
		padding: 15px;
		border-radius: 5px;
		overflow-x: auto;
		color: #d4d4d4;
	}
	code {
		color: #d4d4d4;
	}
</style>
