<script lang="ts">
	import rebstock from './rebstock.jpg';
	import schusterjunge from './schusterjunge.avif';
	import linde from './linde.jpg';
	import waldulm from './rebstock-waldulm.jpg';
	import faxe from './faxe.jpg';
	import williams from './williams.jpg';
	import prinzen from './prinzen.jpeg';
	import perle from './perle.jpg';
	import spinner from './spinner.jpg';
	import mighty2 from './mighty2.jpg';
	import graessel from './graessel.avif';
	import sonne from './sonne.jpg';
	import jaeger from './jaeger.webp';
    import leben from './leben.jpeg';
	import heimat from './heimat.jpg';
	import baeuerlehof from 'baeuerlehof.jpg'; 


	interface Stay {
		name: string;
		description: string;
		image: string;
		link: string;
		address: string;
		position: number[];
	}

	const stays: Stay[] = [
		{
			name: 'Landgasthof Rebstock',
			description:
				'Wir nehmen uns gerne Zeit für Sie und wünschen Ihnen eine genussvolle Zeit hier bei uns im Rebstock in Furschenbach.',
			image: rebstock,
			link: 'https://www.landgasthofrebstock.de/',
			address: 'Dorfstraße 1, 77883 Ottenhöfen im Schwarzwald',
			position: [48.5795887, 8.1330446]
		},
		{
			name: 'Schusterjunge',
			description: 'Ferien & Business Apartments für Urlauber:innen und Geschäftsreisende.',
			image: schusterjunge,
			link: 'https://www.schusterjunge-aparthotel.de/',
			address: 'Im Winkel 1, 77887 Sasbachwalden',
			position: [48.6183827, 8.1224028]
		},
		{
			name: 'Gasthaus Linde Oberachern',
			description: 'Hereinkommen, wohlfühlen und mit Freude im Herzen wieder den Nachhauseweg antreten.',
			image: linde,
			link: 'http://www.lindeoberachern.de/',
			address: 'Johannesstrasse 11, 77855 Achern',
			position: [48.6162396,8.081512]
		},
		{
			name: 'Rebstock Waldulm',
			description: 'Komfortabel und detailverliebt ausgestattet, laden unsere Gästezimmer dazu ein loszulassen, den Moment zu genießen und Kraft zu schöpfen.',
			image: waldulm,
			link: 'https://rebstock-waldulm.de/',
			address: 'Kutzendorf 1, 77876 Kappelrodeck',
			position: [48.5816702,8.1024251]
		},
		{
			name: 'Hotel "Faxe" Schwarzwälder Hof',
			description: 'Geniessen Sie Ihren Urlaub in einer der schönsten Regionen Deutschlands, verwöhnt vom hervorragendem Klima des Rheingrabens - der "Toscana Deutschlands" - und doch schon im Schwarzwald.',
			image: faxe,
			link: 'http://www.faxehof.de/',
			address: 'Weinstraße 79, 77876 Kappelrodeck',
			position: [48.5850432,8.1004391]
		},
		{
			name: 'Pension Williams',
			description: 'Relax, Hike, Explore and More...',
			image: williams,
			link: 'http://www.pension-williams.com/contact_us.html',
			address: 'Schützenhausstraße 4, 77889 Seebach',
			position: [48.5797902,8.1768849]
		},
		{
			name: 'Prinzen Hotel',
			description: 'Gastfreundschaft besteht aus ein wenig Wärme, ein wenig Nahrung und großer Ruhe.',
			image: prinzen,
			link: 'http://www.zumprinzen.de/',
			address: 'Hauptstraße 86, 77876 Kappelrodeck',
			position: [48.5906497,8.1153226]
		},
		{
			name: 'Berghotel Schwarzwaldperle',
			description: 'Unser Berghotel liegt auf 700 Meter über Meereshöhe in Sasbachwalden im Ortsteil Brandmatt und bietet ein unbeschreibliches Panorama über die Rheinebene bis zu den Vogesen in Frankreich.',
			image: perle,
			link: 'http://hotel-schwarzwaldperle.de/',
			address: 'Brandmatt 18, 77887 Sasbachwalden',
			position: [48.6140251,8.1614526]
		},
		{
			name: 'Hotel Restaurant Spinnerhof',
			description: 'Hoch über dem beliebten Blumen- und Weindorf Sasbachwalden liegt unser Spinnerhof,',
			image: spinner,
			link: 'http://spinnerhof.de/',
			address: 'Am Schloßberg 8, 77887 Sasbachwalden',
			position: [48.6151052,8.140559]
		},
		{
			name: 'mightyTwice Hotel Achern',
			description: 'Ausgefallenes Design-Hotel im badischen Achern – inkl. Frühstück, Begrüßungsgetränk & spätem-Check-out',
			image: mighty2,
			link: 'https://www.twicehotels.de/achern',
			address: 'Illenauer Str. 49, 77855 Achern',
			position: [48.6253106,8.0780627]
		},
		{
			name: 'Gasthaus zur Grässelmühle',
			description: 'Die Grässelmühle ist ein Hotel und Restaurant im schönen Schwarzwald. Tradition und familiäre Warmherzigkeit spielen hier eine sehr große Rolle.',
			image: graessel,
			link: 'http://www.graesselmuehle.de/',
			address: 'Sasbachwaldener Str. 64, 77880 Sasbach',
			position: [48.6246516,8.1018583]
		},
		{
			name: 'Hotel Sonne Eintracht',
			description: 'Entdecken Sie den Zauber der "Sonne Eintracht" in Achern, wo herzliche Gastfreundschaft auf zeitlose Tradition trifft.',
			image: sonne,
			link: 'http://www.hotel-sonne-eintracht.com/',
			address: 'Hauptstraße 112, 77855 Achern',
			position: [48.6290961,8.0745853]
		},
		{
			name: 'Jägerhof',
			description: 'Schöne, familienfreundliche Apartments direkt neben dem Lebenshof Mut im Bauch.',
			image: jaeger,
			link: 'https://benzottenhoefen.wixsite.com/jaegerhof-benz',
			address: 'Am Bach 16, 77883 Ottenhöfen im Schwarzwald',
			position: [48.5836123,8.1461086]
		},
		{
			name: 'Ferienwohnung Schwarzwaldleben',
			description: 'Die Ferienwohnung Schwarzwald(l)eben begrüßt euch in ruhiger Ortsrandlage im Mummelseedorf Seebach mitten im Nationalpark Schwarzwald.',
			image: leben,
			link: 'https://www.schwarzwaldleben.com/',
			address: 'Waldstraße 16C, 77889 Seebach',
			position: [48.5810177,8.1773364]
		},
		{
			name: 'Pension Heimat',
			description: 'Bei uns beginnt der Urlaub direkt nach der Ankunft: Ankommen und Entspannen.',
			image: heimat,
			link: 'http://www.pension-heimat.de/',
			address: 'Ruhesteinstraße 27, 77883 Ottenhöfen im Schwarzwald',
			position: [48.5711844,8.1417912]
		},
		{
			name: 'Bäuerlehof',
			description: 'Unser Haus liegt an einem sonnigen Südhang auf der Sommerseite Seebachs. Abseits jeglicher Alltagshektik genießen Sie bei uns erholsame und schöne Ferientage in einer familiären Atmosphäre.',
			image: baeuerlehof,
			link: 'http://www.baeuerlehof.de/',
			address: 'Sommerseite 55, 77889 Seebach',
			position: [48.5792004,8.1886692]
		}
	];
</script>

<div class="mx-auto max-w-4xl">
	<div class="mb-24 text-center">
		<h1 class="mb-4 text-4xl md:text-6xl">Übernachtungsmöglichkeiten</h1>
		<p class="text-3xl md:text-5xl">in der Umgebung</p>
	</div>

	<p class="text-center text-4xl">Map</p>

	<div class="mb-24 grid gap-6 p-6 text-center text-3xl md:grid-cols-3 md:text-5xl">
		{#each stays as stay}
			<div class="max-w-sm overflow-hidden rounded shadow-lg">
				<img class="w-full" src={stay.image} alt={stay.name} />
				<div class="px-6 py-4">
					<div class="mb-2 text-xl font-bold">{stay.name}</div>
					<p class="text-base text-gray-700">
						{stay.description}
					</p>
				</div>
				<div class="px-6 pb-2 pt-4">
					<a
						class="mb-2 mr-2 inline-block rounded-full bg-gray-300 px-3 py-1 text-sm font-semibold text-gray-700 hover:bg-gray-400"
						href={stay.link}
						target="_blank"
						rel="noopener noreferrer">Zur Website</a
					>
				</div>
			</div>
		{/each}
	</div>
</div>
