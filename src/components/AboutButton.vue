<template>
  <div class="inset-0">
    <h3 class="text-white float-right underline-animation hover:cursor-pointer" @click="openModal">
      📒 About
    </h3>
  </div>

  <TransitionRoot appear :show="isOpen" as="template">
    <Dialog as="div" @close="closeModal">
      <div class="fixed inset-0 z-10 overflow-y-auto">
        <div class="min-h-screen text-center">
          <TransitionChild
            as="template"
            enter="duration-300 ease-out"
            enter-from="opacity-0"
            enter-to="opacity-100"
            leave="duration-200 ease-in"
            leave-from="opacity-100"
            leave-to="opacity-0"
          >
            <DialogOverlay class="fixed inset-0"/>
          </TransitionChild>

          <span class="inline-block h-screen align-middle" aria-hidden="true">
            &#8203;
          </span>

          <TransitionChild
            as="template"
            enter="duration-300 ease-out"
            enter-from="opacity-0 scale-95"
            enter-to="opacity-100 scale-100"
            leave="duration-200 ease-in"
            leave-from="opacity-100 scale-100"
            leave-to="opacity-0 scale-95"
          >
            <div
              class="inline-block w-11/12 sm:w-5/6 lg:w-3/4 p-6 my-8 overflow-hidden text-left align-middle transition-all transform bg-white shadow-xl rounded-2xl"
            >
              <DialogTitle>
                <h2 class="text-center">About Me</h2>
              </DialogTitle>

              <div class="divide-y divide-gray-300 divide-solid flex flex-col">
                <span></span>
                <span></span>
              </div>

              <div class="dialog-section">
                <h4>Education</h4>
                <p class="ml-8">
                  NTUT Junior studying Electrical Engineering and Computer Science
                </p>
              </div>

              <div class="dialog-section">
                <h4>Skills & Interests</h4>
                <ul class="list-disc">
                  <li>Programming: Started programming since 2016, currently with experience in frontend and app development, willing to learn different skills in the future.</li>
                  <li>Speedcubing: 7 years of experience in attending and holding WCA competitions, and contributing the Rubik's cube community in Taiwan.</li>
                  <li>Table Tennis: Started learning table tennis in elementary school, currently an amateur player.</li>
                  <li>Cats: Follow my cat Pudding <a href="https://instagram.com/pudding_cat_123456/">here</a></li>
                </ul>
              </div>

              <div class="dialog-section">
                <h4>Experiences</h4>
                <ul class="list-disc">
                  <li>3x3 FMC event 1st place in <a href="https://www.worldcubeassociation.org/competitions/MaruCubeDay2017">Maru Cube Day 2017</a></li>
                  <li>Organizer of <a href="https://www.worldcubeassociation.org/competitions/CKCubingParty2018">CK Cubing Party 2018</a></li>
                  <li>Organizer of <a href="https://www.worldcubeassociation.org/competitions/ZhuyuangangOpen2019">Zhuyuangang Open 2019</a></li>
                  <li>Organizer of <a href="https://www.worldcubeassociation.org/competitions/ZhuyuangangOpen2020">Zhuyuangang Open 2020</a></li>
                  <li><a href="https://ntut.club/">NTUT Programming Club</a> 4th President</li>
                  <li>Google Developer Student Club Lead of NTUT (2020 - 2021)</li>
                  <li>Volunteer of <a href="https://sitcon.org/2021/">SITCON 2021</a></li>
                </ul>
              </div>

              <div class="mt-20 text-center">
                <button
                  type="button"
                  class="inline-flex justify-center px-4 py-2 text-sm font-medium text-blue-900 bg-blue-100 border border-transparent rounded-md hover:bg-blue-200 focus:outline-none focus-visible:ring-2 focus-visible:ring-offset-2 focus-visible:ring-blue-500 hover:cursor-pointer duration-150"
                  @click="closeModal"
                >
                  Back
                </button>
              </div>
            </div>
          </TransitionChild>
        </div>
      </div>
    </Dialog>
  </TransitionRoot>
</template>

<script>
import {defineComponent, ref} from "vue";
import {
  TransitionRoot,
  TransitionChild,
  Dialog,
  DialogOverlay,
  DialogTitle,
} from '@headlessui/vue'

export default defineComponent({
  name: "AboutButton",
  components: {
    TransitionRoot,
    TransitionChild,
    Dialog,
    DialogOverlay,
    DialogTitle,
  },
  setup() {
    const isOpen = ref(false)

    return {
      isOpen,
      closeModal() {
        isOpen.value = false
      },
      openModal() {
        isOpen.value = true
      },
    }
  },
});
</script>

<style scoped>
.dialog-section {
  @apply mt-2 sm:ml-8 lg:ml-16;
}
</style>