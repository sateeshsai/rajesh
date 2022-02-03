<script>
  import Masonry from "svelte-bricks";

  let items = [
    {
      id: 9,
      author: "Vineet",
      type: "Text",
      text: `Thank you Rajesh, for the wonderful contribution to innumerable audit pursuits and countless projects that you have supported through your tenure. 
      It is sad to see you go but also glad to see you growing in your career. Wishing you all the best for your future endeavors. Be well and do well.`,
    },
    {
      id: 8,
      author: "Mark",
      type: "Text",
      text: `Rajesh, 
      Thank you for all you have done in your time with Deloitte. You raised the bar on many projects and have a terrific creative talent. I remember working with you and Sateesh on the illustrations for the video (last year I think) and they were fantastic.
      I wish you all the best in the future, we will miss you.`,
    },

    {
      id: 18,
      author: "Rajat ",
      type: "Video",
      src: "/images/rajat.mp4",
    },

    {
      id: 10,
      author: "Tripti G",
      type: "Text",
      text: `Wishing you all the best Rajesh 😊, it was great collaborating and sharing experiences with you. I learnt so much from you as a colleague, buddy and coach 😊
      Will definitely miss our lunch and dinner sessions, and the super spicy and yummy dishes you got!! Hoping you get all the success in life and so much more. Take care, stay safe and keep in touch 😊`,
    },

    {
      id: 4,
      author: "Manju",
      type: "Text",
      text: `Rajesh wish you all the very best in this next phase of your career journey, am sure you will continue to shine in everything you do. All the very best!!`,
    },

    {
      id: 20,
      author: "Sateesh",
      type: "Text",
      text: `Thank you for everything you did for our team, Rajesh. I have worked closely with you on many projects and you consistently managed to deliver amazing work. I always appreciated the way you enthusiastically help fellow team members.
      You have incredible talent and a great attitude which will take you places. It's been a pleasure working with you and hope we will get to work together again. Wish you the very best and we'll miss you. - Sateesh`,
    },

    {
      id: 19,
      author: "Simon ",
      type: "Video",
      src: "/images/simon.mp4",
    },

    {
      id: 1,
      author: "Eesha ",
      type: "Text",
      text: `Dearest Rajesh,
      It has been so nice to know a kind , helpful and talented person like you. From the most stupidest doubts to  questions on the most complicated tools on any adobe software, you have been there through all of it. It's a bit hard to imagine the team without you since you were such an integral part of it . You were the life of the zoom calls, team hhuddle yoga sessions(haha!), impromptu sessions on innovative graphics. You ran the show!!!
      
      You have so genuinely helped out people and me in times of need. Being patient through out. You are a good friend before being a good colleague. I still remember my day one at Deloitte and we both walked in as newbies and I was glad to have a kind company back then and still am.
      
      I wish the best for you and I hope you have fun in your new workplace and definitely miss all of us! :P 
      
      - Your Lata Mangeshkar desk partner
      Eesha`,
    },
    {
      id: 11,
      author: "Tripti R",
      type: "Text",
      text: `Thank you Rajesh for being your honest self always.
      It has been wonderful working with you. Have seen you and your artwork evolve in the past 2 years. Will miss your enthusiasm to learn and try new things. Really happy for you and wish you the very best in everything that you do ahead!`,
    },

    {
      id: 3,
      author: "Kainaz",
      type: "Text",
      text: `Rajesh you would be truly missed in the team! I've enjoyed collaborating with you on key pursuits witnessing your creative and unique design style and the ability to bring in that extra spark. You have the ability to visualize things differently (like 4K Ultra HD) and do it very professionally.
      All the very best for your future endeavors, surely you'll shine wherever you go! 😊`,
    },

    {
      id: 16,
      author: "Shweta",
      type: "Text",
      text: `Rajesh is always up for the help in our team. I could always count on him for any kind of support I need. Wishing you success on your new adventure. I am sorry to see you go 🙁 I’m sure we’ll cross paths again someday. Stay in touch, and remember us when you are famous 😀`,
    },

    {
      id: 6,
      author: "Azeem",
      type: "Text",
      text: `Hi Rajesh, wish you the best for the future. Haven't worked together as much as I'd have liked but you've been great to work with. Congrats on the new adventure`,
    },

    {
      id: 17,
      author: "Pujitha ",
      type: "Text",
      text: `It was great knowing and working with you Rajesh! We will miss you here and all the very best for your exciting future ahead!`,
    },

    {
      id: 5,
      author: "Skandh ",
      type: "Text",
      text: `I had the chance of understanding the design aspects of a pursuit in Deloitte by working with Rajesh on my first few pursuits. Always ready to help, extremely creative, and ready to put in the hard yards, when needed — these, I believe, were the key strengths of Rajesh. Being a new PM, working with him was very easy for me. Plus, I will always cherish my first win in Deloitte, with him. 
      Although we haven't met face to face, we have had a very good understanding of each other. Wishing Rajesh the very best in his professional and personal journey, always! And yes, (now that I am in Hyderabad) look forward to meeting you soon!`,
    },

    {
      id: 13,
      author: "Minal",
      type: "Text",
      text: `RAJESH! I'm so sad you're leaving because we haven't nearly had enough epic conversations yet! But whatever we did have, I will always be so grateful for. You've helped me so much in the 4 months I've been here, and I think I speak on behalf of the new hires in our team when I say, we would be lost with you.
      From my Day 1 at Deloitte, you've just been there, and you are so approachable! I love that. Thank you for always staying late with me when I needed it. Anywhere you go, the people around you are always going to be lucky to have you - as a designer AND as a friend.
      And the one last thing I want to say to you, is in the portrait.`,
    },

    {
      id: 2,
      author: "Nitesh ",
      type: "Text",
      text: `The one who knows his game but stays so humble that everyone should learn from him. It's all about the character of a person, that makes a positive impact in people's lives. 
      I believe that kindness is the most powerful thing in this world, and I have seen that inside you, and nothing can change that. 
      Lots of learning from you, in such a short span of time. 
      Love and light 
      Rana`,
    },

    {
      id: 14,
      author: "Kashyap",
      type: "Text",
      text: `I would like to say a few words about Rajesh as an artist i really love his art style and the way he helps us understand how he did them. Is something that i really liked about him. I can proudly say he is an inspiration to me.`,
    },
    {
      id: 15,
      author: "Mohit",
      type: "Text",
      text: `Rajesh,
      Wish I could have worked with you for longer. You are a badass artist, you have a great sense of humor, and most importantly you are a helping and beautiful person travelling between Karimnagar and Hyderabad. I wish you all the best and lots of color in your future endeavors. Stay crafty Stay creative 😊`,
    },

    {
      id: 12,
      author: "Venkatesh",
      type: "Text",
      text: `This isn't Goodbye, it simply means you will be missed until we meet next time.
      Let me begin with Thanking you for the kind support and guidance. We got to work together for a very short time, but it was best.
      Once again Thank you very much. Wishing you best on your new beginning.`,
    },
  ];

  // $: items = testimonials.sort((a, b) => {
  //   if (a.author > b.author) {
  //     return 1;
  //   } else {
  //     return -1;
  //   }
  // });

  // $: console.log(items);

  let [minColWidth, maxColWidth, gap] = [300, 900, 50];
  let width, height;
</script>

<Masonry {items} {minColWidth} {maxColWidth} {gap} let:item bind:width bind:height>
  {#if item.type === "Video"}
    <h3>{item.author}</h3>
    <video controls src={item.src} />
  {:else}
    <div class="wrapper">
      <h3>{item.author}</h3>
      <p>
        {item.text}
      </p>
    </div>
  {/if}
</Masonry>

<style>
  h3 {
    /* font-family: "IBM Plex Mono", monospace; */
    font-weight: 800;
    font-size: 1.5rem;
    position: relative;
    z-index: 99;
    /* color: var(--backgroundColorHome); */
  }

  h3::before {
    content: "";
    width: 100%;
    height: 0.2rem;
    /* background-color: #3c3847; */
    background-color: var(--accentColor);
    position: absolute;
    left: -0.15rem;
    z-index: -1;
    top: -3rem;
  }

  p {
    font-size: 1.2rem;
    font-weight: 200;
    line-height: 1.65rem;
  }

  video {
    max-width: 100%;
  }
</style>
