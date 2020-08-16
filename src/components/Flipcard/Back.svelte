<style>
  p {
    text-align: center;
    margin: 1em auto;
  }

  .flip-card-back {
    position: absolute;
    -webkit-backface-visibility: hidden; /* Safari */
    backface-visibility: hidden;
  }
  .flip-card-back {
    transform: rotateY(180deg);
  }

  .boulder {
    border-radius: 50%;
    width: 50%;
    display: inline-block;
    border: 3px solid #232121;
  }

  @media (min-width: 480px) {
    .boulder {
      border-radius: 50%;
      width: 25%;
      display: inline-block;
    }
  }
</style>

<div class="flip-card-back">
  <img class="boulder" src="boulder.jpg" alt="" />
  <div class="about-me">
    <p>
      Originally from a small town near Stuttgart, I went on to get my
      bachelor's degree in human-computer-interaction from
      Julius-Maximilians-University in Würzburg. During this time, I not only
      learned heaps about Usability Engineering, UX Design & Computer Science,
      but also got my first job as a Web Developer. Pretty soon I knew, that
      combining my expertise from these areas was what I wanted to pursue
      further after finishing uni.
    </p>
    <p>
      In my spare time you'll most likely find me in the bouldering gym on
      weekdays & somewhere in the mountains on the weekend. Some days I just
      want to spend with my PlayStation, though. Apart from that, I thoroughly
      enjoy cooking with my collection of cast iron pans & finding the right
      beer to go with my food.
    </p>
  </div>
</div>
