<p align="center">
    <img src="/assets/img/logo-80x82.png" alt="Jonathan Lovera"/>
    <br>
    <h1>Jonathan Lovera's Portfolio</h1>
</p>

instagram-php-scraper is a simple file written in PHP that scrapes and show in a JSON format an instagram user's photos, likes, videos, etc. Use responsibly.

# Installation
1. Clone the repository
`git clone https://github.com/jonlov/jonlov.github.io.git`

2. Copy the index.php file into a folder

3. Change $user variable in the php file for the user that you would like to get information
`$user = "USERNAME_HERE";`

# Basic Usage
You could make a Javascript file which reads the information from the JSON
`function instagramAjax() {
    return $.ajax({
        type: "GET",
        // REPLACE THIS WITH THE URL OF THE INDEX FILE
        // url: "api/instagram/",
        url: "api/instagram/example.json",
        dataType: 'json',
        success: function(res) {
            // Just console.log the res or have a look to the example.json
            // to see all the information that it brings

            // console.log(res);
            // display_src
            // thumbnail_src
            // likes
            // date
            // is_video
            // caption

            var html = '';
            // For 9 images do the following
            for (var i = 0; i < 9; i++) {
                // This will be the url of a picture
                // 'https://www.instagram.com/p/' + res[i].code + '/'

                // This will be the png file of a picture
                // res[i].display_src
            }
        },
        error: function(res) {
            // console.log(res);
        }
    });
}`

Done!

# License

This project is licensed under [MIT](https://github.com/jonlov/instagram-php-scraper/blob/master/LICENSE).
