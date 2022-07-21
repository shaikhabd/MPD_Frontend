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
		} else if (selected == 4) {
			goto('/searchte/' + SearchValue);
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
					<option value="4">Therapeutic </option>
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
						<option value="Hyoscine_or_Scopolamine">Hyoscine_or_Scopolamine</option>
						<option value="Hyoscyamine">Hyoscyamine </option>
						<option value="Micotianamine">Micotianamine </option>
						<option
							value="Atropine
						"
							>Atropine
						</option>
						<option value="Oleic acid">Oleic acid</option>
						<option
							value="Daturilin
						"
							>Daturilin
						</option>
						<option
							value="β-sitosterol
						"
							>β-sitosterol
						</option>
						<option
							value="Daturaolone
						"
							>Daturaolone
						</option>
						<option
							value="Daturadiol
						"
							>Daturadiol
						</option>
						<option
							value="Hyosane
						"
							>Hyosane
						</option>
						<option
							value="Fastusic acid
						"
							>Fastusic acid
						</option>
						<option
							value="Fastusine
						"
							>Fastusine
						</option>
						<option
							value="Fastusinine
						"
							>Fastusinine
						</option>
						<option
							value="Fastunine
						"
							>Fastunine
						</option>
						<option
							value="Fastudine
						"
							>Fastudine
						</option>
						<option
							value="Daluranlone
						"
							>Daluranlone
						</option>
						<option
							value="Citrostadienol
						"
							>Citrostadienol
						</option>
						<option
							value="Obtusifoliol
						"
							>Obtusifoliol
						</option>
						<option
							value="Allantoin
						"
							>Allantoin
						</option>
						<option value="Linoleic acid">Linoleic acid</option>
						<option value="Datumetine">Datumetine</option>
						<option value="Vitamin C">Vitamin C</option>
						<option value="Chlorogenic acid">Chlorogenic acid</option>
						<option value="β-Me-sterols">β-Me-sterols</option>
						<option value="Tigloidine">Tigloidine</option>
						<option
							value="Apohyoscine
						"
							>Apohyoscine
						</option>
						<option
							value="3α-tigloyloxytropane
						"
							>3α-tigloyloxytropane
						</option>
						<option
							value="Norhyoscine
						"
							>Norhyoscine
						</option>
						<option
							value="Norhyocyamine
						"
							>Norhyocyamine
						</option>
						<option
							value="Meteloidine
						"
							>Meteloidine
						</option>
						<option
							value="Cuscohygrine
						"
							>Cuscohygrine
						</option>
						<option
							value="Tropine
						"
							>Tropine
						</option>
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
				{#if selected == 4}
					<select
						bind:value={SearchValue}
						style="margin-right:2%; width:40%;font-weight: 600;"
						class="form-select size"
						aria-label="Default select example"
					>
						<option value="Anticholinergic, Antiemetic, Antivertigo" selected
							>Anticholinergic, Antiemetic, Antivertigo</option
						>
						<option value="Antimuscarinic">Antimuscarinic</option>
						<option value="Anti-inflammatory">Anti-inflammatory</option>
						<option value="Anticancer"> Anticancer</option>
						<option value="Cardioprotective"> Cardioprotective </option>
						<option value="Neuroprotective"> Neuroprotective</option>
						<option value="Prebiotic"> Prebiotic </option>
						<option value="Analgesic"> Analgesic </option>
						<option value="Anti-tumor"> Anti-tumor</option>
						<option value="Antiallergic"> Antiallergic </option>
						<option value="Antiangiogeni"> Antiangiogeni</option>
						<option value="Anti-arthritic">Anti-arthritic </option>
						<option value="Antiasthmatic"> Antiasthmatic</option>
						<option value="Antibacterial"> Antibacterial</option>
						<option value="Anticholinergic"> Anticholinergic</option>
						<option value="Anticholinergics"> Anticholinergics</option>
						<option value="Anticholinesterase"> Anticholinesterase</option>
						<option value="Anticolic"> Anticolic</option>
						<option value="Anti-diabetic"> Anti-diabetic</option>
						<option value="Anti-dyslipidemic"> Anti-dyslipidemic</option>
						<option value="Antiemetic"> Antiemetic</option>
						<option value="Anti-epileptic"> Anti-epileptic</option>
						<option value="Antifungal"> Antifungal</option>
						<option value="Anti-genotoxic"> Anti-genotoxic</option>
						<option value="Antigiardia"> Antigiardia</option>
						<option value="Antiglaucoma"> Antiglaucoma</option>
						<option value="Anti-hepatotoxic"> Anti-hepatotoxic</option>
						<option value="Antihistamine"> Antihistamine</option>
						<option value="Antihyperalgesi"> Antihyperalgesi</option>
						<option value="Anti-hyperglycemic"> Anti-hyperglycemic</option>
						<option value="Antihyperlipidemic"> Antihyperlipidemic</option>
						<option value="Anti-hypoxia"> Anti-hypoxia</option>
						<option value="Anti-inflammatory"> Anti-inflammatory</option>
						<option value="Antimalarial"> Antimalarial</option>
						<option value="Antimicrobial"> Antimicrobial</option>
						<option value="Antimuscarinic"> Antimuscarinic</option>
						<option value="Antineoplastic"> Antineoplastic</option>
						<option value="Antinociceptive"> Antinociceptive</option>
						<option value="Anti-obesity"> Anti-obesity</option>
						<option value="Antioxidant"> Antioxidant</option>
						<option value="Antiproleferative"> Antiproleferative</option>
						<option value="Antiprotozoal"> Antiprotozoal</option>
						<option value="Antipyretic"> Antipyretic</option>
						<option value="Antiseptic"> Antiseptic</option>
						<option value="Antispasmodic">Antispasmodic </option>
						<option value="Anti-thrombotic"> Anti-thrombotic</option>
						<option value="Antivertigo"> Antivertigo</option>
						<option value="Antiviral"> Antiviral</option>
						<option value="Cardiovascular-protective"> Cardiovascular-protective</option>
						<option value="Hepatoprotective"> Hepatoprotective</option>
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
