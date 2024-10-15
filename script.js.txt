async function loadAds() {
    const response = await fetch('http://localhost:3000/api/ads');
    const ads = await response.json();
    const adsContainer = document.getElementById('ads-container');
    adsContainer.innerHTML = ''; // Clear previous ads
    ads.forEach(ad => {
        adsContainer.innerHTML += `
            <div class="ad">
                ${ad.content}
            </div>`;
    });
}
loadAds();

document.getElementById('login-btn').addEventListener('click', function() {
    alert('Login functionality will be implemented later.');
});

document.getElementById('register-btn').addEventListener('click', function() {
    alert('Registration functionality will be implemented later.');
});
