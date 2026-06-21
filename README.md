<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Cam's Barbershop</title>
<style>
    *{
        margin:0;
        padding:0;
        box-sizing:border-box;
        font-family:Arial, Helvetica, sans-serif;
        scroll-behavior:smooth;
    }

    body{
        background:#111;
        color:#fff;
        line-height:1.6;
    }

    header{
        background:linear-gradient(135deg,#000,#1f1f1f);
        border-bottom:4px solid gold;
        padding:35px 18px 25px;
        text-align:center;
    }

    .logo-circle{
        width:110px;
        height:110px;
        margin:0 auto 15px;
        border-radius:50%;
        background:gold;
        color:#111;
        display:flex;
        align-items:center;
        justify-content:center;
        font-size:42px;
        font-weight:700;
        border:4px solid #fff;
        box-shadow:0 0 25px rgba(255,215,0,.55);
    }

    h1{
        color:gold;
        font-size:clamp(2rem, 7vw, 3.2rem);
        margin-bottom:6px;
    }

    .subtitle{
        font-size:1.05rem;
        color:#e7e7e7;
    }

    nav{
        background:#000;
        border-bottom:1px solid rgba(255,215,0,.6);
        padding:12px 10px;
        text-align:center;
        position:sticky;
        top:0;
        z-index:10;
    }

    nav a{
        display:inline-block;
        margin:5px;
        padding:11px 16px;
        background:gold;
        color:#111;
        text-decoration:none;
        font-weight:700;
        border-radius:10px;
    }

    .hero{
        padding:50px 18px 40px;
        text-align:center;
        background:linear-gradient(to bottom,#151515,#0f0f0f);
    }

    .hero h2{
        color:gold;
        font-size:clamp(1.7rem, 6vw, 2.8rem);
        margin-bottom:12px;
    }

    .hero p{
        max-width:750px;
        margin:0 auto;
        font-size:1.08rem;
        color:#ededed;
    }

    .barber-pole{
        width:60px;
        height:180px;
        margin:20px auto 0;
        border-radius:30px;
        border:4px solid #fff;
        background:repeating-linear-gradient(
            -45deg,
            #d11 0px,
            #d11 18px,
            #fff 18px,
            #fff 36px,
            #1d4ed8 36px,
            #1d4ed8 54px
        );
        animation:spin 4s linear infinite;
        background-size:100% 200%;
    }

    @keyframes spin{
        from{background-position:0 0;}
        to{background-position:0 200px;}
    }

    main{
        max-width:1100px;
        margin:0 auto;
        padding:20px 16px 40px;
    }

    section{
        margin:22px 0;
    }

    .card{
        background:#1b1b1b;
        border:1px solid rgba(255,215,0,.55);
        border-radius:18px;
        padding:22px;
        box-shadow:0 10px 30px rgba(0,0,0,.18);
    }

    .section-title{
        color:gold;
        font-size:1.7rem;
        margin-bottom:12px;
    }

    .buttons{
        text-align:center;
        margin-top:18px;
    }

    .btn{
        display:inline-block;
        margin:8px 6px;
        padding:12px 18px;
        background:gold;
        color:#111;
        text-decoration:none;
        font-weight:700;
        border-radius:10px;
    }

    .btn.secondary{
        background:#2b2b2b;
        color:#fff;
        border:1px solid gold;
    }

    .grid{
        display:grid;
        grid-template-columns:repeat(auto-fit,minmax(210px,1fr));
        gap:16px;
    }

    .service, .photo, .review, .request-box{
        background:#222;
        border:1px solid rgba(255,215,0,.45);
        border-radius:16px;
        padding:18px;
    }

    .service h3,
    .review h3{
        color:gold;
        margin-bottom:8px;
    }

    .price{
        margin-top:10px;
        font-size:1.25rem;
        font-weight:700;
        color:gold;
    }

    .photo{
        min-height:170px;
        display:flex;
        flex-direction:column;
        justify-content:center;
        align-items:center;
        text-align:center;
        gap:8px;
    }

    .photo span{
        font-size:2rem;
    }

    .before-after{
        display:grid;
        grid-template-columns:repeat(auto-fit,minmax(240px,1fr));
        gap:16px;
    }

    .before, .after{
        min-height:220px;
        border-radius:16px;
        padding:18px;
        display:flex;
        flex-direction:column;
        justify-content:space-between;
        border:1px solid rgba(255,215,0,.45);
    }

    .before{
        background:linear-gradient(135deg,#2a1c1c,#1f1414);
    }

    .after{
        background:linear-gradient(135deg,#1a2a1c,#141f16);
    }

    .tag{
        display:inline-block;
        padding:6px 10px;
        border-radius:999px;
        background:gold;
        color:#111;
        font-weight:700;
        font-size:.9rem;
        width:max-content;
    }

    .reviews{
        display:grid;
        grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
        gap:16px;
    }

    .stars{
        color:gold;
        letter-spacing:2px;
        margin-bottom:8px;
    }

    form{
        display:grid;
        gap:12px;
        margin-top:10px;
    }

    input, textarea{
        width:100%;
        padding:12px 14px;
        border-radius:10px;
        border:1px solid rgba(255,215,0,.45);
        background:#111;
        color:#fff;
        outline:none;
        font-size:1rem;
    }

    textarea{
        min-height:120px;
        resize:vertical;
    }

    .footer{
        text-align:center;
        padding:24px 16px 36px;
        border-top:1px solid rgba(255,215,0,.4);
        color:#ddd;
    }

    .small{
        color:#bdbdbd;
        font-size:.95rem;
        margin-top:8px;
    }
</style>
</head>
<body>

<header>
    <div class="logo-circle">CF</div>
    <h1>Cam's Barbershop</h1>
    <div class="subtitle">Owned & Operated by Cameron Fillian</div>
</header>

<nav>
    <a href="#booking">Book Your Fresh Cut</a>
    <a href="#gallery">Haircut Gallery</a>
    <a href="#reviews">Reviews</a>
    <a href="#request">Request a Cut</a>
</nav>

<div class="hero">
    <h2>Fresh Cuts. Great Service.</h2>
    <p>
        A small barbershop in Cameron's room with a clean, professional style.
        Cam's Barbershop is all about sharp cuts, good vibes, and building a dream one haircut at a time.
    </p>
    <div class="barber-pole"></div>
</div>

<main>

    <section id="about" class="card">
        <div class="section-title">About Cameron</div>
        <p>
            Hi, my name is <strong>Cameron Fillian</strong>. Welcome to <strong>Cam's Barbershop</strong>.
            I like cutting hair, learning new styles, and making people feel fresh.
            This is my small barbershop setup in my room, and I work hard to make every cut look clean.
        </p>
    </section>

    <section id="booking" class="card">
        <div class="section-title">Ready for a Fresh Cut?</div>
        <p>
            Call or text <strong>512-993-1789</strong> to book an appointment at Cam's Barbershop.
        </p>
        <div class="buttons">
            <a class="btn" href="tel:5129931789">📞 Call Now</a>
            <a class="btn secondary" href="sms:5129931789">💬 Text to Book</a>
        </div>
        <p class="small">Ask a parent or guardian before booking.</p>
    </section>

    <section id="services" class="card">
        <div class="section-title">Services</div>
        <div class="grid">
            <div class="service">
                <h3>Basic Haircut</h3>
                <p>Clean and simple haircut for a fresh look.</p>
                <div class="price">$10</div>
            </div>
            <div class="service">
                <h3>Fade</h3>
                <p>Smooth fade with a sharp finish.</p>
                <div class="price">$15</div>
            </div>
            <div class="service">
                <h3>Line Up</h3>
                <p>Sharp edges and a crisp hairline.</p>
                <div class="price">$5</div>
            </div>
            <div class="service">
                <h3>Haircut + Line Up</h3>
                <p>Best value if you want both.</p>
                <div class="price">$15</div>
            </div>
        </div>
    </section>

<section id="gallery" class="card">
    <div class="section-title">Haircut Gallery</div>

    <div class="grid">

        <div class="photo">
            <img src="YOURPHOTO1.jpg" alt="Haircut 1" style="width:100%;border-radius:12px;">
            <h3>Fresh Fade</h3>
        </div>

        <div class="photo">
            <img src="YOURPHOTO2.jpg" alt="Haircut 2" style="width:100%;border-radius:12px;">
            <h3>Line Up</h3>
        </div>

        <div class="photo">
            <img src="YOURPHOTO3.jpg" alt="Haircut 3" style="width:100%;border-radius:12px;">
            <h3>Classic Cut</h3>
        </div>

        <div class="photo">
            <img src="YOURPHOTO4.jpg" alt="Haircut 4" style="width:100%;border-radius:12px;">
            <h3>Custom Style</h3>
        </div>

    </div>
</section>

    <section id="beforeafter" class="card">
        <div class="section-title">Before & After</div>
        <div class="before-after">
            <div class="before">
                <div class="tag">Before</div>
                <div>
                    <h3>Before the Cut</h3>
                    <p>Put a “before” photo here to show the transformation.</p>
                </div>
            </div>
            <div class="after">
                <div class="tag">After</div>
                <div>
                    <h3>After the Cut</h3>
                    <p>Put the finished haircut photo here for the clean final look.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="reviews" class="card">
        <div class="section-title">Reviews</div>
        <div class="reviews">
            <div class="review">
                <div class="stars">★★★★★</div>
                <h3>Clean and Fresh</h3>
                <p>“Great haircut and super nice service.”</p>
            </div>
            <div class="review">
                <div class="stars">★★★★★</div>
                <h3>Sharp Detail</h3>
                <p>“The fade came out really clean.”</p>
            </div>
            <div class="review">
                <div class="stars">★★★★★</div>
                <h3>Friendly Barber</h3>
                <p>“Easy to book and a great vibe.”</p>
            </div>
        </div>
    </section>

    <section id="request" class="card">
        <div class="section-title">Haircut Request Form</div>
        <p>Use this form to leave a message about the haircut you want.</p>

        <form onsubmit="event.preventDefault(); alert('Thanks! Your haircut request is ready to send.');">
            <input type="text" placeholder="Your Name" />
            <input type="tel" placeholder="Phone Number" />
            <input type="text" placeholder="Haircut Style" />
            <textarea placeholder="Tell Cam what you want for your haircut..."></textarea>
            <button class="btn" type="submit" style="border:none; cursor:pointer;">Submit Request</button>
        </form>
    </section>

    <section class="card">
        <div class="section-title">Why Choose Cam's Barbershop?</div>
        <ul style="padding-left:20px; line-height:1.9;">
            <li>Friendly and professional service</li>
            <li>Affordable prices</li>
            <li>Clean setup in a room barbershop</li>
            <li>Young entrepreneur working hard</li>
            <li>Fresh cuts with attention to detail</li>
        </ul>
    </section>

</main>

<div class="footer">
    <strong>Cam's Barbershop</strong> · Cameron Fillian
    <div class="small">Call or text 512-993-1789 to book an appointment.</div>
</div>

</body>
</html>
