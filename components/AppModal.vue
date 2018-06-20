<template>
  <transition name="modal">
    <div class="modal-mask">
      <div class="modal-wrapper">
        <div class="modal-container">
          <hgroup>
            <div class="screenshots">
              <slot name="screenshots"></slot>
            </div>
            <vgroup class="preview">
                <slot name="header"></slot>
                <vgroup class="body">
                  <slot name="body"></slot>
                </vgroup>
            </vgroup>
            <vgroup class="details">
                <h4>Developer:</h4>
                <span>Height Advantage Games</span>
                <h4>Available On:</h4>
                <span>IOS / Android</span>
                <h4>Release Date:</h4>
                <span><slot name="release"></slot></span>

                <h5><a onclick="gotoTrailer()">Trailer</a></h5>
            </vgroup>
        </hgroup>


          <div class="modal-body">
          </div>

          <div class="modal-footer">
            <slot name="footer">
              <button class="modal-default-button" @click="$emit('close')">
                close
              </button>
            </slot>
          </div>
        </div>
      </div>
    </div>
  </transition>

</template>

<script>
</script>

<style>
.screenshots {
  width:220px;
}
.preview {
  padding: 10px;
}
.details {
    min-width: 250px;
    padding: 27px 10px;
}
.details h4 {
  text-transform: uppercase;
  margin-top: 20px;
}
.screenshots img {
  width:220px;
  height:363px
}
.body {
  color: #fff;
}

.modal-mask {
  position: fixed;
  z-index: 9998;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, .5);
  display: table;
  transition: opacity .3s ease;
}

.modal-wrapper {
  display: table-cell;
  vertical-align: middle;
}

.modal-container {
  max-width: 1080px;
  width: 80%;
  margin: 0px auto;
  padding: 20px 30px;
  background: #333 url("~/assets/images/background.png");
  border-radius: 2px;
  border: 5px solid #fff;
  box-shadow: 0 2px 8px rgba(0, 0, 0, .33);
  transition: all .3s ease;
  font-family: Helvetica, Arial, sans-serif;
  text-align: left;
}

.modal-header h3 {
  margin-top: 0;
  color: #42b983;
}

.modal-body {
  margin: 20px 0;
}

.modal-default-button {
  float: right;
      border: none;
    background: none;
    color: #aaa;
    cursor: pointer;
    font-weight: bold;
    margin-top: -15px;
}

/*
 * The following styles are auto-applied to elements with
 * transition="modal" when their visibility is toggled
 * by Vue.js.
 *
 * You can easily play with the modal transition by editing
 * these styles.
 */

.modal-enter {
  opacity: 0;
}

.modal-leave-active {
  opacity: 0;
}

.modal-enter .modal-container,
.modal-leave-active .modal-container {
  -webkit-transform: scale(1.1);
  transform: scale(1.1);
}

.details h4 {
  color: #aaa;
}
.details span {
  color: #fff;
  font-size: 18px;
}
</style>
