<template>
  <div>
    <!-- Button to open/close the sidebar on mobile -->
    <button
      data-drawer-target="default-sidebar"
      data-drawer-toggle="default-sidebar"
      aria-controls="default-sidebar"
      type="button"
      class="inline-flex items-center p-2 mt-2 ms-3 text-sm text-gray-500 rounded-lg sm:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600"
      @click="toggleSidebar"
    >
      <span class="sr-only">Open sidebar</span>
      <svg
        class="w-6 h-6"
        aria-hidden="true"
        fill="currentColor"
        viewBox="0 0 20 20"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          clip-rule="evenodd"
          fill-rule="evenodd"
          d="M2 4.75A.75.75 0 012.75 4h14.5a.75.75 0 010 1.5H2.75A.75.75 0 012 4.75zm0 10.5a.75.75 0 01.75-.75h7.5a.75.75 0 010 1.5h-7.5a.75.75 0 01-.75-.75zM2 10a.75.75 0 01.75-.75h14.5a.75.75 0 010 1.5H2.75A.75.75 0 012 10z"
        ></path>
      </svg>
    </button>

    <!-- Sidebar -->
    <aside
      id="default-sidebar"
      :class="sidebarClass"
      class="fixed top-0 left-0 border-r-8 border-gray-700 z-40 w-64 h-screen transition-transform -translate-x-full sm:translate-x-0"
      aria-label="Sidebar"
    >
      <div
        class="h-full px-3 py-4 overflow-y-auto bg-gray-50 dark:bg-gray-800 relative"
      >
        <!-- Close button in the top left corner of the mobile sidebar, shown only on mobile -->
        <button
          @click="toggleSidebar"
          class="top-4 left-4 mb-2 p-2 text-white bg-gray-500 rounded-full hover:bg-gray-700 focus:outline-none sm:hidden"
          aria-label="Close sidebar"
        >
          <svg
            class="w-5 h-5"
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M6 18L18 6M6 6l12 12"
            />
          </svg>
        </button>

        <!-- Sidebar content -->
        <ul class="space-y-2 font-medium">
          <li>
            <NuxtLink
              to="/"
              class="flex items-center p-2 text-gray-900 rounded-lg dark:text-white hover:bg-gray-100 dark:hover:bg-gray-700 group"
            >
              <svg
                width="30"
                height="30"
                viewBox="0 0 96 96"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M68 32C32 40 23.6 64.68 15.28 85.36L22.84 88L26.64 78.8C28.56 79.48 30.56 80 32 80C76 80 88 12 88 12C84 20 56 21 36 25C16 29 8 46 8 54C8 62 15 69 15 69C28 32 68 32 68 32Z"
                  fill="#9CA3AF"
                />
              </svg>

              <span class="ms-3">Intro</span>
            </NuxtLink>
          </li>
          <li>
            <NuxtLink
              to="/ontwikkelen"
              class="flex items-center p-2 text-gray-900 rounded-lg dark:text-white hover:bg-gray-100 dark:hover:bg-gray-700 group"
            >
              <svg
                width="30"
                height="30"
                viewBox="0 0 96 96"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M47.9998 62C44.2868 62 40.7259 60.525 38.1004 57.8995C35.4748 55.274 33.9998 51.713 33.9998 48C33.9998 44.287 35.4748 40.726 38.1004 38.1005C40.7259 35.475 44.2868 34 47.9998 34C51.7129 34 55.2738 35.475 57.8993 38.1005C60.5249 40.726 61.9998 44.287 61.9998 48C61.9998 51.713 60.5249 55.274 57.8993 57.8995C55.2738 60.525 51.7129 62 47.9998 62ZM77.7198 51.88C77.8798 50.6 77.9998 49.32 77.9998 48C77.9998 46.68 77.8798 45.36 77.7198 44L86.1599 37.48C86.9199 36.88 87.1198 35.8 86.6398 34.92L78.6398 21.08C78.1598 20.2 77.0798 19.84 76.1998 20.2L66.2398 24.2C64.1598 22.64 61.9998 21.28 59.4798 20.28L57.9998 9.68001C57.9186 9.20888 57.6732 8.78172 57.3071 8.47421C56.941 8.16671 56.4779 7.99872 55.9998 8.00001H39.9998C38.9998 8.00001 38.1598 8.72001 37.9998 9.68001L36.5198 20.28C33.9998 21.28 31.8398 22.64 29.7598 24.2L19.7998 20.2C18.9198 19.84 17.8398 20.2 17.3598 21.08L9.35985 34.92C8.83985 35.8 9.07985 36.88 9.83985 37.48L18.2798 44C18.1198 45.36 17.9998 46.68 17.9998 48C17.9998 49.32 18.1198 50.6 18.2798 51.88L9.83985 58.52C9.07985 59.12 8.83985 60.2 9.35985 61.08L17.3598 74.92C17.8398 75.8 18.9198 76.12 19.7998 75.8L29.7598 71.76C31.8398 73.36 33.9998 74.72 36.5198 75.72L37.9998 86.32C38.1598 87.28 38.9998 88 39.9998 88H55.9998C56.9998 88 57.8398 87.28 57.9998 86.32L59.4798 75.72C61.9998 74.68 64.1598 73.36 66.2398 71.76L76.1998 75.8C77.0798 76.12 78.1598 75.8 78.6398 74.92L86.6398 61.08C87.1198 60.2 86.9199 59.12 86.1599 58.52L77.7198 51.88Z"
                  fill="#9CA3AF"
                />
              </svg>

              <span class="ms-3">Ontwikkelen</span>
            </NuxtLink>
          </li>
          <li>
            <NuxtLink
              to="/ontwerpen"
              class="flex items-center p-2 text-gray-900 rounded-lg dark:text-white hover:bg-gray-100 dark:hover:bg-gray-700 group"
            >
              <svg
                width="30"
                height="30"
                viewBox="0 0 96 96"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M12.0001 69V84H27.0001L71.2401 39.72L56.2401 24.72L12.0001 69ZM90.4401 73.44L73.4401 90.44L52.6401 69.64L59.7201 62.56L63.7201 66.56L73.6001 56.64L79.2801 62.32L73.4401 68L77.6801 72L83.3601 66.4L90.4401 73.44ZM26.4401 43.32L5.56006 22.56L22.5601 5.56L29.6001 12.64L19.7201 22.56L24.0001 26.8L33.8401 16.88L39.5201 22.56L33.8401 28.2L37.8401 32.2L26.4401 43.32ZM82.8401 28C84.4001 26.44 84.4001 24 82.8401 22.36L73.4801 13.16C72.0001 11.6 69.4001 11.6 67.8401 13.16L60.4801 20.48L75.4801 35.48L82.8401 28Z"
                  fill="#9CA3AF"
                />
              </svg>

              <span class="ms-3">Ontwerpen</span>
            </NuxtLink>
          </li>
          <li>
            <NuxtLink
              to="ondernemen"
              class="flex items-center p-2 text-gray-900 rounded-lg dark:text-white hover:bg-gray-100 dark:hover:bg-gray-700 group"
            >
              <svg
                width="30"
                height="30"
                viewBox="0 0 96 77"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M48.51 12.78L33.99 24.54C31.575 26.49 31.11 30 32.94 32.505C34.875 35.175 38.64 35.7 41.235 33.675L56.13 22.095C57.18 21.285 58.68 21.465 59.505 22.515C60.33 23.565 60.135 25.065 59.085 25.89L55.95 28.32L76.8 47.52V19.2H76.695L76.11 18.825L65.22 11.85C62.925 10.38 60.24 9.59998 57.51 9.59998C54.24 9.59998 51.06 10.725 48.51 12.78ZM51.93 31.44L44.175 37.47C39.45 41.16 32.595 40.2 29.055 35.34C25.725 30.765 26.565 24.375 30.96 20.82L43.44 10.725C41.7 9.98998 39.825 9.61498 37.92 9.61498C35.1 9.59998 32.355 10.44 30 12L19.2 19.2V52.8H23.43L37.14 65.31C40.08 67.995 44.625 67.785 47.31 64.845C48.135 63.93 48.69 62.865 48.975 61.755L51.525 64.095C54.45 66.78 59.01 66.585 61.695 63.66C62.37 62.925 62.865 62.07 63.18 61.185C66.09 63.135 70.05 62.73 72.495 60.06C75.18 57.135 74.985 52.575 72.06 49.89L51.93 31.44ZM2.4 19.2C1.08 19.2 0 20.28 0 21.6V52.8C0 55.455 2.145 57.6 4.8 57.6H9.6C12.255 57.6 14.4 55.455 14.4 52.8V19.2H2.4ZM7.2 48C7.83652 48 8.44697 48.2528 8.89706 48.7029C9.34714 49.153 9.6 49.7635 9.6 50.4C9.6 51.0365 9.34714 51.6469 8.89706 52.097C8.44697 52.5471 7.83652 52.8 7.2 52.8C6.56348 52.8 5.95303 52.5471 5.50294 52.097C5.05286 51.6469 4.8 51.0365 4.8 50.4C4.8 49.7635 5.05286 49.153 5.50294 48.7029C5.95303 48.2528 6.56348 48 7.2 48ZM81.6 19.2V52.8C81.6 55.455 83.745 57.6 86.4 57.6H91.2C93.855 57.6 96 55.455 96 52.8V21.6C96 20.28 94.92 19.2 93.6 19.2H81.6ZM86.4 50.4C86.4 49.7635 86.6529 49.153 87.1029 48.7029C87.553 48.2528 88.1635 48 88.8 48C89.4365 48 90.047 48.2528 90.4971 48.7029C90.9471 49.153 91.2 49.7635 91.2 50.4C91.2 51.0365 90.9471 51.6469 90.4971 52.097C90.047 52.5471 89.4365 52.8 88.8 52.8C88.1635 52.8 87.553 52.5471 87.1029 52.097C86.6529 51.6469 86.4 51.0365 86.4 50.4Z"
                  fill="#9CA3AF"
                />
              </svg>

              <span class="ms-3">Ondernemen</span>
            </NuxtLink>
          </li>
          <li>
            <NuxtLink
              to="/betrokken"
              class="flex items-center p-2 text-gray-900 rounded-lg dark:text-white hover:bg-gray-100 dark:hover:bg-gray-700 group"
            >
              <svg
                width="30"
                height="30"
                viewBox="0 0 96 96"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M36 22C36 18.8174 37.2643 15.7652 39.5147 13.5147C41.7652 11.2643 44.8174 10 48 10C51.1826 10 54.2348 11.2643 56.4853 13.5147C58.7357 15.7652 60 18.8174 60 22C60 25.1826 58.7357 28.2348 56.4853 30.4853C54.2348 32.7357 51.1826 34 48 34C44.8174 34 41.7652 32.7357 39.5147 30.4853C37.2643 28.2348 36 25.1826 36 22ZM74 14C71.3478 14 68.8043 15.0536 66.9289 16.9289C65.0536 18.8043 64 21.3478 64 24C64 26.6522 65.0536 29.1957 66.9289 31.0711C68.8043 32.9464 71.3478 34 74 34C76.6522 34 79.1957 32.9464 81.0711 31.0711C82.9464 29.1957 84 26.6522 84 24C84 21.3478 82.9464 18.8043 81.0711 16.9289C79.1957 15.0536 76.6522 14 74 14ZM22 14C19.3478 14 16.8043 15.0536 14.9289 16.9289C13.0536 18.8043 12 21.3478 12 24C12 26.6522 13.0536 29.1957 14.9289 31.0711C16.8043 32.9464 19.3478 34 22 34C24.6522 34 27.1957 32.9464 29.0711 31.0711C30.9464 29.1957 32 26.6522 32 24C32 21.3478 30.9464 18.8043 29.0711 16.9289C27.1957 15.0536 24.6522 14 22 14ZM38.5 38C36.2457 38 34.0837 38.8955 32.4896 40.4896C30.8955 42.0837 30 44.2457 30 46.5V68C30 72.7739 31.8964 77.3523 35.2721 80.7279C38.6477 84.1036 43.2261 86 48 86C52.7739 86 57.3523 84.1036 60.7279 80.7279C64.1036 77.3523 66 72.7739 66 68V46.5C66 44.2457 65.1045 42.0837 63.5104 40.4896C61.9163 38.8955 59.7543 38 57.5 38H38.5ZM26 46.5C26 43.3 27.204 40.378 29.184 38.166C28.6295 38.0554 28.0654 37.9998 27.5 38H16.5C14.2457 38 12.0837 38.8955 10.4896 40.4896C8.89553 42.0837 8 44.2457 8 46.5V66C7.99933 68.4177 8.62479 70.7944 9.81546 72.8986C11.0061 75.0028 12.7214 76.7627 14.7943 78.0071C16.8672 79.2515 19.227 79.9378 21.6439 79.9993C24.0609 80.0608 26.4525 79.4954 28.586 78.358C26.8828 75.1715 25.9944 71.6131 26 68V46.5ZM70 68C70 71.744 69.064 75.27 67.414 78.358C69.5475 79.4954 71.9391 80.0608 74.3561 79.9993C76.773 79.9378 79.1328 79.2515 81.2057 78.0071C83.2786 76.7627 84.9939 75.0028 86.1845 72.8986C87.3752 70.7944 88.0007 68.4177 88 66V46.5C88 44.2457 87.1045 42.0837 85.5104 40.4896C83.9163 38.8955 81.7543 38 79.5 38H68.5C67.9227 38.0013 67.3613 38.0567 66.816 38.166C68.8696 40.4558 70.0037 43.4242 70 46.5V68Z"
                  fill="#9CA3AF"
                />
              </svg>

              <span class="ms-3">Betrokken</span>
            </NuxtLink>
          </li>
          <li>
            <NuxtLink
              to="/stageterugkomdagen"
              class="flex items-center p-2 text-gray-900 rounded-lg dark:text-white hover:bg-gray-100 dark:hover:bg-gray-700 group"
            >
              <svg
                width="30"
                height="30"
                viewBox="0 0 96 96"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M8 76C8 82.8 13.2 88 20 88H76C82.8 88 88 82.8 88 76V44H8V76ZM76 16H68V12C68 9.6 66.4 8 64 8C61.6 8 60 9.6 60 12V16H36V12C36 9.6 34.4 8 32 8C29.6 8 28 9.6 28 12V16H20C13.2 16 8 21.2 8 28V36H88V28C88 21.2 82.8 16 76 16Z"
                  fill="#9CA3AF"
                />
              </svg>

              <span class="ms-3">Stageterugkomdagen</span>
            </NuxtLink>
          </li>
          <li>
            <NuxtLink
              to="/uitwisselingsbezoek"
              class="flex items-center p-2 text-gray-900 rounded-lg dark:text-white hover:bg-gray-100 dark:hover:bg-gray-700 group"
            >
              <svg
                width="30"
                height="30"
                viewBox="0 0 96 73"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <g clip-path="url(#clip0_2006_47)">
                  <path
                    d="M86.069 19.8621C86.069 17.1034 85.1035 14.7586 83.1724 12.8276C81.2414 10.8966 78.8966 9.93103 76.1379 9.93103H72.8276V29.7931H76.1379C78.8966 29.7931 81.2414 28.8276 83.1724 26.8966C85.1035 24.9655 86.069 22.6207 86.069 19.8621ZM0 59.5862H92.6897C92.6897 63.2414 91.3966 66.3621 88.8103 68.9483C86.2241 71.5345 83.1035 72.8276 79.4483 72.8276H13.2414C9.58621 72.8276 6.46552 71.5345 3.87931 68.9483C1.2931 66.3621 0 63.2414 0 59.5862ZM96 19.8621C96 25.3448 94.0603 30.0259 90.181 33.9052C86.3017 37.7845 81.6207 39.7241 76.1379 39.7241H72.8276V41.3793C72.8276 44.5517 71.6897 47.2759 69.4138 49.5517C67.1379 51.8276 64.4138 52.9655 61.2414 52.9655H24.8276C21.6552 52.9655 18.931 51.8276 16.6552 49.5517C14.3793 47.2759 13.2414 44.5517 13.2414 41.3793V3.31034C13.2414 2.41379 13.569 1.63793 14.2241 0.982759C14.8793 0.327586 15.6552 0 16.5517 0H76.1379C81.6207 0 86.3017 1.93966 90.181 5.81897C94.0603 9.69828 96 14.3793 96 19.8621Z"
                    fill="#9CA3AF"
                  />
                </g>
                <defs>
                  <clipPath id="clip0_2006_47">
                    <rect width="96" height="72.8276" fill="white" />
                  </clipPath>
                </defs>
              </svg>

              <span class="ms-3">Uitwisselingsbezoek</span>
            </NuxtLink>
          </li>
          <li>
            <NuxtLink
              to="/conclusie"
              href="#"
              class="flex items-center p-2 text-gray-900 rounded-lg dark:text-white hover:bg-gray-100 dark:hover:bg-gray-700 group"
            >
              <svg
                width="30"
                height="30"
                viewBox="0 0 96 96"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M20 84C17.8 84 15.9173 83.2173 14.352 81.652C12.7867 80.0867 12.0027 78.2027 12 76V20C12 17.8 12.784 15.9173 14.352 14.352C15.92 12.7867 17.8027 12.0027 20 12H76C78.2 12 80.084 12.784 81.652 14.352C83.22 15.92 84.0027 17.8027 84 20V50.8L69.4 65.4L60.9 56.9L43.9 73.8L54.1 84H20ZM44 52H68V44H44V52ZM44 36H68V28H44V36ZM69.4 88L55.2 73.8L60.9 68.2L69.4 76.7L86.4 59.7L92 65.4L69.4 88ZM32 52C33.1333 52 34.084 51.616 34.852 50.848C35.62 50.08 36.0027 49.1307 36 48C35.9973 46.8693 35.6133 45.92 34.848 45.152C34.0827 44.384 33.1333 44 32 44C30.8667 44 29.9173 44.384 29.152 45.152C28.3867 45.92 28.0027 46.8693 28 48C27.9973 49.1307 28.3813 50.0813 29.152 50.852C29.9227 51.6227 30.872 52.0053 32 52ZM32 36C33.1333 36 34.084 35.616 34.852 34.848C35.62 34.08 36.0027 33.1307 36 32C35.9973 30.8693 35.6133 29.92 34.848 29.152C34.0827 28.384 33.1333 28 32 28C30.8667 28 29.9173 28.384 29.152 29.152C28.3867 29.92 28.0027 30.8693 28 32C27.9973 33.1307 28.3813 34.0813 29.152 34.852C29.9227 35.6227 30.872 36.0053 32 36Z"
                  fill="#9CA3AF"
                />
              </svg>

              <span class="ms-3">Conclusie</span>
            </NuxtLink>
          </li>
          <li>
            <NuxtLink
              to="/onderzoeksverslag"
              class="flex items-center p-2 text-gray-900 rounded-lg dark:text-white hover:bg-gray-100 dark:hover:bg-gray-700 group"
            >
              <svg
                width="30"
                height="30"
                viewBox="0 0 96 96"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <mask
                  id="mask0_2006_47"
                  style="mask-type: luminance"
                  maskUnits="userSpaceOnUse"
                  x="6"
                  y="4"
                  width="84"
                  height="88"
                >
                  <path
                    d="M10 14C10 12.4087 10.6321 10.8826 11.7574 9.75736C12.8826 8.63214 14.4087 8 16 8H64C65.5913 8 67.1174 8.63214 68.2426 9.75736C69.3679 10.8826 70 12.4087 70 14V88H16C14.4087 88 12.8826 87.3679 11.7574 86.2426C10.6321 85.1174 10 83.5913 10 82V14Z"
                    fill="white"
                    stroke="white"
                    stroke-width="6.06897"
                    stroke-linejoin="round"
                  />
                  <path
                    d="M70 48C70 46.9391 70.4214 45.9217 71.1716 45.1716C71.9217 44.4214 72.9391 44 74 44H82C83.0609 44 84.0783 44.4214 84.8284 45.1716C85.5786 45.9217 86 46.9391 86 48V82C86 83.5913 85.3679 85.1174 84.2426 86.2426C83.1174 87.3679 81.5913 88 80 88H70V48Z"
                    stroke="white"
                    stroke-width="6.06897"
                    stroke-linejoin="round"
                  />
                  <path
                    d="M22 24H38M22 38H46"
                    stroke="black"
                    stroke-width="6.06897"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  />
                </mask>
                <g mask="url(#mask0_2006_47)">
                  <path d="M0 0H96V96H0V0Z" fill="#9CA3AF" />
                </g>
              </svg>

              <span class="ms-3">Onderzoeksverslag</span>
            </NuxtLink>
          </li>
          <li>
            <button
              type="button"
              class="flex items-center w-full p-2 text-base text-gray-900 transition duration-75 rounded-lg group hover:bg-gray-100 dark:text-white dark:hover:bg-gray-700"
              aria-controls="dropdown-example"
              @click="toggleDropdown"
            >
              <svg
                class="flex-shrink-0 w-5 h-5 text-gray-500 transition duration-75 group-hover:text-gray-900 dark:text-gray-400 dark:group-hover:text-white"
                aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg"
                fill="currentColor"
                viewBox="0 0 18 21"
              >
                <path
                  d="M15 12a1 1 0 0 0 .962-.726l2-7A1 1 0 0 0 17 3H3.77L3.175.745A1 1 0 0 0 2.208 0H1a1 1 0 0 0 0 2h.438l.6 2.255v.019l2 7 .746 2.986A3 3 0 1 0 9 17a2.966 2.966 0 0 0-.184-1h2.368c-.118.32-.18.659-.184 1a3 3 0 1 0 3-3H6.78l-.5-2H15Z"
                />
              </svg>
              <span
                class="flex-1 ms-3 text-left rtl:text-right whitespace-nowrap"
              >
                E-commerce
              </span>
              <svg
                class="w-3 h-3"
                aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 10 6"
              >
                <path
                  stroke="currentColor"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="m1 1 4 4 4-4"
                />
              </svg>
            </button>
            <ul
              v-show="dropdownVisible"
              id="dropdown-example"
              class="py-2 space-y-2"
            >
              <li>
                <a
                  href="#"
                  class="flex items-center w-full p-2 text-gray-900 transition duration-75 rounded-lg pl-11 group hover:bg-gray-100 dark:text-white dark:hover:bg-gray-700"
                  >Products</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="flex items-center w-full p-2 text-gray-900 transition duration-75 rounded-lg pl-11 group hover:bg-gray-100 dark:text-white dark:hover:bg-gray-700"
                  >Billing</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="flex items-center w-full p-2 text-gray-900 transition duration-75 rounded-lg pl-11 group hover:bg-gray-100 dark:text-white dark:hover:bg-gray-700"
                  >Invoice</a
                >
              </li>
            </ul>
          </li>
          <!-- Other sidebar items here (unchanged) -->
        </ul>
      </div>
    </aside>
  </div>
</template>

<script lang="ts">
import { ref, computed } from "vue";

export default {
  name: "Sidebar",
  setup() {
    // State for controlling the dropdown visibility
    const dropdownVisible = ref(false);

    // State for controlling the sidebar visibility
    const sidebarVisible = ref(false);

    // Function to toggle dropdown visibility
    const toggleDropdown = () => {
      dropdownVisible.value = !dropdownVisible.value;
    };

    // Function to toggle sidebar visibility on mobile
    const toggleSidebar = () => {
      sidebarVisible.value = !sidebarVisible.value;
    };

    return {
      dropdownVisible,
      sidebarVisible,
      toggleDropdown,
      toggleSidebar,
      sidebarClass: computed(() =>
        sidebarVisible.value ? "translate-x-0" : "-translate-x-full"
      ),
    };
  },
};
</script>

<style scoped>
/* Add custom styles if necessary */
</style>
