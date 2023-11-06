<template>
    <div class="box">
        <div class="group">
            <div class="overlap-group">
                <div class="ellipse"></div>
                <!-- other ellipses -->
            </div>
        </div>
    </div>
    <div class="benefit-page">
        <div class="container">
            <Header class="Header"/>
            <div class="content">
            <div class="top">
                <p class="p1">
                    Transform Communication
                    <img src="../assets/whatshot.png" alt="logo" />
                </p>
                <p>Data-Driven Engagement, Streamlined Impact.</p>
            </div>
            <div class="bottom">
                <div class="left-image">
                    <img src="../assets/diversity_3.png" alt="i" class="img1"/>
                    <img src="../assets/3p.png" alt="i" class="img2"/>
                    <img src="../assets/speaker_notes.png" alt="i" class="img3"/>
                    <img src="../assets/campaign.png" alt="i" class="img4"/>
                    <img src="../assets/smallwhats.png" alt="i" class="img5"/>
                </div>
                <div class="text-content">
                    <p class="p2">
                        <strong>Dynamic Grouping:</strong> Create customized groups effortlessly, tailored to your unique
                        criteria. Filter by name, location, interests, and more to ensure your groups are finely tuned for
                        maximum engagement.
                    </p>
                    <p class="p2">
                        <strong>Personalized Messaging:</strong> Send individual messages to group members, adding that
                        personal touch that fosters stronger connections.
                    </p>
                    <p class="p2">
                        <strong>Communicate Till Last Cadre:</strong> Reach every member of your group without the hassle of
                        individual messaging. Keep everyone informed and connected effortlessly.
                    </p>
                    <p class="p2">
                        <strong>Broadcasting Capabilities:</strong> Deliver essential announcements efficiently to all
                        members
                        at once. Keep your community or organization effortlessly informed.
                    </p>
                    <p class="p2">
                        <strong>WhatsApp Integration:</strong> Seamlessly integrate WhatsApp into our platform, harnessing
                        the
                        extensive reach of WhatsApp while enjoying the advanced capabilities of Mannit e-Messenger.
                    </p>
                </div>
            </div>
        </div>
    </div>
    </div>
</template>

<style scoped>
.benefit-page {
    font-family: 'Unbounded', sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f2f2f2;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 95vh; /* Center vertically within the viewport */
    font-size: 24px;
    font-style: normal;
    font-weight: 200;
}

.container {
    border: 1px solid #ccc;
    border-radius: 40px;
    width: 95%;
    background: linear-gradient(127deg, #FFF 0.29%, rgba(255, 255, 255, 0.67) 31.2%, rgba(255, 255, 255, 0.33) 95.34%, rgba(255, 255, 255, 0.10) 116.12%, rgba(255, 255, 255, 0.00) 145.68%, rgba(255, 255, 255, 0.00) 174.9%);
    backdrop-filter: blur(69.60322570800781px);
    
}
.content{
    display: flex;
    flex-direction: column;
    overflow: hidden;
    width: 100%;
    height: 500px;
    border-radius: 20px;
    align-items: center; /* Center horizontally within the container */
}

.top {
    font-family: 'Unbounded', sans-serif;
    font-size: 24px;
    line-height: 1;
    text-align: center;
    margin-top: 50px;
}

.bottom {
    width: 100%;
    font-size: 15px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.left-image {
    
    display: flex;
    height: 250px; 
    flex-direction: column;
    align-items: center;
}

.left-image img {
    display: block;
}

.img1 {
    position: absolute;
    width: 28.625px;
    height: 20.818px;
    flex-shrink: 0;
    margin-top: 15px;
    margin-right: 20px; 

}

.img2 {
    position: absolute;
    width: 28.625px;
    height: 20.818px;
    flex-shrink: 0;
    margin-top: 70px;
    margin-right: 20px;
}
.img3 {
    position: absolute;
    width: 28.625px;
    height: 20.818px;
    flex-shrink: 0;
    margin-top: 115px;
    margin-right: 20px;
}
.img4 {
    position: absolute;
    width: 28.625px;
    height: 20.818px;
    flex-shrink: 0;
    margin-top: 160px;
    margin-right: 20px;
}
.img5 {
    position: absolute;
    width: 28.625px;
    height: 20.818px;
    flex-shrink: 0;
    margin-top: 210px;
    margin-right: 20px;
}

.img1,
.img2,
.img3,
.img4,
.img5 {
    width: 2g.625px;
    height: 20.818px;
    flex-shrink: 0;
    margin-bottom: 10px;
    margin-right:10px; /* Adjust this margin to create space between images horizontally */
}
.text-content {
    flex: 1;
    max-width: 925px;
    font-size: 15px;
}

p {
    text-align: left;
    margin-left: 50px; /* Adjust the margin to align with the images */
    min-height: 1em;
}

.p1 {
    text-align: center;
    color: #25a449;
}

.p2 {
    font-size: 14px;
    text-align: justify;
    font-family: 'Unbounded',sans-serif;
}

img {
    width: 25px;
    height: 25px;
}

@media screen and (max-width: 900px) and (min-width: 600px) {
    .top {
        font-size: 18px;
    }

    .container {
        width: 95%;
    }
}

@media screen and (min-width: 1100px) {
    .top {
        font-family: 'Unbounded', sans-serif;
        font-size: 32px;
    }
}
</style>

<script>
import Header from "../components/Header.vue"
</script>
