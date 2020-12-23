<template class="red">
    <div>
        <v-container>
            <v-alert 
                v-model="error"
                type="error"
                dismissible
                border="left"
                elevation="2"
                v-show="error"
                >
                 File size is too big.
            </v-alert>
            <div class="mb-8">
                <h1 class="float-left">Step 2</h1>
                <v-btn class="float-right red" depressed @click="$router.push('/register/particulars')">
                    &larr; Back</v-btn>
            </div>
            <v-row>
                <v-col cols="12" md="6" offset-md="4">
                    <h2>Upload An Image</h2>
                    <div class="image-preview mt-4">
                        <img src="@/assets/no-image.png" ref="thumbnail" alt="">
                    </div>
                    <input type="file" name="profile-photo" id="profile-photo" ref="profile-photo-input" accept=".jpg, .jpeg, .png" @change="getFile">
                    <v-btn @click="selectImage" class="mt-4 mx-auto select-photo-btn light-green darken-3">Select Image 
                        <v-icon color="white">mdi-image</v-icon>
                     </v-btn>
                    <v-btn class="mt-4 mx-auto teal darken-3" dark block>Submit</v-btn>
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>

<script>
export default {
    name: "ProfilePhoto",
    data(){
        return {
            error: false
        }
    },
    methods: {
        selectImage(){
            this.$refs['profile-photo-input'].click();
        },
        getFile(e){
            let file = e.target.files[0];
            console.log(file);
            let imageFileSize = this.checkImageFileSize(file);

            if (imageFileSize > 1) {
                this.error = !this.error
                return;
            } else {
                this.error = false;
                this.$refs["thumbnail"].classList.add("obj");
                this.$refs["thumbnail"].file = file;

                const reader = new FileReader();
                reader.onload = (function(aImg) { return function(e) { aImg.src = e.target.result; }; })(this.$refs["thumbnail"]);
                reader.readAsDataURL(file);
                console.log(e.target.result);
            }
        },
        checkImageFileSize(file){
            let size = file.size;
            return parseInt(size / 1024);
        }
    }
}
</script>

<style>
    #profile-photo {
        display: none;
    }

    .image-preview {
        height: 350px;
        width: 350px;
    }

    img {
        display: inline-block;
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: center;
    }

    .select-photo-btn {
        display: inline-block;
    }
</style>