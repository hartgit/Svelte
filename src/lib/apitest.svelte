<script>
    let img;
    const baseurl = "https://api.unsplash.com";

    fetch(`${baseurl}/search/photos/?client_id=D82-RRjMGYl6d9Np2EA4QhTgfEU7WX3sLi4Yq5vGwkM&query=storm`)
    .then(res => res.json())
    .then(data => {
        img = data.results[0].urls.full;
        console.log(img);
    })
  </script>

  