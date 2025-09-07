<script>
	import Accordion from './common/Accordion.svelte';
	const items = [
		{
			q: '¿IQ Option México es gratis?',
			a: 'Sí. Abrir una cuenta y usar la versión demo de IQ Option es completamente gratis. Puedes explorar la plataforma, practicar con USD $10,000 en fondos virtuales y probar estrategias sin depositar dinero real. Pero para hacer trading real necesitarás hacer un depósito mínimo de USD $10.'
		},
		{
			q: '¿IQ Option México es legal?',
			a: 'Sí. Los residentes en México pueden hacer trading en IQ Option sin restricciones legales. Los traders en México también deben conocer los requisitos fiscales y de reporte locales sobre ganancias de trading.'
		},
		{
			q: '¿IQ Option es una estafa?',
			a: 'No. IQ Option opera desde 2013, tiene millones de usuarios registrados en todo el mundo y está regulado para sus operaciones en la UE por la CySEC. IQ Option sigue medidas estrictas de seguridad operativa y financiera, incluyendo cifrado SSL y cuentas de clientes segregadas.'
		},
		{
			q: '¿Se puede confiar en IQ Option?',
			a: 'Sí. IQ Option ha construido una reputación por su confiabilidad, condiciones de trading transparentes y procesamiento seguro de pagos. Los fondos se mantienen en cuentas segregadas, y la plataforma ofrece términos y políticas claras, lo que la convierte en una opción confiable para muchos traders en México.'
		},
		{
			q: '¿IQ Option es seguro?',
			a: 'Sí. IQ Option usa cifrado SSL para proteger los datos personales y financieros, mantiene los fondos de clientes separados del capital de la empresa y ofrece autenticación de dos factores (2FA) para mayor seguridad de tu cuenta.'
		},
		{
			q: '¿IQ Option México e IQ Broker son la misma empresa?',
			a: 'Sí. IQ Broker es la marca matriz bajo la cual opera la plataforma IQ Option. Los nombres a veces se usan de forma intercambiable, pero se refieren al mismo servicio de trading.'
		}
	];
</script>

<section>
	<h2>Preguntas frecuentes</h2>

	{#each items as item, idx}
		{#if idx === 0}
			<Accordion open {item} />{:else}<Accordion {item} />{/if}
	{/each}
</section>
