
! At first, i create the project !
rails new my-app
cd my-app

! Then, i run bundle and install tailwind !
./bin/bundle add tailwindcss-rails
./bin/rails tailwindcss:install

! Next, i replace the "content" in application.tailwind.css !
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    './app/helpers/**/*.rb',
    './app/javascript/**/*.js',
    './app/views/**/*',
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}

! The last part was check in application.tailwind.css !
@tailwind base;
@tailwind components;
@tailwind utilities;

Now i have Tailwind in my project in RoR 7

!!! Another opcion is to use "rails new my-app --css tailwind" when i created the project !!!
