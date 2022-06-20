<script>
	import { goto } from '$app/navigation';
	let SearchValue;
	let selected;
	function submitSearch() {
		if (selected == 0) {
			goto('/search/' + SearchValue);
		} else if (selected == 1) {
			goto('/searchcn/' + SearchValue);
		} else if (selected == 2) {
			goto('/searchtg/' + SearchValue);
		} else if (selected == 3) {
			goto('/searchtp/' + SearchValue);
		}
	}
	let example = [
		'e.g.Amla, Dhatura, Bhangra',
		'e.g.Hyoscyamine, Daucosterol, Verazine, Linoleic acid, Oleic acid, Datumetelin',
		'e.g. cholinergic receptor muscarinic 4, adenylate cyclase 1, cholinergic receptor muscarinic 1',
		'e.g. Muscarinic acetylcholine receptor M1, Muscarinic acetylcholine receptor M2, Muscarinic acetylcholine receptor M4'
	];
</script>

<section id="sb" class="hero color is-halfheight">
	<div class="maindiv">
		<div class="align">
			<p style="color:#4caae7;" class="title">Search Plant Information:</p>
		</div>
		<br />
		<div>
			<form on:submit={submitSearch} class="align2">
				<select
					bind:value={selected}
					style="margin-right:2%; width:40%;font-weight: 600;"
					class="form-select size"
					aria-label="Default select example"
				>
					<option value="0" selected>Plant Name</option>
					<option value="1">Chemical Compound </option>
					<option value="2">Target Gene </option>
					<option value="3">Target Protein </option>
				</select>
				{#if selected == 0}
					<select
						bind:value={SearchValue}
						style="margin-right:2%; width:40%;font-weight: 600;"
						class="form-select size"
						aria-label="Default select example"
					>
						<option value="Dhatura" selected>Dhatura</option>
						<option value="Bhangra">Bhangra </option>
						<option value="Amla">Amla</option>
						<option value="Harshingar">Harshingar</option>
						<option value="Ratanjyot">Ratanjyot</option>
						<option value="Bael">Bael</option>
						<option value="Chaste Tree">Chaste Tree</option>
					</select>
				{/if}
				{#if selected == 1}
					<select
						bind:value={SearchValue}
						style="margin-right:2%; width:40%;font-weight: 600;"
						class="form-select size"
						aria-label="Default select example"
					>
						<option value="Hyoscyamine">Hyoscyamine</option>
						<option value="Daucosterol">Daucosterol</option>
						<option value="Verazine">Verazine</option>
						<option value="Linoleic acid">Linoleic acid</option>
						<option value="Oleic acid">Oleic acid</option>
						<option value="Datumetelin">Datumetelin</option>
					</select>
				{/if}
				{#if selected == 2}
					<select
						bind:value={SearchValue}
						style="margin-right:2%; width:40%;font-weight: 600;"
						class="form-select size"
						aria-label="Default select example"
					>
						<option value="cholinergic receptor muscarinic 4" selected
							>cholinergic receptor muscarinic 4</option
						>
						<option value="cholinergic receptor muscarinic 1"
							>cholinergic receptor muscarinic 1
						</option>
						<option value="adenylate cyclase 1">adenylate cyclase 1</option>
					</select>
				{/if}
				{#if selected == 3}
					<select
						bind:value={SearchValue}
						style="margin-right:2%; width:40%;font-weight: 600;"
						class="form-select size"
						aria-label="Default select example"
					>
						<option value="Muscarinic acetylcholine receptor M1" selected
							>Muscarinic acetylcholine receptor M1</option
						>
						<option value="Muscarinic acetylcholine receptor M4"
							>Muscarinic acetylcholine receptor M4</option
						>
						<option value="Muscarinic acetylcholine receptor M2"
							>Muscarinic acetylcholine receptor M2</option
						>
					</select>
				{/if}
				<input
					bind:value={SearchValue}
					style="border-top-right-radius:0; border-bottom-right-radius:0;"
					class="input is-primary"
					type="text"
					placeholder="Enter your text here"
				/>
				<button style="border-top-left-radius:0; border-bottom-left-radius:0;" class="button green"
					>Search</button
				>
			</form>
			<h6 style="margin-left: 28%;" />
		</div>
	</div>
</section>

<style>
	.green {
		background-color: #22b36c;
		color: white;
	}
	.maindiv {
		padding: 2%;
	}
	.align {
		display: flex;
		justify-content: center;
	}
	.color {
		background-color: aliceblue;
	}
	.align2 {
		display: flex;
	}
	input:focus::placeholder {
		color: transparent;
	}
</style>
