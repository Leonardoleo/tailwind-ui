# Tailwind UI Components

### Follow the steps below to make sure it works successfully on your project.

1. Install [HeadlessUI](https://headlessui.dev/)

```
npm install @headlessui/vue
```

2. Install [HeroIcons](https://heroicons.com/)

```
npm install @heroicons/vue
```

3. Install and add the following Tailwind plugins in your `tailwind.config.js`

```
npm install @tailwindcss/forms @tailwindcss/typography @tailwindcss/aspect-ratio

module.exports = {
    plugins: [
        require('@tailwindcss/forms'),
        require('@tailwindcss/typography'),
        require('@tailwindcss/aspect-ratio')
    ],
}
```

4. If somehow the component doesn't work, please check the `comments` on top of
   each component Vue file.
