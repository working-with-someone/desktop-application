<script>
  const winControl = (action) => {
    window.electronAPI.winControl(action);
  };
</script>

<div class="win-control-btns">
  <button class="win-control-btn close" on:click={() => winControl("close")}>
    <!-- <i class="fa-solid fa-xmark" /> -->
  </button>
  <button
    class="win-control-btn minimize"
    on:click={() => winControl("minimize")}
  >
    <!-- <i class="fa-solid fa-minus" /> -->
  </button>
  <button
    class="win-control-btn maximize"
    on:click={() => winControl("maximize")}
  >
    <!-- <i class="fa-solid fa-compress" /> -->
  </button>
</div>

<style lang="scss">
  .win-control-btns {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    margin: 20px 15px;
    button.win-control-btn {
      width: 15px;
      height: 15px;
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 3px;

      &.close {
        background-color: #fb5d4f;
      }
      &.minimize {
        background-color: #fdc033;
      }
      &.maximize {
        background-color: #00ce4e;
      }
    }
  }
</style>
