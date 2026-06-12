CineMagic - Movie Experience Platform
A Modern, Responsive Web Application for Movie Discovery

Project Overview
CineMagic is a fully responsive, single-page web application for movie discovery.
Built with pure HTML5, CSS3, and vanilla JavaScript, it features a dynamic hero slider, real-time search, genre filtering,
and interactive movie cards with detailed modal views.

Key Features
Dynamic Hero Slider – Auto-rotating showcase of featured movies
Live Search – Real-time movie title filtering
Genre Filtering – Filter by Action, Drama, Comedy, Sci-Fi, Thriller
Interactive Cards – Hover effects with preview overlays
Movie Modal – Detailed view with cast and director info
Fully Responsive – Optimized for all screen sizes

Technology Stack
HTML5 – Semantic document structure
CSS3 – Flexbox/Grid, animations, responsive design
Vanilla JavaScript – Dynamic rendering, event handling, DOM manipulation
Font Awesome 6 – Icon system
Google Fonts – Poppins & Montserrat typography

cinemagic/
└── index.html          # Complete application (HTML/CSS/JS)

Movie Database
The application includes 8 curated movies:

1. Dune: Part Two (2024) – Rating: 8.7
Genres: Sci-Fi, Action, Drama
Director: Denis Villeneuve
Cast: Timothée Chalamet, Zendaya, Rebecca Ferguson, Josh Brolin
Duration: 2h 46m

2. Oppenheimer (2023) – Rating: 8.3
Genres: Drama, Thriller
Director: Christopher Nolan
Cast: Cillian Murphy, Emily Blunt, Matt Damon, Robert Downey Jr.
Duration: 3h

3. John Wick: Chapter 4 (2023) – Rating: 7.8
Genres: Action, Thriller
Director: Chad Stahelski
Cast: Keanu Reeves, Donnie Yen, Bill Skarsgård, Laurence Fishburne
Duration: 2h 49m

Key Code Examples
Movie Data Structure
{
    id: 1,
    title: "Dune: Part Two",
    year: 2024,
    rating: 8.7,
    genre: ["sci-fi", "action", "drama"],
    duration: "2h 46m",
    director: "Denis Villeneuve",
    cast: ["Timothée Chalamet", "Zendaya"]
}

Star Rating Generator
function generateStarRating(rating) {
    const fullStars = Math.floor(rating / 2);
    let starsHTML = '';
    for (let i = 0; i < 5; i++) {
        starsHTML += i < fullStars ? '<i class="fas fa-star"></i>' 
                                   : '<i class="far fa-star"></i>';
    }
    return starsHTML;
}

Genre Filter Implementation

filterButtons.forEach(button => {
    button.addEventListener('click', () => {
        const filter = button.dataset.filter;
        movieCards.forEach(card => {
            card.style.display = (filter === 'all' || 
                card.dataset.genre.includes(filter)) ? 'block' : 'none';
        });
    });
});

Browser Support
All modern browsers are supported:
Chrome (version 90 and above)
Firefox (version 88 and above)
Safari (version 14 and above)
Edge (version 90 and above)


© 2024 CineMagic Project | Made with love for movie lovers worldwide











