<!-- NO JS -->

<!-- we get hello three times because what we're doing is in our feedback list:
  
  <script>
  import FeedbackItem from './FeedbackItem.svelte'
  export let feedback = []
</script>

{#each feedback as fb (fb.id)}
  <FeedbackItem item={fb} />
{/each} 

we're get we're bringing in our feedback we're looping through and we're displaying the feedback item 

In the feedback item we have our card component:

<script>
  import Card from './Card.svelte'
  export let item
</script>

<Card>Hello</Card>

and then we have whatever we want to display in the card passed in 
here it's just hello obviously it's going to be the item ultimately -->
<div class="card">
  <slot></slot>
</div> 

<style>
  .card{
  background-color: #fff;
  color: #d35400;
  border-radius: 15px;
  padding: 40px 50px;
  margin: 20px 0;
  position: relative;
  }
</style>