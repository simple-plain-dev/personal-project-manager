<script lang="ts">
	import * as Tabs from '$lib/components/ui/tabs';
	import * as Card from '$lib/components/ui/card';
	import { Label } from '$lib/components/ui/label';
	import { Input } from '$lib/components/ui/input';
	import { Checkbox } from '$lib/components/ui/checkbox';
  import { Button } from '$lib/components/ui/button';
</script>

<h1 class="block text-center h-full p-2 font-bold text-2xl">Personal Project Manager</h1>

<Tabs.Root value="register" class="container max-w-sm" >
  <Tabs.List class="grid w-full grid-cols-2" >
    <Tabs.Trigger value="register">Register</Tabs.Trigger>
    <Tabs.Trigger value="login">Login</Tabs.Trigger>
  </Tabs.List>
  <Tabs.Content value="register">
    <Card.Root> 
      <Card.Header> 
        <Card.Title>Register Form</Card.Title>
        <Card.Description>Fill in this form to register</Card.Description>
      </Card.Header>
      <Card.Content> 
        <form action="?/register" method="post" class="flex flex-col gap-2">
          <Label for="email" >Email</Label>
          <Input name="email" />
          <Label for="password">Password</Label>
          <Input name="password" type="password" />
          <Label for="confirmPassword">Confirm Password</Label>
          <Input name="confirmPassword" type="password" />
          <Label class="py-1" >
            <Checkbox class="align-bottom" /> Accept terms and conditions
          </Label>
          <Button type="submit" >Register</Button>
        </form>
      </Card.Content>
    </Card.Root>

  </Tabs.Content>
  <Tabs.Content value="login">
    <Card.Root> 
      <Card.Header> 
        <Card.Title>Register Form</Card.Title>
        <Card.Description>Fill in this form to register</Card.Description>
      </Card.Header>
      <Card.Content> 
        <form action="?/register" method="post" class="flex flex-col gap-2">
          <Label for="email" >Email</Label>
          <Input name="email" />
          <Label for="password">Password</Label>
          <Input name="password" type="password" />
          <Button type="submit" >Login</Button>
        </form>
      </Card.Content>
    </Card.Root>
  </Tabs.Content>
</Tabs.Root>