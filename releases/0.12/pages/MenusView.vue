<template lang="pug">
  component-view(v-bind:doc="doc" id="menus-view")
</template>

<script>

  export default {
    data () {
      return {
        doc: {
          title: 'Menu',
          component: 'menu',
          edit: 'MenusView',
          desc: 'The <code>v-menu</code> component shows a menu at the position of the element used to activate it.',
          examples: [
            { header: 'Activator', file: 'menus/1', desc: 'Remember to put the element that activates the menu in the <code>activator</code> slot.' },
            { header: 'Menus', file: 'menus/2', desc: 'Menus can be placed within almost any component.' },
            { header: 'Custom transitions', file: 'menus/3', desc: `Vuetify comes with 3 standard transitions, <strong>scale</strong>, <strong>slide-x</strong> and <strong>slide-y</strong>. You can also create your own and pass it as the transition argument. For an example of how the stock transitions are constructed, visit <a href="https://github.com/vuetifyjs/vuetify/blob/master/src/util/helpers.js#L13" target="_blank">here</a>.` }
          ],
          props: {
            'v-menu': {
              params: [
                [
                  'top',
                  'Boolean',
                  'False',
                  'Designates menu open up'
                ],
                [
                  'right',
                  'Boolean',
                  'False',
                  'Designates menu overflow to the right'
                ],
                [
                  'bottom',
                  'Boolean',
                  'False',
                  'Designates menu open down'
                ],
                [
                  'left',
                  'Boolean',
                  'False',
                  'Designates menu overflow to the left'
                ],
                [
                  'offset-x',
                  'Boolean',
                  'False',
                  'Offset the menu on the x-axis. Works in conjunction with direction left/right'
                ],
                [
                  'offset-y',
                  'Boolean',
                  'False',
                  'Offset the menu on the y-axis. Works in conjunction with direction top/rightbottom'
                ],
                [
                  'disabled',
                  'Boolean',
                  'False',
                  'Disables the menu'
                ],
                [
                  'max-height',
                  'Number',
                  'null',
                  'The maximum height of the menu, will overflow-y with scroll if content is too large'
                ],
                [
                  'nudge-x-auto',
                  'Number',
                  '-16',
                  'Nudge the menu on the x-axis'
                ],
                [
                  'nudge-y-auto',
                  'Number',
                  '-18',
                  'Nudge the menu on the y-axis'
                ],
                [
                  'nudge-top',
                  'Number',
                  '0',
                  'Nudge the menu from the top'
                ],
                [
                  'nudge-bottom',
                  'Number',
                  '0',
                  'Nudge the menu from the bottom'
                ],
                [
                  'nudge-left',
                  'Number',
                  '0',
                  'Nudge the menu from the left'
                ],
                [
                  'nudge-right',
                  'Number',
                  '0',
                  'Nudge the menu from the right'
                ],
                [
                  'open-on-click',
                  'Boolean',
                  'True',
                  'Designates whether menu should open on activator click'
                ],
                [
                  'close-on-click',
                  'Boolean',
                  'True',
                  'Designates if menu should close on outside-activator click'
                ],
                [
                  'origin',
                  'String',
                  'top left',
                  'Set the transform-origin of the transition'
                ],
                [
                  'transition',
                  'String',
                  'v-menu-transition',
                  'Set the transition component'
                ],
                [
                  'lazy',
                  'Boolean',
                  'False',
                  'Conditionally renders content on mounted'
                ]
              ]
            }
          },
          slots: {
            'v-menu': {
              shared: ['default'],
              params: [
                [
                  'activator',
                  'The element that will activate the menu'
                ]
              ]
            }
          }
        }
      }
    },

    mounted () {
      this.$emit('view', this.meta())
    },

    preFetch () {
      return this.methods.meta()
    },

    methods: {
      meta () {
        return {
          title: 'Menu Component | Vuetify.js',
          h1: 'Menus',
          description: 'Menu component for Vuetify Framework',
          keywords: 'vuetify, menus, components'
        }
      }
    }
  }
</script>
