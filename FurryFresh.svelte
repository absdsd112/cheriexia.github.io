<script>
    let menuItems = {
        dogs: [
            { name: "Senior", img: "SeniorDog.png", alt: "Pet Food - Duck & Chicken" },
            { name: "Adult", img: "AdultDog.png", alt: "Pet Food - Salmon & Chicken" },
            { name: "Puppy", img: "puppy.png", alt: "Pet Food - Chicken & Turkey" }
        ],
        cats: [
            { name: "Senior", img: "SeniorCat.png", alt: "Pet Food - Chicken & Turkey" },
            { name: "Adult", img: "Adultcat.png", alt: "Pet Food - Chicken & Turkey" },
            { name: "Kitten", img: "Kitten.png", alt: "Pet Food - Chicken & Turkey" }
        ]
    };
</script>

<style>
    

    header {
        background-color: #ff6b81;
        padding: 20px;
        color: white;
        font-size: 24px;
    }

    nav {
        max-width: 1200px;
        margin: 0 auto;
    }

    .nav-links {
        list-style: none;
        padding: 0;
        margin: 0;
        display: flex;
        justify-content: center;
        gap: 20px;
    }

    .nav-links li {
        display: inline;
    }

   

    .hero {
        margin: 30px 0;
    }

    .features {
        margin: 20px auto;
    }

    .features ul {
        list-style: none;
        padding: 0;
    }

    .menu {
        text-align: center;
        margin-top: 20px;
    }

    .menu h3 {
        text-align: left;
        width: 80%;
        font-size: 20px;
        font-weight: bold;
        color: #333;
        margin: 10px auto;
    }

    .menu-category {
        display: flex;
        justify-content: center;
        gap: 10px;
        flex-wrap: wrap;
        margin-bottom: 30px;
    }

    .menu-item {
        text-align: center;
        flex: 0 1 100px;
    }

    .menu-item img {
        width: 120px;
        height: auto;
        border-radius: 10px;
        box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        transition: transform 0.3s ease-in-out;
    }

    .menu-item img:hover {
        transform: scale(1.05);
    }

    .menu-item p {
        font-size: 18px;
        font-weight: bold;
        color: #333;
        margin-top: 10px;
    }
</style>

<header>
    <nav>
        <ul class="nav-links">
            <li>Woosf Shop</li>
            <li>Meow Shop</li>
            <li>Pet Club</li>
            <li>About Us</li>
            <li>Log In</li>
            <li>Cart</li>

        </ul>
    </nav>
</header>

<section class="hero">
    <h2>Love Starts with Fresh, Healthy Food</h2>
    <p>At Furry Fresh, we only offer natural nutrition for the pets you love.</p>
</section>

<section class="features">
    <h3>Why Choose Us?</h3>
    <ul>
        <li>Meat As Number #1</li>
        <li>Better Flavour for Pets</li>
        <li>Local Productions</li>
        <li>Organic Products</li>
    </ul>
</section>

<section class="menu">
    <h3>Daily Menu For Dogs</h3>
    <div class="menu-category">
        {#each menuItems.dogs as item}
            <div class="menu-item">
                <p>{item.name}</p>
                <img src={item.img} alt={item.alt}>
            </div>
        {/each}
    </div>

    <h3>Daily Menu For Cats</h3>
    <div class="menu-category">
        {#each menuItems.cats as item}
            <div class="menu-item">
                <p>{item.name}</p>
                <img src={item.img} alt={item.alt}>
            </div>
        {/each}
    </div>
</section>

<footer>
    <p>© 2024 Furry Fresh. All rights reserved.</p>
</footer>
