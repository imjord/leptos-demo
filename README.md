# leptos-demo


use leptos::prelude::*;

fn main() {
    leptos::mount::mount_to_body(|| {
        view! {
            <>
                // Navbar
                <nav class="navbar">
                    <div class="nav-logo">"MySite"</div>
                    <ul class="nav-links">
                        <li><a href="#home">"Home"</a></li>
                        <li><a href="#about">"About"</a></li>
                        <li><a href="#contact">"Contact"</a></li>
                    </ul>
                </nav>

                // Landing section
                <section id="home" class="landing">
                    <h1>"Welcome to MySite"</h1>
                    <p>"A super simple Leptos landing page"</p>
                    <button class="cta">"Get Started"</button>
                </section>
            </>
        }
    })
}


//css

body {
    margin: 0;
    font-family: Arial, sans-serif;
}

/* Navbar */
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: #333;
    padding: 1rem;
}

.nav-logo {
    color: white;
    font-size: 1.5rem;
    font-weight: bold;
}

.nav-links {
    list-style: none;
    display: flex;
    gap: 1rem;
    margin: 0;
    padding: 0;
}

.nav-links a {
    color: white;
    text-decoration: none;
}

.nav-links a:hover {
    text-decoration: underline;
}

/* Landing */
.landing {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 90vh;
    background: linear-gradient(135deg, #6b73ff, #000dff);
    color: white;
    text-align: center;
}

.cta {
    margin-top: 1.5rem;
    padding: 0.75rem 1.5rem;
    font-size: 1rem;
    border: none;
    border-radius: 4px;
    background: #ff4081;
    color: white;
    cursor: pointer;
}

.cta:hover {
    background: #e73370;
}

