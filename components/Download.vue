<template>
  <div id="downloadSection" class="mt-16">
    <h2 class="font-extrabold text-2xl">Descargar</h2>
    <div class="stepC mt-6">
      <p>Acepte los términos antes de descargar.</p>
      <Check
        v-for="(item, index) in downloadCheckList"
        :downloadCheckList="downloadCheckList"
        :item="item"
        :key="index"
        :index="index"
      />
      <button
        ref="downloadPackage"
        @click="downloadPackage"
        class="inline-block bg-gray-700 leading-none text-2xl tracking-wide border-2 border-transparent font-extrabold p-6 rounded mt-12 select-none transition-colors duration-200 focus:outline-none"
        :title="
          downloadChecked
            ? ''
            : 'Complete la lista de verificación para descargar la tarjeta empaquetada.'
        "
        :class="
          downloadChecked
            ? 'bg-emerald-600 cursor-pointer text-white focus:bg-emerald-500 hover:bg-emerald-500'
            : 'cursor-not-allowed text-black'
        "
      >
      Guardar la tarjeta digital en su edición web
      </button>
      <p class="mt-6 border p-4 rounded border-gray-700 text-gray-400">
        Extraiga el archivo ZIP descargado y siga el
        <a
          class="cursor-pointer underline font-extrabold text-emerald-600 hover:text-emerald-500 focus:text-emerald-500 transition-colors duration-200"
          href="https://www.youtube.com/playlist?list=PLsFzOs6X4MmrdXNgpyjDXMsttkb1OkY6P"
          rel="noreferrer"
          target="_blank"
          >Videotutorial para colocar en el hosting</a
        >        
        la tarjeta de presentación digital.
        <br /><br />
        Si desea respaldar este servicio, compre una solución de hosting con nosotros.
        <br /><a
          class="inline-block font-extrabold tracking-wide leading-none shrink-0 p-3 text-white bg-gray-700 rounded hover:bg-gray-600 focus:bg-gray-600 transition-colors duration-200 mt-4"
          href="https://www.vishnuraghav.com/donate/"
          rel="noreferrer"
          target="_blank"
          >Adquirir un plan hosting básico</a
        >
      </p>
    </div>
  </div>
</template>

<script>
import Check from '@/components/Check'
export default {
  props: ['downloadCheckList', 'downloadChecked', 'downloadPackage'],
  components: {
    Check,
  },
}
</script>