<template>
    <div class="hamburgueria">
        <header>
            <h1>Deliciosos Hamburguers</h1>
        </header>
        <section class="menu">
            <h2>Cardápio</h2>
            <div class="item" v-for="(item, index) in menu" :key="index">
                <img :src="item.image" :alt="item.name" />
                <h3>{{ item.name }}</h3>
                <p>{{ item.description }}</p>
                <span class="price">{{ item.price }}</span>
            </div>
        </section>
        <footer>
            <p>&copy; 2023 Hamburgueria Delícia</p>
        </footer>
    </div>
</template>
  
<script>
export default {
    data() {
        return {
            menu: [
                {
                    name: 'Hamburguer Clássico',
                    description: 'Pão, carne, alface, tomate e queijo.',
                    price: '$10.99',
                    image: 'https://www.sabornamesa.com.br/media/k2/items/cache/bf1e20a4462b71e3cc4cece2a8c96ac8_XL.jpg',
                },
                {
                    name: 'Hamburguer Vegano',
                    description: 'Pão vegano, hambúrguer de grão de bico, alface, tomate e abacate.',
                    price: '$12.99',
                    image: 'https://www.sabornamesa.com.br/media/k2/items/cache/bf1e20a4462b71e3cc4cece2a8c96ac8_XL.jpg',
                },
                // Adicione mais itens ao cardápio aqui
            ],
        };
    },
};
</script>
  
<style scoped>
/* Estilos para a página de hamburgueria */
.hamburgueria {
    display: flex;
    flex-direction: column;
    justify-content: center;
    font-family: Arial, sans-serif;
    text-align: center;
    padding: 20px;
}

header {
    background-color: #ff8c00;
    padding: 10px;
    color: white;
}

.menu {
    margin-top: 20px;
}

.item {
    margin: 20px;
    /* padding: 20px; */
    border: 1px solid #ddd;
    border-radius: 5px;
    background-color: #f9f9f9;
}

.item img {
    max-width: 600px;
}

.price {
    font-weight: bold;
    color: #ff8c00;
}

footer {
    margin-top: 20px;
    background-color: #333;
    color: white;
    padding: 10px;
}
</style>
  