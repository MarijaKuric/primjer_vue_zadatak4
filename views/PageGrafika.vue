<script>
export default {
    name: "PageGrafika"
}
</script>

<template>
  <div class="grow flex flex-col gap-4">
    <h1 class="text-indigo-100 text-2xl text-center font-medium mt-2">
      GRAFIKA
    </h1>

    <hr class="border-indigo-200/50 border rounded-full my-2" />

    <section class="grid grid-cols-2 items-center text-justify">
      <p>
        Za ovaj dio projekta izrađena je vektorska grafika. Koristit će se program Inkscape, 
        pomoću kojeg će se izraditi dizajn mačke, uz detaljan opis postupka izrade.
      </p>
      <img
        src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/0d/Inkscape_Logo.svg/1200px-Inkscape_Logo.svg.png"
        alt="inkscape logo"
        class="h-24 w-full object-contain"
      />
    </section>

    <hr class="border-indigo-200/50 border rounded-full my-2" />

    <section class="flex w-full items-center">
      <img src="@/assets/images/cats.png" alt="mačka"
        class="h-64 grow object-contain" />
    </section>

    <hr class="border-indigo-200/50 border rounded-full my-2" />

    <section class="text-justify flex flex-col gap-2">
      Koraci izrade:
      <ol class="flex flex-col gap-1 list-decimal pl-8">
        <li>
          Priprema dokumenta
          <ul class="list-disc pl-8">
            <li>
              Otvori se novi dokument u Inkscapeu i postavi odgovarajuće dimenzije canvas-a.
            </li>
            <li>
              Kreiraju se tri sloja: Obris, Pozadina, i Efekti za bolje upravljanje elementima.
            </li>
          </ul>
        </li>
        <li>
          Dodaje se gotovi obris mačke
          <ul class="list-disc pl-8">
            <li>Boja obrisa postavlja se na crvenu.</li>
          </ul>
        </li>
        <li>
          Dodavanje pozadine
          <ul class="list-disc pl-8">
            <li>Na sloj Pozadina dodaje se pravokutnik koji prekriva cijelu površinu platna.</li>
            <li>Primjenjuje se gradijent...</li>
            <li>Oblik mačke kopira se i koristi kao maska.</li>
          </ul>
        </li>
        <li>
          Primjena maske
          <ul class="list-disc pl-8">
            <li>Grupiranje i maskiranje.</li>
          </ul>
        </li>
        <li>
          Dodavanje efekata i sjena
          <ul class="list-disc pl-8">
            <li>Dodaje se duplicirani oblik za sjenu.</li>
            <li>Sjena se zatamnjuje i zamućuje.</li>
          </ul>
        </li>
      </ol>
    </section>
  </div>
</template>
