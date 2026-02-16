<template>
  <a
    href="#"
    target="_blank"
    rel="noopener noreferrer"
    class="group hover:border--600 relative flex w-full items-center gap-4 rounded-xl border border-gray-700 bg-gray-800 p-4 shadow-md shadow-gray-900/50 transition-all duration-300 hover:scale-[1.02] hover:shadow-xl hover:shadow-teal-500/20"
  >
    <!-- Icon Container -->
    <div
      class="flex h-12 w-12 shrink-0 items-center justify-center rounded-lg bg-gray-700 text-teal-400 transition-all duration-300 group-hover:scale-110 group-hover:bg-teal-500 group-hover:text-white group-hover:shadow-xl group-hover:shadow-teal-500/20"
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="32"
        height="32"
        viewBox="0 0 24 24"
      >
        <!-- Icon from Majesticons by Gerrit Halfmann - https://github.com/halfmage/majesticons/blob/main/LICENSE -->
        <g fill="currentColor">
          <path
            d="M12.486 5.414a1 1 0 0 0-.972 0L5.06 9l6.455 3.586a1 1 0 0 0 .972 0L18.94 9l-6.455-3.586zm-1.943-1.749a3 3 0 0 1 2.914 0l8.029 4.46a1 1 0 0 1 0 1.75l-8.03 4.46a3 3 0 0 1-2.913 0l-8.029-4.46a1 1 0 0 1 0-1.75l8.03-4.46z"
          />
          <path
            d="M21 8a1 1 0 0 1 1 1v7a1 1 0 1 1-2 0V9a1 1 0 0 1 1-1zM6 10a1 1 0 0 1 1 1v5.382l4.553 2.276a1 1 0 0 0 .894 0L17 16.382V11a1 1 0 1 1 2 0v6a1 1 0 0 1-.553.894l-5.105 2.553a3 3 0 0 1-2.684 0l-5.105-2.553A1 1 0 0 1 5 17v-6a1 1 0 0 1 1-1z"
          />
        </g>
      </svg>
      <svg
        viewBox="0 0 24 24"
        fill="none"
        stroke="currentColor"
        class="h-6 w-6 transition-transform duration-300 group-hover:rotate-6"
      ></svg>
    </div>

    <!--Text Content-->

    <div class="min-w-0 flex-1">
      <h3 class="truncate font-display font-semibold text-white">Link Title</h3>
      <p>This is where information will go.</p>
    </div>
    <!-- Hover Glow Effect -->
    <div
      class="absolute inset-0 rounded-xl bg-linear-to-r from-teal-500/0 via-teal-500/10 to-teal-500/0 opacity-0 transition-opacity duration-300 group-hover:opacity-100"
    />
  </a>
</template>
