<script setup lang="ts">
import type { ChatItem } from "./components/Chat.vue";
import { ref } from "vue";
import Chat from "./components/Chat.vue";

const settings = {
  website: "https://salamdal.gozle.org",
};

const chats = ref<ChatItem[][]>([
  [
    {
      name: "Timur Agayev",
      message: "Salam",
      image: "/avatars/1.jpg",
      time: "12:34",
      position: "start",
    },
    {
      name: "Alfred",
      message: "Salam...",
      image: "/avatars/2.jpg",
      time: "12:35",
      position: "end",
    },
  ],
  [
    {
      name: "Timur Agayev",
      message:
        "Telegram, premium abunalarynyň satuwyny artdyrmak üçin doglan gününi goşmaga mümkinçilik berdi. UX dizaýnerleri gowy iş etdiler gerek?",
      image: "/avatars/1.jpg",
      time: "12:38",
      position: "start",
    },
    {
      name: "Alfred",
      message:
        "Sen ony gowy UX hasap edýäňmi? Dizaýneriň eden işi näme ol ýerde? Marketologlaryň eden işi bu.",
      image: "/avatars/2.jpg",
      time: "12:39",
      position: "end",
    },
  ],
  [
    {
      name: "Timur Agayev",
      message:
        "Salamaleýkum! Telegram, premium abunalarynyň satuwyny artdyrmak üçin doglan gününi goşmaga mümkinçilik berdi. UX dizaýnerleri gowy iş etdiler gerek?",
      image: "/avatars/1.jpg",
      time: "12:38",
      position: "start",
    },
    {
      name: "Alfred",
      message:
        "Waleýkumassalam! Sen ony gowy UX hasap edýäňmi? Dizaýneriň eden işi näme ol ýerde? Marketologlaryň eden işi bu.",
      image: "/avatars/2.jpg",
      time: "12:39",
      position: "end",
    },
  ],
  [
    {
      name: "Mergen A 🇹🇲",
      message:
        "Salam Häzirki wagtda meşgul däl bolsaňyz, size sorag berip biljekdigimi bilmek isledim? Häzirki wagtda şular ýaly zatlaryň üstünde işleýärin we şeýle we şeýle etmek isleýärin ...",
      image: "/avatars/3.jpg",
      time: "22:38",
      position: "start",
    },
  ],
]);
</script>

<template>
  <div class="md:p-12 p-4 space-y-4">
    <div class="prose prose-headings:text-center mx-auto">
      <h1>Gaýrat ediň, söhbetdeşlikde diňe "Salam" ýazmaň</h1>
    </div>

    <div class="max-w-[666px] mx-auto">
      <div class="p-4 bg-neutral-900 rounded-xl space-y-2">
        <Chat :items="chats[0]" />

        <p class="text-center w-fit mx-auto px-4 py-2 rounded-xl">
          … sorag düzýänça garaşýar …
        </p>

        <Chat :items="chats[1]" />
      </div>
    </div>

    <div class="prose mx-auto">
      <p>
        Bu telefonda birine jaň edip, “Salam!” diýip, ümsümlige salan ýaly
        bolýar.
      </p>

      <p>Gowusy:</p>
    </div>

    <div class="max-w-[666px] mx-auto">
      <div class="p-4 bg-neutral-900 rounded-xl space-y-12">
        <Chat :items="chats[2]" />
      </div>
    </div>

    <div class="prose mx-auto">
      <p>
        Üns beriň, siz jogabyňyzy çalt alýarsyňyz we söhbetdeşiňizi
        garaşdyrmaýarsyňyz, we ol derrew jogaby hakda pikirlenip başlaýar.
      </p>

      <p>
        Size göni meselä geçmän, duşuşykdaky ýaly sypaýy bolmana
        çemeleşýärsiňiz. Ýone çat - başga gürruň. Adamlar çalt gürleşýärler,
        ýone haýal ýazyşýarlar. Sypaýa bolmagyň ýerine, sorag düzüp oturkaňyz,
        siz beýleki adamy garaşdyrýarsyňyz, şeýdiň hem öndürjiligi pese
        düşürýärsiňiz.
      </p>

      <p>
        "Salam", "Salowmaleýkim", "Salam, gowmy?", "Salam, nirede?", "Salam,
        sorag bar", "Wagtyň barmy" ýaly hatlara-da degişli. Sorag berde goý!
      </p>

      <p>
        Eger-de size salam diýip göni soraga geçmeklik gödek görünýän bolsa,
        şeýle hem edip bilersiňiz:
      </p>
    </div>

    <div class="max-w-[666px] mx-auto">
      <div class="p-4 bg-neutral-900 rounded-xl space-y-12">
        <Chat :items="chats[3]" />
      </div>
    </div>

    <div class="prose mx-auto">
      <p>
        Üstesine, haçanda sorag göni berlende, bilelikde işleşmek mümkinçigi
        açylýar. Eger-de söhbetdeş elýeter däl bolsa, we siz ol elýeter bolýança
        çatdan çyksaňyz, ol şonda-da soragyňyzya jogap berip biler, we siziň
        "Salam"-yňyza jogap berip, näme bolduka diýiň pikirlenip oturmaz.
      </p>

      <hr />

      <p>
        Eger-de siz biriniň profilinde şu makala salgy görseňiz, ol siziň
        "Salam" hatyňyzya jogap bermez.
      </p>

      <p>
        Bu makalanyň salgysy:
        <a :href="settings.website">{{ settings.website }}</a>
      </p>

      <p>
        Suratda:
        <a :href="settings.website + '/surat.jpg'" target="_blank"
          >{{ settings.website }}/surat.jpg</a
        >
      </p>

      <div class="flex items-center gap-2">
        <span>Domen üçin:</span>

        <a
          href="https://donate.stream/salamdaldir"
          target="_blank"
          class="hover:opacity-60 transition"
        >
          <div
            class="w-full h-auto overflow-hidden rounded max-w-[120px] relative"
          >
            <iframe
              id="donate"
              class="h-[30px] pointer-events-none -ml-3"
              src="https://donate.stream/widget-stats?uid=b1adb7025d0844c9958dfac001ada40d&token=9CldoKt6yRvbupW5NYZXAegJqqTp5we48OVPIHz9PE"
            />
          </div>
        </a>

        <div class="flex gap-2">
          <span>ýa-da</span>

          <span><a href="/qr-donate.png" target="_blank">QR</a></span>
        </div>
      </div>
    </div>
  </div>

  <div class="bg-neutral-900 p-4">
    <div class="prose mx-auto">
      <p>
        Hakyky makala —
        <a href="https://neprivet.com/" target="_blank">neprivet.com</a>, ýazan:
        <a href="https://github.com/selimdev00" target="_blank">selimdev</a>,
        host:
        <a href="https://github.com/gozle/" target="_blank">Gozle</a>
      </p>
    </div>
  </div>
</template>
