# Playkeyboard_AppTech_EarlyBird

<button id="shareButton" data-url="https://apps.apple.com/kr/app/%ED%94%8C%EB%A0%88%EC%9D%B4%ED%82%A4%EB%B3%B4%EB%93%9C-%ED%8F%B0%ED%8A%B8-%ED%85%8C%EB%A7%88-%ED%82%A4%EB%B3%B4%EB%93%9C%EB%B0%B0%EA%B2%BD-%EC%9D%B4%EB%AA%A8%ED%8B%B0%EC%BD%98/id1552856161">공유</button>

<script>
document.addEventListener("DOMContentLoaded", function() {
    document.querySelector("#shareButton").addEventListener("click", function(event) {
        event.preventDefault();
        
        const urlToShare = event.target.getAttribute("data-url");

        if (navigator.share) {
            navigator.share({
                title: document.title,
                url: urlToShare
            }).then(() => {
                console.log('Thanks for sharing!');
            }).catch(console.error);
        } else {
            alert('Sharing not supported');
        }
    });
});
</script>
