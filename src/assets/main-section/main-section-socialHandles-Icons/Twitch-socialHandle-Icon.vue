<template>
  <svg
    xmlns="http://www.w3.org/2000/svg"
    xmlns:xlink="http://www.w3.org/1999/xlink"
    width="86.558"
    height="83.472"
    viewBox="0 0 86.558 83.472"
  >
    <defs>
      <filter
        id="Rectangle_751"
        x="0"
        y="0"
        width="86.558"
        height="83.472"
        filterUnits="userSpaceOnUse"
      >
        <feOffset dy="3" input="SourceAlpha" />
        <feGaussianBlur stdDeviation="3" result="blur" />
        <feFlood flood-opacity="0.161" />
        <feComposite operator="in" in2="blur" />
        <feComposite in="SourceGraphic" />
      </filter>
    </defs>
    <g transform="matrix(1, 0, 0, 1, 0, 0)" filter="url(#Rectangle_751)">
      <rect
        id="Rectangle_751-2"
        data-name="Rectangle 751"
        width="68.558"
        height="65.472"
        rx="12"
        transform="translate(9 6)"
        fill="#f6f6f6"
      />
    </g>
    <g id="twitch" transform="translate(28.437 24.104)">
      <path
        id="Path_328"
        data-name="Path 328"
        d="M.975,5.636V28.171h7.76V32.4h4.237l4.23-4.228h6.351l8.469-8.448V0H3.09ZM5.913,2.814H29.2v15.5l-4.941,4.93H16.5l-4.23,4.221V23.239H5.913Z"
        transform="translate(-0.975 0)"
        fill="#626262"
      />
      <path
        id="Path_329"
        data-name="Path 329"
        d="M10.385,6.262h2.821v8.45H10.385Z"
        transform="translate(2.317 2.191)"
        fill="#626262"
      />
      <path
        id="Path_330"
        data-name="Path 330"
        d="M16.133,6.262h2.823v8.45H16.133Z"
        transform="translate(4.328 2.191)"
        fill="#626262"
      />
    </g>
  </svg>
</template>

<script>
export default {
  name: "TwitchSocialHandle",
};
</script>
