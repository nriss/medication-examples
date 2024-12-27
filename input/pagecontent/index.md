<p style="padding: 5px; border-radius: 5px; border: 2px solid maroon; background: #ffffe6; width: 65%">
<b>Brief description of this Implementation Guide</b><br>
[Add a brief description of this IG in English]
</p>

{% if site.data.info.releaselabel == 'ci-build' %}
<div style="width: 65%">
    <blockquote class="stu-note">
    <p>
    <b>Attention !</b> Cet Implementation Guide n'est pas en version courante. La version courante sera accessible via l'URL canonique suite à la première release : http://interop.esante.gouv.fr/ig/fhir/[code - ig]
    </p>
    </blockquote>
</div>
{% endif %}

<!--  A décommenter si CI-SIS
<div class="figure">
    <img src="ci-sis-logo.png" alt="CI-SIS" title="Logo du CI-SIS" style="width:100%;">
</div>
-->

### Introduction

L'objectif de ce guide est de contenir un ensemble d'exemples de prescriptions afin de voir si FHIR permet d'indiquer l'ensemble des types de prescription française.

L'objectif de ces travaux est de commencer dans un premier temps à modéliser les prescriptions les plus simples pour répondre à 90%+ des prescriptions, puis dans un second temps de se concentrer sur les precriptions complexes.

Les travaux vont commencer par la modélisation de la ligne de prescription, la prescription multi-ligne sera travaillée dans un second temps au niveau de travaux plus larges : FHIR Document, groupIdentifier, RequestGroup, ...

Ces travaux s'appuieront et seront en corrélation avec le guide d'implémentation développé par InteropSanté https://github.com/Interop-Sante/hl7.fhir.fr.medication.

### Expression de la quantité prescrite

1-A/ En nombre d'unité de présentation (ex. comprimé)

1-B/ En quantité massique (500 mg)

1-C/ En quantité volumique (5 ml)

1-D/ en quantité calculée par rapport au poids corporel de façon explicite

1-E/ En quantité rapportée au poids corporel (par ex. 50 mg / kg)

1-F/ Par fourchette (1 à 2 comprimés)

1-G/ Par quantité variable (doses progressives, doses dégressives et doses en alternance)

1-H/ Par quantité variable par rapport à d'autres paramètres (en fonction d'une échelle de la douleur pour les antalgiques)

1-I/ En termes indeterminés (par ex, appliquer une fine pellicule, utiliser une quantité de la taille d'un petit pois)

### Moment de prise et fréquence

2-A/ Par un intervalle de temps entre deux prises ? (exemple contramal 50mg toutes les 6h)

2-B/ par un moment de prise spécifique horaire (exemple : à 22h)

2-C/ De façon relative avec d'autres événements (après le repas)

2-D/ Par précision d'une date spécifique (à débuter le 20 janvier)

2-E/ Par précision d'une date relative (exemple : au 1er jour des règles)

2-F/ Par une fréquence journalière (exemple : 3x par jour)

2-G/ Par une fréquence non journalière (hebdo, mensuelle, annuelle, ...)

### Dépendances

{% include dependency-table.xhtml %}

### Propriété intellectuelle

{% include ip-statements.xhtml %}
