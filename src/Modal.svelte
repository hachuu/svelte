<script>
  let showModal = false;
  let isPromo = true;

  const toggleModal = () => {
    showModal = !showModal;
  }
</script>

<button on:click="{toggleModal}">Show Modal</button>
{#if showModal}
<div class="backdrop" class:promo={isPromo}>
  <div class="modal">
    <p on:click="{toggleModal}">Modal is here!</p>
    <input type="time" id="appt" name="appt"
       min="09:00" max="18:00" required>
  </div>
</div>
{/if}
<style> 
  .backdrop {
    width: 100%;
    height: 100%;
    position: fixed;
    top: 0;
    left: 0;
    background: rgba(0, 0, 0, 0.8);
  }   
  .modal {
    padding: 10px;
    border-radius: 10px;
    max-width: 400px;
    margin: 10% auto;
    text-align: center;
    background: white;
  }
  .promo .modal {
    background: gray;
    color: white;
  }
</style>