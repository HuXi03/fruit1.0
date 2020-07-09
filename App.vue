<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
	uni-checkbox .uni-checkbox-input {
	        border-radius: 50% !important;
	        color: #ffffff !important;
	    }
	    
	    uni-checkbox .uni-checkbox-input.uni-checkbox-input-checked {
	        color: #fff;
	        border-color: rgb(255, 43, 1);
	        background:rgb(250, 0, 0);
	    }
	    uni-checkbox .uni-checkbox-input.uni-checkbox-input-checked:after{
	        font-size: 18px;
	    }
</style>
