<script setup lang="ts">
import { ref } from 'vue'
import img1 from '../assets/product/1.png'
import img2 from '../assets/product/2.png'
import img3 from '../assets/product/3.png'
import img4 from '../assets/product/4.png'
import img5 from '../assets/product/5.png'
import img6 from '../assets/product/6.png'

const active = ref<boolean>(false);
const toggle = () => active.value = !active.value 
</script>

<template>
    <!-- 商品列表容器 -->
    <div class="container">
        <!-- 总标题 -->
        <h3 class="title">organic products</h3>

        <!-- 商品容器 -->
        <div class="products-container">

            <!-- 商品 -->
            <div class="product" data-name="p-1" @click="toggle">
                <img :src="img1" alt="">
                <h3>strawberries</h3>
                <div class="price">$2.00</div>
            </div>

            <!-- 商品 -->
            <div class="product" data-name="p-2">
                <img :src="img2" alt="">
                <h3>strawberries</h3>
                <div class="price">$2.00</div>
            </div>
            <!-- 商品 -->
            <div class="product" data-name="p-3">
                <img :src="img3" alt="">
                <h3>strawberries</h3>
                <div class="price">$2.00</div>
            </div>
            <!-- 商品 -->
            <div class="product" data-name="p-4">
                <img :src="img4" alt="">
                <h3>strawberries</h3>
                <div class="price">$2.00</div>
            </div>
            <!-- 商品 -->
            <div class="product" data-name="p-5">
                <img :src="img5" alt="">
                <h3>strawberries</h3>
                <div class="price">$2.00</div>
            </div>
            <!-- 商品 -->
            <div class="product" data-name="p-6">
                <img :src="img6" alt="">
                <h3>strawberries</h3>
                <div class="price">$2.00</div>
            </div>

        </div>
    </div>
    <!-- 商品预览容器 -->
    <div class="products-preview" :class="{ active }">

        <!-- 预览块 -->
        <div class="preview" data-target="p-1" :class="{ active }">
            <!-- 商品名 -->
            <img :src="img1" alt="">
            <!-- 商品标题 -->
            <h3>organic strawberries</h3>
            <!-- 商品星级 -->
            <div class="star">
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star-half-alt"></i>
                <span>( 250 )</span>
            </div>
            <!-- 商品描述 -->
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Soluta quo praesentium temporibus laudantium
                repudiandae eos repellendus voluptate accusantium ipsa obcaecati, inventore vel pariatur corporis
                dolore, rem dicta mollitia illo libero.</p>
            <!-- 商品价格 -->
            <div class="price">$2.00</div>
            <!-- 操作 -->
            <div class="buttons">
                <a href="" class="buy">buy now</a>
                <a href="" class="cart">add to cart</a>
            </div>
        </div>
        <!-- 预览块 -->
        <div class="preview" data-target="p-2">
            <!-- 商品名 -->
            <img :src="img2" alt="">
            <!-- 商品标题 -->
            <h3>organic strawberries</h3>
            <!-- 商品星级 -->
            <div class="star">
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star-half-alt"></i>
                <span>( 250 )</span>
            </div>
            <!-- 商品描述 -->
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Soluta quo praesentium temporibus laudantium
                repudiandae eos repellendus voluptate accusantium ipsa obcaecati, inventore vel pariatur corporis
                dolore, rem dicta mollitia illo libero.</p>
            <!-- 商品价格 -->
            <div class="price">$2.00</div>
            <!-- 操作 -->
            <div class="buttons">
                <a href="" class="buy">buy now</a>
                <a href="" class="cart">add to cart</a>
            </div>
        </div>
        <!-- 预览块 -->
        <div class="preview" data-target="p-3">
            <!-- 商品名 -->
            <img :src="img3" alt="">
            <!-- 商品标题 -->
            <h3>organic strawberries</h3>
            <!-- 商品星级 -->
            <div class="star">
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star-half-alt"></i>
                <span>( 250 )</span>
            </div>
            <!-- 商品描述 -->
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Soluta quo praesentium temporibus laudantium
                repudiandae eos repellendus voluptate accusantium ipsa obcaecati, inventore vel pariatur corporis
                dolore, rem dicta mollitia illo libero.</p>
            <!-- 商品价格 -->
            <div class="price">$2.00</div>
            <!-- 操作 -->
            <div class="buttons">
                <a href="" class="buy">buy now</a>
                <a href="" class="cart">add to cart</a>
            </div>
        </div>
        <!-- 预览块 -->
        <div class="preview" data-target="p-4">
            <!-- 商品名 -->
            <img :src="img4" alt="">
            <!-- 商品标题 -->
            <h3>organic strawberries</h3>
            <!-- 商品星级 -->
            <div class="star">
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star-half-alt"></i>
                <span>( 250 )</span>
            </div>
            <!-- 商品描述 -->
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Soluta quo praesentium temporibus laudantium
                repudiandae eos repellendus voluptate accusantium ipsa obcaecati, inventore vel pariatur corporis
                dolore, rem dicta mollitia illo libero.</p>
            <!-- 商品价格 -->
            <div class="price">$2.00</div>
            <!-- 操作 -->
            <div class="buttons">
                <a href="" class="buy">buy now</a>
                <a href="" class="cart">add to cart</a>
            </div>
        </div>
        <!-- 预览块 -->
        <div class="preview" data-target="p-5">
            <!-- 商品名 -->
            <img :src="img5" alt="">
            <!-- 商品标题 -->
            <h3>organic strawberries</h3>
            <!-- 商品星级 -->
            <div class="star">
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star-half-alt"></i>
                <span>( 250 )</span>
            </div>
            <!-- 商品描述 -->
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Soluta quo praesentium temporibus laudantium
                repudiandae eos repellendus voluptate accusantium ipsa obcaecati, inventore vel pariatur corporis
                dolore, rem dicta mollitia illo libero.</p>
            <!-- 商品价格 -->
            <div class="price">$2.00</div>
            <!-- 操作 -->
            <div class="buttons">
                <a href="" class="buy">buy now</a>
                <a href="" class="cart">add to cart</a>
            </div>
        </div>
    </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Nunito:wght@200;300;400;500;600&display=swap');

body {
    background-color: #fff;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 3rem 2rem;
}

.container .title {
    font-size: 3.5rem;
    color: #444;
    margin-bottom: 3rem;
    text-transform: uppercase;
    text-align: center;
}

.container .products-container {
    display: grid;
    /* 每列的设置保持一样：自适应 最小宽度30rem，最大宽度充满 */
    grid-template-columns: repeat(auto-fit, minmax(30rem, 1fr));
    gap: 2rem;
}

.container .products-container .product {
    text-align: center;
    padding: 3rem 2rem;
    background-color: #fff;
    /* 垂直方向添加阴影 */
    box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.1);
    outline: .1rem solid #ccc;
    /* 轮廓朝内部移动 */
    outline-offset: -1.5rem;
    cursor: pointer;
}

.container .products-container .product:hover {
    outline: .1rem solid #222;
    outline-offset: 0;
}

.container .products-container .product img {
    height: 25rem;
}

.container .products-container .product img:hover {
    /* 尺寸缩放为原来的0.9倍 */
    transform: scale(.9);
}

.container .products-container .product h3 {
    font-size: 2rem;
    padding: .5rem 0;
    color: #444;
}

.container .products-container .product:hover h3 {
    color: #00f;
}

.container .products-container .product .price {
    font-size: 2rem;
    color: #444;
}

.products-preview {
    position: fixed;
    top: 0;
    left: 0;
    height: 100vh;
    width: 100%;
    background-color: rgba(0, 0, 0, 0.8);
    display: none;
    align-items: center;
    justify-content: center;
}

.products-preview.active {
    display: flex;
}

.products-preview .preview {
    display: none;
    padding: 2rem;
    text-align: center;
    background-color: #fff;
    position: relative;
    margin: 2rem;
    width: 40rem;
}

.products-preview .preview.active {
    display: inline-block;
}

.products-preview .preview img {
    height: 30rem;
}

.products-preview .preview h3 {
    color: #444;
    padding: .5rem 0;
    font-size: 2.5rem;
}

.products-preview .preview p {
    padding: 1rem 0;
    line-height: 1.5;
    font-size: 1.7rem;
    color: #777;
}

.products-preview .preview .price {
    padding: 1rem 0;
    font-size: 2.5rem;
    color: #27ae60;
}

.products-preview .preview .buttons {
    display: flex;
    flex-wrap: wrap;
    gap: 1.5rem;

    margin-top: 1rem;
}

.products-preview .preview .buttons a {
    flex: 1 1 16rem;
    padding: 1rem;
    font-size: 1.8rem;
    color: #444;
    border: .1rem solid #444;
}

.products-preview .preview .buttons a.cart {
    background-color: #444;
    color: #fff;
}

.products-preview .preview .buttons a.cart:hover {
    background-color: #111;
}

.products-preview .preview .buttons a.buy:hover {
    background-color: #111;
    color: #fff;
}
</style>