<script setup lang="ts">
import { Button } from '@/components/ui/button'
import { Input } from '@/components/ui/input'
import { Label } from '@/components/ui/label'
</script>

<template>
  <div class="relative w-full h-screen overflow-hidden flex items-center justify-center">
    <video class="absolute top-0 left-0 w-full h-full object-cover" autoplay muted loop>
      <source src="./assets/WhatsApp Video 2024-07-25 at 16.13.17.mp4" type="video/mp4"/>
    </video>
    <div class="absolute top-0 left-0 w-full h-full bg-black opacity-60"></div>
    <div class="relative z-10 w-full max-w-md">
      <div class="grid gap-4 bg-white p-8 rounded-2xl shadow-md h-full ">
        <div class="grid gap-2 text-center">
          <h1 class="text-3xl font-bold">
            ZAP DIGITAL NERD
          </h1>
          <p class="text-balance text-muted-foreground">
            Bem vindo!
          </p>
        </div>
        <div class="grid gap-4">
          <div class="grid gap-2">
            <Label for="email">Email</Label>
            <Input
              id="email"
              type="email"
              placeholder="m@example.com"
              required
            />
          </div>
          <div class="grid gap-2">
            <div class="flex items-center">
              <Label for="password">Senha</Label>
            </div>
            <Input id="password" type="password" required />
          </div>
          <Button type="submit" class="w-full">
            Login
          </Button>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
video {
  object-fit: cover;
}
</style>
