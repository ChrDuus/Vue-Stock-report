<template>
    <div class="BaseCard">

        <slot></slot>
    </div>

</template>

<script>
export default{
    name: 'BaseCard',
    components:{

    }
}

</script>

<style>
.BaseCard{
    border-radius: 16px;
    background-color: #011F35;
    padding: 24px 32px;

}

</style>