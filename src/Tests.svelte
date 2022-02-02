<script>
  import Masonry from "svelte-bricks";

  $: items = [
    {
      id: 1,
      author: "Eesha ",
      text: `Dearest Rajesh,
      It has been so nice to know a kind , helpful and talented person like you. From the most stupidest doubts to  questions on the most complicated tools on any adobe software, you have been there through all of it. It's a bit hard to imagine the team without you since you were such an integral part of it . You were the life of the zoom calls, team hhuddle yoga sessions(haha!), impromptu sessions on innovative graphics. You ran the show!!!
      
      You have so genuinely helped out people and me in times of need. Being patient through out. You are a good friend before being a good colleague. I still remember my day one at Deloitte and we both walked in as newbies and I was glad to have a kind company back then and still am.
      
      I wish the best for you and I hope you have fun in your new workplace and definitely miss all of us! :P 
      
      Your Lata Mangeshkar desk partner
      Eesha`,
    },
    {
      id: 2,
      author: "Tripti ",
      text: `Donec quis ligula convallis, pretium quam eget, molestie metus. Nunc eget lectus eu diam sodales interdum. Ut efficitur congue urna nec porta. Vivamus vitae felis rutrum, efficitur purus eget, aliquam leo. Sed luctus malesuada libero. Nulla nisi ex, mollis ut velit at, sollicitudin pretium diam. Nullam urna augue, fringilla a imperdiet eget, congue vel lectus. Sed at lobortis orci, a pharetra libero. Nam quis nisl et massa tempor sodales eget vitae sem. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Suspendisse laoreet nunc sit amet quam auctor, sit amet blandit nisi sodales. Mauris facilisis sapien in est sagittis, eu consectetur ante blandit.`,
    },
    {
      id: 3,
      author: "Rakesh",
      text: `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla nec justo quis tortor vestibulum sagittis. Fusce in facilisis elit. Vestibulum auctor justo eu enim volutpat, ut tincidunt velit molestie. Quisque a blandit justo. In vulputate vulputate congue. Aliquam ut scelerisque lorem. Nullam ornare commodo enim eu luctus. Curabitur vestibulum laoreet nisl, eget mattis tellus. Donec fermentum tortor ante. Quisque consectetur, dui vel tempus ornare, massa enim rutrum urna, a scelerisque justo risus vel sapien. Maecenas elit orci, bibendum sit amet dignissim eget, sollicitudin a orci. Sed neque tortor, faucibus a fermentum ullamcorper, consequat a leo.`,
    },
    {
      id: 4,
      author: "Akhila",
      text: `Nunc mattis quam eget augue molestie consequat. Nunc sollicitudin, neque a pulvinar faucibus, sem augue elementum erat, eu tempor libero ligula nec sem. Duis in consequat ipsum. Nam malesuada nibh vitae mauris vehicula, vel feugiat lectus tristique. Praesent nunc lorem, malesuada quis interdum nec, maximus sed augue. Donec posuere justo sed feugiat dictum. Fusce tempor turpis turpis, nec malesuada lacus mollis at. Mauris laoreet consectetur leo, vitae rutrum ante consequat non.`,
    },
    {
      id: 5,
      author: "Nitesh",
      text: `Donec quis ligula convallis, pretium quam eget, molestie metus. Nunc eget lectus eu diam sodales interdum. Ut efficitur congue urna nec porta. Vivamus vitae felis rutrum, efficitur purus eget, aliquam leo. Sed luctus malesuada libero. Nulla nisi ex, mollis ut velit at, sollicitudin pretium diam. Nullam urna augue, fringilla a imperdiet eget, congue vel lectus. Sed at lobortis orci, a pharetra libero. Nam quis nisl et massa tempor sodales eget vitae sem. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Suspendisse laoreet nunc sit amet quam auctor, sit amet blandit nisi sodales. Mauris facilisis sapien in est sagittis, eu consectetur ante blandit.`,
    },

    {
      id: 6,
      author: "Mohit",
      text: `Donec quis ligula convallis, pretium quam eget, molestie metus. Nunc eget lectus eu diam sodales interdum. Ut efficitur congue urna nec porta. Vivamus vitae felis rutrum, efficitur purus eget, aliquam leo. Sed luctus malesuada libero. Nulla nisi ex, mollis ut velit at, sollicitudin pretium diam. Nullam urna augue, fringilla a imperdiet eget, congue vel lectus. Sed at lobortis orci, a pharetra libero. Nam quis nisl et massa tempor sodales eget vitae sem. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Suspendisse laoreet nunc sit amet quam auctor, sit amet blandit nisi sodales. Mauris facilisis sapien in est sagittis, eu consectetur ante blandit.`,
    },
    {
      id: 8,
      author: "Vineet",
      text: `Nunc mattis quam eget augue molestie consequat. Nunc sollicitudin, neque a pulvinar faucibus, sem augue elementum erat, eu tempor libero ligula nec sem. Duis in consequat ipsum. Nam malesuada nibh vitae mauris vehicula, vel feugiat lectus tristique. Praesent nunc lorem, malesuada quis interdum nec, maximus sed augue. Donec posuere justo sed feugiat dictum. Fusce tempor turpis turpis, nec malesuada lacus mollis at. Mauris laoreet consectetur leo, vitae rutrum ante consequat non.`,
    },
    {
      id: 9,
      author: "Mark",
      text: `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla nec justo quis tortor vestibulum sagittis. Fusce in facilisis elit. Vestibulum auctor justo eu enim volutpat, ut tincidunt velit molestie. Quisque a blandit justo. In vulputate vulputate congue. Aliquam ut scelerisque lorem. Nullam ornare commodo enim eu luctus. Curabitur vestibulum laoreet nisl, eget mattis tellus. Donec fermentum tortor ante. Quisque consectetur, dui vel tempus ornare, massa enim rutrum urna, a scelerisque justo risus vel sapien. Maecenas elit orci, bibendum sit amet dignissim eget, sollicitudin a orci. Sed neque tortor, faucibus a fermentum ullamcorper, consequat a leo.`,
    },
    {
      id: 10,
      author: "Minal",
      text: `Donec quis ligula convallis, pretium quam eget, molestie metus. Nunc eget lectus eu diam sodales interdum. Ut efficitur congue urna nec porta. Vivamus vitae felis rutrum, efficitur purus eget, aliquam leo. Sed luctus malesuada libero. Nulla nisi ex, mollis ut velit at, sollicitudin pretium diam. Nullam urna augue, fringilla a imperdiet eget, congue vel lectus. Sed at lobortis orci, a pharetra libero. Nam quis nisl et massa tempor sodales eget vitae sem. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Suspendisse laoreet nunc sit amet quam auctor, sit amet blandit nisi sodales. Mauris facilisis sapien in est sagittis, eu consectetur ante blandit.`,
    },
  ];

  let [minColWidth, maxColWidth, gap] = [300, 900, 50];
  let width, height;
</script>

<Masonry {items} {minColWidth} {maxColWidth} {gap} let:item bind:width bind:height>
  <div class="wrapper">
    <h3>{item.author}</h3>
    <p>
      {item.text}
    </p>
  </div>
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
</style>
