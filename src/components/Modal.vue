<template>
    <div class="modal" v-show="showModal">
        <div class="mask">
            <div class="modal-dialog">
                <div class="modal-header">
                    <span>标题</span>
                    <a href="javascript:;" class="icon-close"></a>
                </div>
                <div class="modal-body">
                    <slot name="body"></slot>
                </div>
                <div class="modal-footer">
                    <div class="btn-group">
                        <a href="javascript:;" class="btn">确定</a>
                        <a href="javascript:;" class="btn">取消</a>
                    </div>
                    
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    export default{
        name:'modal',
        props:{
            //弹框类型:小small、中midlle、大large表单
            modalType:{
                type:String,
                default:'form'
            },
            //弹框标题
            title:String,
            //按钮类型：1：确定按钮2：取消按钮
            btnType:String,
            sureText:{
                type:String,
                default:'确定'
            },
            cancelText:{
                type:String,
                default:'取消'
            },
            showModal:Boolean
        }
    }
</script>
<style lang="scss">
@import './../assets/scss/config.scss';
@import './../assets/scss/mixin.scss';
@import './../assets/scss/modal.scss';
</style>