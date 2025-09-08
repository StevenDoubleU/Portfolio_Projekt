<template>
  <div class="min-h-screen bg-gradient-to-b from-slate-900 to-slate-800 text-slate-100 flex flex-col">
    <header class="container mx-auto px-6 py-8">
      <h1 class="text-3xl font-semibold tracking-tight">Mein Portfolio</h1>
    </header>

    <main class="flex-1">
      <!-- Hero: Bild mit Animation + Text darunter -->
      <section class="container mx-auto px-6 py-12">
        <div class="flex flex-col items-center text-center gap-6">
          <div class="w-full flex flex-col items-center">
            <div class="h-px w-64 bg-slate-600/70 mb-3"></div>
            <div class="overflow-visible">
              <img
                src="../assets/platzhalter_portrait.png"
                alt="Profilbild Platzhalter"
                class="w-40 h-40 sm:w-48 sm:h-48 object-cover rounded-full shadow-xl animate-riseFromLine"
              />
            </div>
          </div>

          <div class="max-w-2xl opacity-0 animate-fadeInDelayed">
            <h2 class="text-2xl sm:text-3xl font-bold">Hallo, ich bin [Dein Name]</h2>
            <p class="mt-2 text-slate-300">
              Kurze Vorstellung über dich – z. B. dein Beruf, deine
              Schwerpunkte und wofür du brennst. Das Bild klappt sich aus
              einem horizontalen Strich auf, danach erscheint dieser Text.
            </p>
          </div>
        </div>
      </section>

      <!-- Projekte: Platzhalterbereich -->
      <section id="projects" class="container mx-auto px-6 py-16">
        <h3 class="text-xl sm:text-2xl font-semibold mb-6">Projekte</h3>
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
          <div class="rounded-lg bg-slate-700/40 border border-slate-600/50 p-6 min-h-[140px]">
            Projekt-Platzhalter – hier kommen Karten/Teaser hin.
          </div>
        </div>
      </section>

      <!-- Kontakt + Links: Platzhalterbereich -->
      <section id="contact" class="container mx-auto px-6 py-16">
        <h3 class="text-xl sm:text-2xl font-semibold mb-6">Kontakt</h3>
        <div class="grid gap-8 md:grid-cols-2">
          <form class="space-y-4">
            <input
              type="text"
              placeholder="Name"
              class="w-full rounded-md bg-slate-900/60 border border-slate-700/60 px-4 py-2 outline-none focus:border-sky-500 focus:ring-1 focus:ring-sky-500"
            />
            <input
              type="email"
              placeholder="E-Mail"
              class="w-full rounded-md bg-slate-900/60 border border-slate-700/60 px-4 py-2 outline-none focus:border-sky-500 focus:ring-1 focus:ring-sky-500"
            />
            <textarea
              placeholder="Nachricht"
              rows="5"
              class="w-full rounded-md bg-slate-900/60 border border-slate-700/60 px-4 py-2 outline-none focus:border-sky-500 focus:ring-1 focus:ring-sky-500"
            ></textarea>
            <button
              type="button"
              class="inline-flex items-center justify-center rounded-md bg-sky-600 hover:bg-sky-500 active:bg-sky-700 px-4 py-2 font-medium"
            >
              Senden
            </button>
          </form>

          <div class="space-y-3">
            <h4 class="text-lg font-medium">Links</h4>
            <ul class="space-y-2">
              <li>
                <a href="#" class="text-sky-400 hover:text-sky-300">LinkedIn</a>
              </li>
              <li>
                <a href="#" class="text-sky-400 hover:text-sky-300">GitHub</a>
              </li>
              <li>
                <a href="#" class="text-sky-400 hover:text-sky-300">E-Mail</a>
              </li>
            </ul>
          </div>
        </div>
      </section>
    </main>

    <footer class="border-t border-slate-700/60">
      <div class="container mx-auto px-6 py-6 text-sm text-slate-400">
        © {{ new Date().getFullYear() }} Dein Name
      </div>
    </footer>
  </div>
</template>

<script setup>
// Noch kein Script benötigt – rein statische Struktur/Animation.
</script>

<style scoped>
@keyframes riseFromLine {
  0% {
    transform: scaleY(0.02);
    opacity: 0;
  }
  60% {
    opacity: 1;
  }
  100% {
    transform: scaleY(1);
    opacity: 1;
  }
}

.animate-riseFromLine {
  animation: riseFromLine 900ms ease-out both;
  transform-origin: bottom center;
  display: inline-block;
}

@keyframes fadeInDelayed {
  0% {
    opacity: 0;
    transform: translateY(6px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-fadeInDelayed {
  animation: fadeInDelayed 600ms ease-out 800ms both;
}
</style>
