<template>
  <nav
    class="flex flex-row h-20 align-middle gap-3 px-3 bg-transparent fixed w-full z-10"
  >
    <div
      class="flex self-center rounded-3xl bg-slate-300/50 h-10 content-center justify-center px-4 backdrop-blur"
    >
      <a class="self-center uppercase font-black text-lg hover:no-underline"
        >Rains</a
      >
    </div>
    <div
      class="flex self-center items-center rounded-3xl bg-slate-300/50 h-10 content-center px-4 gap-7 backdrop-blur"
    >
      <a>Nyheder</a>
      <a>Dame</a>
      <a>Herre</a>
      <a>Tasker</a>
      <a>Accessories</a>
      <a>Rains World</a>
    </div>
    <div
      class="flex self-center rounded-3xl bg-slate-300 h-10 content-center justify-center px-2 ml-auto bg-slate-300/50 cursor-pointer backdrop-blur"
    >
      <span class="self-center px-2"
        ><svg
          xmlns="http://www.w3.org/2000/svg"
          width="16"
          height="16"
          fill="currentColor"
          class="bi bi-search text-black"
          viewBox="0 0 16 16"
        >
          <path
            d="M11.742 10.344a6.5 6.5 0 1 0-1.397 1.398h-.001c.03.04.062.078.098.115l3.85 3.85a1 1 0 0 0 1.415-1.414l-3.85-3.85a1.007 1.007 0 0 0-.115-.1zM12 6.5a5.5 5.5 0 1 1-11 0 5.5 5.5 0 0 1 11 0z"
          />
        </svg>
      </span>
      <a class="self-center uppercase pr-2 hover:no-underline">Søg</a>
    </div>
    <div
      class="flex flex-row self-center rounded-3xl bg-slate-300 h-10 content-center justify-center px-2 bg-slate-300/50 cursor-pointer"
    >
      <span class="self-center px-2"
        ><svg
          xmlns="http://www.w3.org/2000/svg"
          width="16"
          height="16"
          fill="currentColor"
          class="bi bi-bag-check"
          viewBox="0 0 16 16"
        >
          <path
            fill-rule="evenodd"
            d="M10.854 8.146a.5.5 0 0 1 0 .708l-3 3a.5.5 0 0 1-.708 0l-1.5-1.5a.5.5 0 0 1 .708-.708L7.5 10.793l2.646-2.647a.5.5 0 0 1 .708 0z"
          />
          <path
            d="M8 1a2.5 2.5 0 0 1 2.5 2.5V4h-5v-.5A2.5 2.5 0 0 1 8 1zm3.5 3v-.5a3.5 3.5 0 1 0-7 0V4H1v10a2 2 0 0 0 2 2h10a2 2 0 0 0 2-2V4h-3.5zM2 5h12v9a1 1 0 0 1-1 1H3a1 1 0 0 1-1-1V5z"
          />
        </svg>
      </span>
      <a class="self-center uppercase pr-2 hover:no-underline">Kurv</a>
    </div>
  </nav>
</template>
