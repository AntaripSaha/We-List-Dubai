<template>
  <Popover v-slot='{ open }' class='relative'>
    <PopoverButton
      :class="[open ? 'text-second-color-900' : 'text-second-color-500', 'group inline-flex items-center text-sm focus:outline-none text-second-color-500 hover:text-second-color-900']">
      <span>
        <h4 class="text-red-400/100" style="color: #3585a4 !important; font-weight: 700 !important">
          Change
        </h4>        
      </span>
    </PopoverButton>

    <transition enter-active-class='transition duration-200 ease-out' enter-from-class='opacity-0 translate-y-1' enter-to-class='opacity-100 translate-y-0'
                leave-active-class='transition duration-150 ease-in' leave-from-class='opacity-100 translate-y-0' leave-to-class='opacity-0 translate-y-1'>
      <PopoverPanel v-slot='{ close }'
                    class='absolute left-full z-10 px-2 mt-3 w-screen max-w-xs transform -translate-x-full rtl:left-auto rtl:right-full rtl:translate-x-full sm:px-0'>
        <div class='overflow-hidden bg-white rounded-lg ring-1 ring-black ring-opacity-5 shadow-lg'>
          <ul
            class='overflow-y-scroll max-h-96 divide-y divide-accent-color-50 scrollbar scrollbar-thumb-accent-color-400 scrollbar-thin scrollbar-track-accent-color-50 scrollbar-thumb-rounded-full'
            role='list'>
            <li v-for='address in this.addresses' :key='address.id' class='px-6 py-5 cursor-pointer hover:bg-gray-50'
                @click='this.setCurrentAddressAction(address); close()'>
              <div class='flex justify-between items-center space-x-3'>
                <div class='flex-1 min-w-0'>
                  <p class='mt-1 font-bold text-second-color-600'>
                    {{ address.description }}
                  </p>
                </div>
              </div>
              <p class='mt-1 text-sm text-second-color-600'>
                {{ address.address }}
              </p>
            </li>
          </ul>
        </div>
      </PopoverPanel>
    </transition>
  </Popover>
</template>

<script>
import { Popover, PopoverButton, PopoverPanel } from '@headlessui/vue'
import { LocationMarkerIcon, PlusIcon } from '@heroicons/vue/outline'
import { mapState, mapActions, mapGetters } from 'vuex'


export default {
  components: {
    Popover,
    PopoverButton,
    PopoverPanel,
    LocationMarkerIcon,
    PlusIcon,
  },

  mounted() {
    this.getAddressesAction()
  },
  computed: {
    ...mapState('user', {
      addresses: state => state.addresses,
      address: state => state.address,
    }),
    ...mapGetters('user', ['getAddress']),
  },
  methods: {
    ...mapActions('user', ['getAddressesAction', 'setCurrentAddressAction', 'toggleAddressPickerAction']),
  },
}
</script>