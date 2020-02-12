<script>
  export let todo;
</script>

<style>
  label {
    padding: 15px 30px;
    padding-left: 40px;
    vertical-align: text-top;
    position: relative;
    cursor: pointer;
  }

  label:focus > span {
    box-shadow: 0 0 0 3px rgba(0, 0, 0, 0.12);
  }

  input {
    position: absolute;
    opacity: 0;
  }

  label:hover > span,
  input:checked ~ span {
    background-color: #c3d8e6;
  }

  input:checked ~ span:after {
    display: inline-block;
  }

  span {
    position: absolute;
    top: 32px;
    left: 3px;
    height: 25px;
    width: 25px;
    background-color: #eee;
  }

  span:after {
    content: "";
    position: absolute;
    display: none;
    margin-right: 10px;
    left: 9px;
    top: 5px;
    width: 5px;
    height: 10px;
    border: solid black;
    border-width: 0 3px 3px 0;
    -webkit-transform: rotate(45deg);
    -ms-transform: rotate(45deg);
    transform: rotate(45deg);
  }
</style>

<label>
  {todo.content}
  <input type="checkbox" class="checkbox" />
  <span />
</label>
