document.addEventListener('DOMContentLoaded', function() {
    const buttons = document.querySelectorAll('.buy-btn');
    const phone = '91XXXXXXXXX'; // Replace with your number

    buttons.forEach(btn => {
        btn.addEventListener('click', function() {
            const product = this.dataset.product;
            const message = encodeURIComponent(`Hi, order ${product} from Majuli Fish Pickle website.`);
            window.open(`https://wa.me/${phone}?text=${message}`, '_blank');
        });
    });

    // Smooth scroll for nav
    document.querySelectorAll('nav a').forEach(anchor => {
        anchor.addEventListener('click', function(e) {
            e.preventDefault();
            document.querySelector(this.getAttribute('href')).scrollIntoView({ behavior: 'smooth' });
        });
    });
});
