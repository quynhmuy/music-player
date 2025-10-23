# Giao diện Ứng dụng Nghe nhạc (Music Player UI)

Đây là một dự án front-end xây dựng giao diện người dùng (UI) cho một ứng dụng nghe nhạc. Dự án được code hoàn toàn bằng HTML, CSS và một chút JavaScript, tập trung vào việc mô phỏng chính xác thiết kế, có tính tương tác và đảm bảo hoạt động trên nhiều kích cỡ màn hình.

---
## 🚀 Tính năng chính

Dự án này đáp ứng đầy đủ các yêu cầu của bài tập:

* **Giao diện đầy đủ:** Giao diện 3 cột (Sidebar, Main Content, Rightbar) và thanh Player được tái hiện chính xác theo mẫu thiết kế.
* **🎨 Chuyển đổi Light / Dark Mode:** Người dùng có thể gạt nút ở thanh sidebar để chuyển đổi qua lại giữa 2 chế độ giao diện Sáng và Tối.
* **📱 Responsive UI Design:** Giao diện tự động điều chỉnh (sử dụng `@media queries`):
    * **Tablet (<= 1100px):** Ẩn cột bên phải (`rightbar`).
    * **Mobile (<= 800px):** Ẩn cả 2 cột bên, giao diện 1 cột, thanh player ghim xuống dưới.
* **✨ Hiệu ứng Transitions:** Tất cả các thành phần tương tác (nút, link, thẻ card) đều có hiệu ứng `hover` mượt mà. Hiệu ứng chuyển đổi Light/Dark mode cũng mượt mà.
* **🎬 Hiệu ứng Animations:** Trang web có hiệu ứng `fadeIn` đơn giản khi tải (sử dụng `@keyframes`).
* **📜 Danh sách cuộn (Scrollable Lists):** Các mục "Recent" và "Next in Queue" có chiều cao cố định và tự động xuất hiện thanh cuộn khi danh sách quá dài.

---

## 🛠️ Công nghệ sử dụng

* **HTML5:** Cấu trúc ngữ nghĩa cho trang web.
* **CSS3:** Tạo kiểu giao diện, bao gồm:
    * **Flexbox** và **Grid** để dựng bố cục.
    * **CSS Variables (Biến CSS)** để quản lý theme Light/Dark.
    * **Media Queries** cho Responsive Design.
    * **Transitions** và **Animations** cho hiệu ứng động.
* **JavaScript (ES6+):** Một đoạn script ngắn gọn để xử lý logic bật/tắt `class` cho Light/Dark mode.

---

<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Circle Music</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1 class="page-title">Music Player</h1>
    <div class="app-container">
        <aside class="sidebar">
            <div class="logo">
                <i class="fas fa-compact-disc"></i> 
                <h1>Circle</h1>
            </div>
            <nav class="menu">
                <a href="#" class="active"><i class="fas fa-home"></i> Home</a>
                <a href="#"><i class="fas fa-search"></i> Search</a>
                <a href="#"><i class="fas fa-list-ul"></i> Playlists</a>
                <a href="#"><i class="fas fa-bell"></i> Notifications</a>
                <a href="#"><i class="fas fa-gem"></i> Premium Content</a>
            </nav>
            <div class="sidebar-footer">                
                <div class="theme-switcher">
                    <i class="fas fa-sun"></i>
                    <label class="switch">
                        <input type="checkbox" id="theme-toggle">
                        <span class="slider round"></span>
                    </label>
                    <i class="fas fa-moon"></i>
                </div>
                <a href="#" class="download-link">Download Desktop App</a>
                <div class="user-profile">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT9EL1tfwm9uFVCV-cSoZeENZLMVMEqA45GWw&s" alt="User Avatar">
                    <span>Quỳnh Mũy</span>
                    <i class="fas fa-chevron-up"></i>
                </div>
            </div>
        </aside>
        <main class="main-content">
            <header class="main-header">
                <div class="tabs">
                    <a href="#" class="active">Music</a>
                    <a href="#">Podcasts</a>
                    <a href="#">Jazz</a>
                    <a href="#">Electronic</a>
                    <a href="#">Rock Classic</a>
                    <a href="#">Hip Hop</a>
                </div>
            </header>
            <section class="content-section">
                <h2>Popular Albums</h2>
                <div class="card-grid-3-cols">
                    <div class="card"><!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Circle Music</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1 class="page-title">Music Player</h1>
    <div class="app-container">
        <aside class="sidebar">
            <div class="logo">
                <i class="fas fa-compact-disc"></i> 
                <h1>Circle</h1>
            </div>
            <nav class="menu">
                <a href="#" class="active"><i class="fas fa-home"></i> Home</a>
                <a href="#"><i class="fas fa-search"></i> Search</a>
                <a href="#"><i class="fas fa-list-ul"></i> Playlists</a>
                <a href="#"><i class="fas fa-bell"></i> Notifications</a>
                <a href="#"><i class="fas fa-gem"></i> Premium Content</a>
            </nav>
            <div class="sidebar-footer">
                <div class="theme-switcher">
                    <i class="fas fa-sun"></i>
                    <label class="switch">
                        <input type="checkbox" id="theme-toggle">
                        <span class="slider round"></span>
                    </label>
                    <i class="fas fa-moon"></i>
                </div>
                <a href="#" class="download-link">Download Desktop App</a>
                <div class="user-profile">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT9EL1tfwm9uFVCV-cSoZeENZLMVMEqA45GWw&s" alt="User Avatar">
                    <span>Quỳnh Mũy</span>
                    <i class="fas fa-chevron-up"></i>
                </div>
            </div>
        </aside>
        <div class="main-content-wrapper">
            <main class="main-content">
                <header class="main-header">
                    <div class="tabs">
                        <a href="#" class="active">Music</a>
                        <a href="#">Podcasts</a>
                        <a href="#">Jazz</a>
                        <a href="#">Electronic</a>
                        <a href="#">Rock Classic</a>
                        <a href="#">Hip Hop</a>
                    </div>
                </header>
                <section class="content-section">
                    <h2>Popular Albums</h2>
                    <div class="card-grid-3-cols">
                        <div class="card">
                            <img src="https://upload.wikimedia.org/wikipedia/vi/c/cd/Taylor_Swift_-_Lover.png" alt="Album Art">
                            <div class="card-content">
                                <div class="card-info">
                                    <h3>Lover</h3>
                                    <p>Taylor Swift</p>
                                    <div class="card-meta">
                                        <span>18 Tracks &bull; 2M+ Likes</span>
                                    </div>
                                </div>
                                <div class="card-actions">
                                    <button class="like-button"><i class="far fa-heart"></i></button>
                                    <button class="play-button"><i class="fas fa-play"></i></button>
                                </div>
                            </div>
                        </div>
                         <div class="card">
                            <img src="https://upload.wikimedia.org/wikipedia/vi/4/43/Nine_Track_Mind.jpg" alt="Album Art">
                            <div class="card-content">
                               <div class="card-info">
                                    <h3>Nine Track Mind</h3>
                                    <p>Charlie Puth</p>
                                    <div class="card-meta">
                                        <span>15 Tracks &bull; 1M+ Likes</span>
                                    </div>
                                </div>
                                <div class="card-actions">
                                    <button class="like-button"><i class="far fa-heart"></i></button>
                                    <button class="play-button"><i class="fas fa-play"></i></button>
                                </div>
                            </div>
                        </div>
                         <div class="card">
                            <img src="https://upload.wikimedia.org/wikipedia/vi/2/27/Justin_Bieber_-_Purpose_%28Official_Album_Cover%29.png" alt="Album Art">
                            <div class="card-content">
                               <div class="card-info">
                                    <h3>Purpose</h3>
                                    <p>Justin Bieber</p>
                                    <div class="card-meta">
                                        <span>14 Tracks &bull; 1M+ Likes</span>
                                    </div>
                                </div>
                                <div class="card-actions">
                                    <button class="like-button"><i class="far fa-heart"></i></button>
                                    <button class="play-button"><i class="fas fa-play"></i></button>
                                </div>
                            </div>
                        </div>
                    </div>
                </section>
                <section class="picked-for-you">
                    <img src="https://image-cdn.nct.vn/playlist/2025/02/21/4/c/a/8/1740127621414_500.jpg" alt="Playlist Art">
                    <div class="info">
                        <span class="playlist-tag">PLAYLIST</span>
                        <h3>Top 100 hits USUK </h3>
                        <p>The 100 most popular songs from the US and UK this week.</p>
                        <div class="meta">
                            <span>05:47:12</span> &bull;
                            <span>50M+ Likes</span> &bull;
                            <span>100 Tracks</span>
                        </div>
                        <div class="tags">
                            <span>Trending Now</span>
                            <span>Hot Hits</span>
                            <span>Pop Vibes</span>
                        </div>
                        <div class="actions">
                            <button class="like-button"><i class="far fa-heart"></i></button>
                            <button class="download-button"><i class="fas fa-arrow-down"></i></button>
                            <button class="play-button"><i class="fas fa-play"></i></button>
                        </div>
                    </div>
                </section>
                <section class="content-section">
                    <h2>Recent</h2>
                    <div class="recent-list">
                        <div class="recent-item">
                            <span class="index">1</span>
                            <img src="https://upload.wikimedia.org/wikipedia/vi/7/7c/Taylor_Swift_-_Blank_Space_%28Official_Single_Cover%29.png" alt="Song Art">
                            <div class="song-info">
                                <h3>Blank Space</h3>
                                <p>Taylor Swift</p>
                            </div>
                            <div class="album-info">
                                <span>1989</span>
                                <p>2014</p>
                            </div>
                            <span class="duration">03:51</span>
                            <div class="actions">
                                <button class="like-button"><i class="far fa-heart"></i></button>
                                <button class="play-button-sm"><i class="fas fa-play"></i></button>
                            </div>
                        </div>
                        <div class="recent-item">
                            <span class="index">2</span>
                            <img src="https://images.genius.com/c48eb30caab693c9a80f49610e2ddb24.1000x1000x1.png" alt="Song Art">
                            <div class="song-info">
                                <h3>Love Yourself</h3>
                                <p>Justin Bieber</p>
                            </div>
                            <div class="album-info">
                                <span>Purpose</span>
                                <p>2015</p>
                            </div>
                            <span class="duration">03:53</span>
                            <div class="actions">
                                <button class="like-button"><i class="far fa-heart"></i></button>
                                <button class="play-button-sm"><i class="fas fa-play"></i></button>
                            </div>
                        </div>
                        <div class="recent-item">
                            <span class="index">3</span>
                            <img src="https://m.media-amazon.com/images/M/MV5BNmFlOWJkOTUtMzk5Ni00YjcxLTkyZTAtZjg5NmIzMTRkNjZkXkEyXkFqcGc@._V1_FMjpg_UX1000_.jpg" alt="Song Art">
                            <div class="song-info">
                                <h3>We Don't Talk Anymore</h3>
                                <p>Charlie Puth feat. Selena Gomez</p>
                            </div>
                            <div class="album-info">
                                <span>Nine Track Mind</span>
                                <p>2016</p>
                            </div>
                            <span class="duration">03:37</span>
                            <div class="actions">
                                <button class="like-button"><i class="far fa-heart"></i></button>
                                <button class="play-button-sm"><i class="fas fa-play"></i></button>
                            </div>
                        </div>
                        <div class="recent-item">
                            <span class="index">4</span>
                            <img src="https://upload.wikimedia.org/wikipedia/en/b/b2/Ariana_Grande_Thank_U_Next.png" alt="Song Art">
                            <div class="song-info">
                                <h3>Thank U, Next</h3>
                                <p>Ariana Grande</p>
                            </div>
                            <div class="album-info">
                                <span>Thank U, Next</span>
                                <p>2019</p>
                            </div>
                            <span class="duration">03:27</span>
                            <div class="actions">
                                <button class="like-button"><i class="far fa-heart"></i></button>
                                <button class="play-button-sm"><i class="fas fa-play"></i></button>
                            </div>
                        </div>
                        <div class="recent-item">
                            <span class="index">5</span>
                            <img src="https://upload.wikimedia.org/wikipedia/vi/2/29/Maroon_5_Sugar_bia_dia_don.png" alt="Song Art">
                            <div class="song-info">
                                <h3>Sugar</h3>
                                <p>Maroon 5</p>
                            </div>
                            <div class="album-info">
                                <span>V</span>
                                <p>2014</p>
                            </div>
                            <span class="duration">03:55</span>
                            <div class="actions">
                                <button class="like-button"><i class="far fa-heart"></i></button>
                                <button class="play-button-sm"><i class="fas fa-play"></i></button>
                            </div>
                        </div>
                        <div class="recent-item">
                            <span class="index">6</span>
                            <img src="https://upload.wikimedia.org/wikipedia/en/a/a7/Mark_Ronson_-_Uptown_Funk_%28feat._Bruno_Mars%29_%28Official_Single_Cover%29.png" alt="Song Art">
                            <div class="song-info">
                                <h3>Uptown Funk</h3>
                                <p>Bruno Mars with Mark Ronson</p>
                            </div>
                            <div class="album-info">
                                <span>Uptown Special</span>
                                <p>2014</p>
                            </div>
                            <span class="duration">04:30</span>
                            <div class="actions">
                                <button class="like-button"><i class="far fa-heart"></i></button>
                                <button class="play-button-sm"><i class="fas fa-play"></i></button>
                            </div>
                        </div>
                    </div>
                </section>
            </main>
            <footer class="player">
                <div class="player-left">
                    <img src="https://hautruong.info/wp-content/uploads/2025/06/SHOOTING-CAPTAIN29003-Copy.jpg" alt="Current Song Art">
                    <div class="item-info">
                        <p class="song-title">Ai lớn cũng phải</p>
                        <p class="song-artist">CAPTAIN BOY</p>
                    </div>
                    <button class="like-button"><i class="far fa-heart"></i></button>
                </div>
                <div class="player-center">
                    <div class="player-buttons">
                        <button><i class="fas fa-shuffle"></i></button>
                        <button><i class="fas fa-step-backward"></i></button>
                        <button class="play-main-button"><i class="fas fa-pause"></i></button>
                        <button><i class="fas fa-step-forward"></i></button>
                        <button><i class="fas fa-repeat"></i></button>
                    </div>
                    <div class="progress-bar-area">
                        <span>01:50</span> <div class="progress-bar"><div class="progress"></div></div>
                        <span>-03:36</span>
                    </div>
                </div>
                <div class="player-right">
                    <i class="fas fa-volume-up"></i>
                    <div class="volume-bar"><div class="volume-level"></div></div>
                </div>
            </footer>
        </div> <aside class="rightbar">
            <div class="search-bar">
                <i class="fas fa-search"></i>
                <input type="text" placeholder="Search ">
            </div>
            <section class="content-section">
                <h2>Popular Artists</h2>
                <div class="artist-grid">
                    <div class="artist-item"><img src="https://upload.wikimedia.org/wikipedia/commons/b/b1/Taylor_Swift_at_the_2023_MTV_Video_Music_Awards_%283%29.png" alt="Artist"><p>Taylor Swift</p></div>
                    <div class="artist-item"><img src="https://media.gq.com/photos/56bcb218cdf2db6945d2ef93/master/pass/bieber-coverstory-square.jpg" alt="Artist"><p>Justin Bieber</p></div>
                    <div class="artist-item"><img src="https://media.newyorker.com/photos/5b16cfe87018915289e3cb28/master/w_2560%2Cc_limit/StFelix-Charlie-Puth.jpg" alt="Artist"><p>Charlie Puth</p></div>
                    <div class="artist-item"><img src="https://upload.wikimedia.org/wikipedia/commons/e/ef/KatyPerryWestminst111224_%2881_of_95%29_%2854206733094%29_%28cropped_2%29.jpg" alt="Artist"><p>Katy Perry</p></div>
                    <div class="artist-item"><img src="https://shapes.inc/api/public/avatar/arianagrande-t61z" alt="Artist"><p>Ariana Grande</p></div>
                    <div class="artist-item"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT1jsg8scCxQ3nuED4RRBO8atiAIgMsnS_YbA&s" alt="Artist"><p>Bruno Mars</p></div>
                </div>
            </section>
            <section class="content-section">
                <h2>Top Podcasts</h2>
                <div class="podcast-grid">
                    <div class="podcast-card"><img src="https://static01.nyt.com/images/2017/01/29/podcasts/the-daily-album-art/the-daily-album-art-videoSixteenByNineJumbo1600-v4.jpg" alt="Podcast"><p>The Daily</p></div>
                    <div class="podcast-card"><img src="https://cdn.prod.website-files.com/64751ad903a904b42aa4adc1/689cd6d990affe313e9c7b45_673e976da21197552d9fee14_673e97550412138dd4ad5a47_Episode%25202%2520-%2520Master%2520Your%2520Sleep.webp" alt="Podcast"><p>Huberman Lab</p></div>
                </div>
            </section>
            <section class="content-section">
                <h2>Next in Queue</h2>
                <div class="queue-list">
                    <div class="queue-item active">
                        <button class="play-pause-btn"><i class="fas fa-xmark"></i></button>
                        <button class="like-button"><i class="fas fa-heart"></i></button>
                        <img src="https://upload.wikimedia.org/wikipedia/en/c/c3/Maroon_5_-_Memories.png" alt="Song Art">
                        <div class="item-info"><h3>Memories</h3><p>Maroon 5</p></div>
                        <span class="duration">03:09</span>
                    </div>
                    <div class="queue-item">
                        <button class="play-pause-btn"><i class="fas fa-xmark"></i></button>
                        <button class="like-button"><i class="far fa-heart"></i></button>
                        <img src="https://upload.wikimedia.org/wikipedia/en/f/f4/That%27s_What_I_Like_Remixes.jpg" alt="Song Art">
                        <div class="item-info"><h3>That's What I Like</h3><p>Bruno Mars</p></div>
                        <span class="duration">03:26</span>
                    </div>
                    <div class="queue-item">
                        <button class="play-pause-btn"><i class="fas fa-xmark"></i></button>
                        <button class="like-button"><i class="far fa-heart"></i></button>
                        <img src="https://upload.wikimedia.org/wikipedia/en/6/60/Firework_cover.png" alt="Song Art">
                        <div class="item-info"><h3>Firework</h3><p>Katy Perry</p></div>
                        <span class="duration">03:48</span>
                    </div>
                    <div class="queue-item">
                        <button class="play-pause-btn"><i class="fas fa-xmark"></i></button>
                        <button class="like-button"><i class="far fa-heart"></i></button>
                        <img src="https://i1.sndcdn.com/artworks-000162897425-k8h6e5-t500x500.jpg" alt="Song Art">
                        <div class="item-info"><h3>See You Again</h3><p>Charlie Puth with Wiz Khalifa</p></div>
                        <span class="duration">03:49</span>
                    </div>
                    <div class="queue-item">
                        <button class="play-pause-btn"><i class="fas fa-xmark"></i></button>
                        <button class="like-button"><i class="far fa-heart"></i></button>
                        <img src="https://images.genius.com/ddab64aa5e55030c98e4979aef0bea20.1000x1000x1.png" alt="Song Art">
                        <div class="item-info"><h3>Sorry</h3><p>Justin Bieber</p></div>
                        <span class="duration">03:20</span>
                    </div>
                     <div class="queue-item">
                        <button class="play-pause-btn"><i class="fas fa-xmark"></i></button>
                        <button class="like-button"><i class="far fa-heart"></i></button>
                        <img src="https://upload.wikimedia.org/wikipedia/vi/b/b9/Taylor_Swift_-_Anti-Hero.png" alt="Song Art">
                        <div class="item-info"><h3>Anti-Hero</h3><p>Taylor Swift</p></div>
                        <span class="duration">03:20</span>
                    </div>
                </div>
            </section>
        </aside>
    </div>
    <script>
        const themeToggle = document.getElementById('theme-toggle');
        const body = document.body;
        themeToggle.addEventListener('change', function() {
            if (this.checked) {
                body.classList.add('dark-mode');
            } else {
                body.classList.remove('dark-mode');
            }
        });
    </script>

</body>
</html>
