<template>
    <div>
        <!--สร้างบาร์เมนู-->
        <b-navbar type="dark" variant="dark"> 
            <b-navbar-nav>
                <nuxt-link clss="nav-item nav-link" to="/" >หน้าหลัก</nuxt-link>
                <nuxt-link clss="nav-item nav-link" to="/posts" >บทความ</nuxt-link>
                <nuxt-link clss="nav-item nav-link" to="/admin" >ผู้เขียน</nuxt-link>
            </b-navbar-nav>
        </b-navbar>
        <nuxt/>
    </div>
</template>