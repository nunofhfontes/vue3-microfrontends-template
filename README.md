# vue3-microfrontends-template
This is a project to show how to build MicroFrontends with Vue 3. This project will be a main-app with the capability to lazy load MicroFrontends and display them on the webpage.

These MicroFrontends can be built using the Web Components (W3C) concept, which means that MicroFrontends are normal webapps but wrapped in Web Components.

The main-app will have the responsability to download the MicroFrontend's scripts, which will happen when routing between pages. The downloads are triggered when Vue is trying to change route, in the router guards.

A MicroFrontend script is download before the page change, and when the page actually changes, the new component that Vue inserts on the page will have the MicroFrontends custom element, which will be activated because it's script was previously downloaded in between page change.
