<template>
  <div class="home">
    <div class="enHome mont" v-if="language == 'en'">
      <Header lang="eng" @change="change" />
      <div class="topDiv">
        <h3>Peyman Profile Asia Co</h3>
        <h1>
          Manufacturer of aluminum products with the most advanced equipment
        </h1>
        <button class="effectBtn">
          <img src="/icons/blackCall.svg" class="blackCallIcon" />
          <span>Get In Touch</span>
        </button>
        <div class="scroll d-flex justify-content-end align-items-center">
          <span class="scrollTitle">Scroll Down</span>
          <div class="scrollIcon">
            <span class="scrollCircle"></span>
          </div>
        </div>
      </div>
      <div class="whoWeAre d-flex justify-content-between align-items-center">
        <div class="texts">
          <h1>Who We Are?</h1>
          <p>
            Peyman Profile Asia Company started its activity in 2016 with
            research in the field of aluminum industry, monitoring market needs
            and building three halls, and with the passage of time and upgrading
            the complex to seven halls and equipping them with the most advanced
            tools for the production of aluminum products ...
          </p>
          <button class="effectBtn">
            <span>Read More</span>
          </button>
        </div>
        <div class="col animation">
          <Lines myVw="685" myVh="605" />
        </div>
      </div>
      <div class="workSmarter">
        <h2>Work smarter. React faster. Think bigger.</h2>
        <p>
          The goals and future plans of this company are based on the following
          policies :
        </p>
        <div class="d-flex justify-content-between icons">
          <div class="iconsDiv">
            <img src="/icons/smarterIcon1.svg" alt="" />
            <div>Equipping and updating machines</div>
          </div>
          <div class="iconsDiv">
            <img src="/icons/smarterIcon2.svg" alt="" />
            <div>Promotion of technical knowledge</div>
          </div>
          <div class="iconsDiv">
            <img src="/icons/smarterIcon3.svg" alt="" />
            <div>Knowing the market of this industry</div>
          </div>
          <div class="iconsDiv">
            <img src="/icons/smarterIcon4.svg" alt="" />
            <div>New standards of aluminum industry</div>
          </div>
        </div>
      </div>
      <div
        class="homeProduct1 d-flex align-items-center justify-content-between"
      >
        <div class="texts">
          <h2>Exclusive products<span>.</span></h2>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna
          </p>
          <button class="effectBtn">
            <span> More Info </span>
          </button>
        </div>
        <img src="/images/homeProduct1.png" alt="" />
      </div>
      <div
        class="homeProduct2 d-flex align-items-center justify-content-between"
      >
        <div class="texts">
          <h2>General products<span>.</span></h2>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna
          </p>
          <button class="effectBtn">
            <span> More Info </span>
          </button>
        </div>
        <img src="/images/homeProduct2.png" alt="" />
      </div>
      <div
        class="homeProduct3 d-flex align-items-center justify-content-between"
      >
        <div class="texts">
          <h2>Industrial products<span>.</span></h2>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna
          </p>
          <button class="effectBtn">
            <span> More Info </span>
          </button>
        </div>
        <img src="/images/homeProduct3.png" alt="" />
      </div>
      <div
        class="homeProduct4 d-flex align-items-center justify-content-between"
      >
        <div class="texts">
          <h2>Ingots & billets<span>.</span></h2>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna
          </p>
          <button class="effectBtn">
            <span> More Info </span>
          </button>
        </div>
        <img src="/images/homeProduct4.png" alt="" />
      </div>
      <div class="units">
        <div class="unitsHead">
          <h2>Units Of Our Company.</h2>
          <button class="effectBtn"><span>Read More</span></button>
        </div>
        <div class="items d-flex justify-content-around flex-wrap">
          <div
            v-for="item in unitItems"
            :key="item.id"
            class="item"
            :class="{ marginItem: item.id % 2 == 0 }"
            :id="`item${item.id}`"
          >
            <div class="number">0{{ item.id }}.</div>
            <div class="title">{{ item.title }}</div>
            <div class="text">{{ item.text }}</div>
          </div>
        </div>
      </div>
      <div
        class="animationImage col-12 d-flex justify-content-center align-items-center px-0"
      >
        <img src="/images/animationImage.png" v-show="!video" id="trigger" />
        <img
          src="/images/videoImg.jpg"
          class="col-12 px-0 video"
          v-show="video"
        />
      </div>
      <div class="news">
        <div class="newsHead">
          <h2>News.</h2>
          <p>We share the news related to the aluminum industry with you</p>
          <div class="button effectBtn">
            <span> All News </span>
          </div>
        </div>
        <div class="newsList">
          <div
            class="d-flex justify-content-between new"
            v-for="item in newsItems"
            :key="item.id"
            :id="`new${item.id}`"
          >
            <img :src="item.image" alt="" data-aos="zoom-in" />
            <div class="d-flex flex-column justify-content-between">
              <div class="titleAndText">
                <h3 class="title">{{ item.title }}</h3>
                <p class="text">{{ item.text }}</p>
              </div>
              <div class="number">0{{ item.id }}.</div>
            </div>
          </div>
        </div>
      </div>
      <Footer lang="en" />
    </div>
    <div class="faHome irancell" v-else>
      <Header lang="fa" @change="change" />
      <div class="topDiv">
        <h3 class="mont">Peyman Profile Asia Co</h3>
        <h1>?????????? ?????????? ?????????????? ???????????????????? ???? ?????????????? ???????? ??????????????</h1>
        <button class="effectBtn">
          <img src="/icons/blackCall.svg" class="blackCallIcon" />
          <span>???????? ???? ????</span>
        </button>
        <div class="scroll d-flex justify-content-end align-items-center">
          <div class="scrollIcon">
            <span class="scrollCircle"></span>
          </div>
          <span class="scrollTitle">Scroll Down</span>
        </div>
      </div>
      <div class="whoWeAre d-flex justify-content-between align-items-center">
        <div class="texts">
          <h1 class="mont">Who We Are?</h1>
          <div class="mb-4 d-flex justify-content-between align-items-center">
            <h2>???????????? ?? ????</h2>
            <div class="blueLine"></div>
          </div>
          <p>
            ???????? ?????????? ???????????? ???????? ???? ?????? 1395 ???? ?????????? ???? ?????????? ???????? ??????????????????
            ?? ?????????? ???? ???????? ?????????? ?? ???????? ???? ???????? ?? ???? ???????? ???????? ?? ???????????? ????????????
            ???? ?????? ???????? ?? ?????????? ???????? ???? ?????????????? ???????? ?????????? ?????????? ???????? ???? ??????
            ??????. ?????????????? ???????????????????? ...
          </p>
          <button class="effectBtn">
            <span>?????????? ??????????????</span>
          </button>
        </div>
        <div class="col animation">
          <Lines myVw="685" myVh="605" />
        </div>
      </div>
      <div class="workSmarter">
        <h2 class="mont">Work smarter. React faster. Think</h2>
        <div class="d-flex justify-content-between mb-4">
          <div class="d-flex align-items-center">
            <h3>?????? ?????????? ????</h3>
            <div class="blueLine"></div>
          </div>
          <h2 class="mont">.bigger</h2>
        </div>
        <p>?????????? ?? ???????????? ?????? ?????? ?????? ???????? ???? ???????? ?????????? ?????? ?????? ?????? :</p>
        <div class="d-flex justify-content-between icons">
          <div class="iconsDiv">
            <img src="/icons/smarterIcon1.svg" alt="" />
            <div>?????????? ?? ???? ?????? ?????????? ?????????? ????????</div>
          </div>
          <div class="iconsDiv">
            <img src="/icons/smarterIcon2.svg" alt="" />
            <div>???????????? ?????????? ???????? ??????</div>
          </div>
          <div class="iconsDiv">
            <img src="/icons/smarterIcon3.svg" alt="" />
            <div>?????????? ?????????? ?????? ????????</div>
          </div>
          <div class="iconsDiv">
            <img src="/icons/smarterIcon4.svg" alt="" />
            <div>?????? ???????????????????????? ????????</div>
          </div>
        </div>
      </div>
      <div
        class="homeProduct1 d-flex align-items-center justify-content-between"
      >
        <div class="texts">
          <h2>?????????????? ??????????<span>.</span></h2>
          <p>
            ?????????????????? ???? ?????? ??????????????? ?? ?????? ?????????? ???????????? ???????????? ?????????? ???????????? ????
            ?????????? ????????.???? ???? ???????? ??????????????????? ?????????? ?????????????? ?? ?????? ???????????? ???????????
            ??????????????? ...
          </p>
          <button class="effectBtn">
            <span>?????????????? ??????????</span>
          </button>
        </div>
        <img src="/images/faHomeProduct1.png" alt="" />
      </div>
      <div
        class="homeProduct2 d-flex align-items-center justify-content-between"
      >
        <div class="texts">
          <h2>?????????????? ????????????????<span>.</span></h2>
          <p>
            ???????????? ?????? ???? ????????????????????? ?? ???????????????????????? ?????????? ?????????????????? ???? ????????
            ?????????????? ???????????????.?????? ???????? ???? ?????? ???????????? ???? ?????????? ???????????? ?? ??????????
            ??????...
          </p>
          <button class="effectBtn">
            <span>?????????????? ??????????</span>
          </button>
        </div>
        <img src="/images/faHomeProduct2.png" alt="" />
      </div>
      <div
        class="homeProduct3 d-flex align-items-center justify-content-between"
      >
        <div class="texts">
          <h2>?????????????? ??????????????<span>.</span></h2>
          <p>
            ???????????? ???????????? ?? ?????????? ?? ???????? ???????? ?? ???????????? ???????????? ???? ???????? ?????????? ??????
            ?? ?????????? .
          </p>
          <button class="effectBtn">
            <span> ?????????????? ?????????? </span>
          </button>
        </div>
        <img src="/images/faHomeProduct3.png" alt="" />
      </div>
      <div class="units">
        <div class="unitsHead">
          <div class="mb-4 d-flex justify-content-between align-items-center">
            <div>
              <div class="blueLine"></div>
              <h3>???????? ?????? ????????????</h3>
            </div>
            <h2 class="mont">.Units Of Our Company</h2>
          </div>
          <button class="effectBtn"><span>?????????? ??????????????</span></button>
        </div>
        <div class="items d-flex justify-content-around flex-wrap">
          <div
            v-for="item in faUnitItems"
            :key="item.id"
            class="item"
            :class="{ marginItem: item.id % 2 == 0 }"
            :id="`item${item.id}`"
          >
            <div v-if="item.id <= 9" class="number mont">0{{ item.id }}.</div>
            <div v-else class="number mont">{{ item.id }}.</div>
            <div class="title">{{ item.title }}</div>
            <div class="text">{{ item.text }}</div>
          </div>
        </div>
      </div>
      <div
        class="animationImage col-12 d-flex justify-content-center align-items-center px-0"
      >
        <img src="/images/animationImage.png" v-show="!video" id="trigger" />
        <img
          src="/images/videoImg.jpg"
          class="col-12 px-0 video"
          v-show="video"
        />
      </div>
      <div class="news">
        <div class="newsHead">
          <div class="d-flex justify-content-between">
            <div class="faNew">
              <div class="d-flex align-items-center mb-4">
                <h3>??????????</h3>
                <div class="blueLine"></div>
              </div>
              <p>
                ?????????? ?????????? ???? ???????? ?????????????????? ???? ???? ?????? ???? ???????????? ???? ????????????.
              </p>
            </div>
            <div class="enNew">
              <h2 class="mont">.News</h2>
              <p class="mont">Lorem ipsum dolor sit</p>
            </div>
          </div>
          <div class="button effectBtn">
            <span> All News </span>
          </div>
        </div>
        <div class="newsList">
          <div
            class="d-flex justify-content-between new"
            v-for="item in faNewsItems"
            :key="item.id"
            :id="`new${item.id}`"
          >
            <img :src="item.image" alt="" data-aos="zoom-in" />
            <div class="d-flex flex-column justify-content-between">
              <div class="titleAndText">
                <h3 class="title">{{ item.title }}</h3>
                <p class="text">{{ item.text }}</p>
              </div>
              <div class="number mont">0{{ item.id }}.</div>
            </div>
          </div>
        </div>
      </div>
      <Footer lang="fa" />
    </div>
    <MouseEffect />
  </div>
</template>

<script>
import gsap from "gsap";
import ScrollTrigger from "gsap/dist/ScrollTrigger";
export default {
  data() {
    return {
      language: "",
      unitItems: [
        {
          id: 1,
          title: "Business unit",
          text: "The mission of this unit is to supply raw materials and machines needed for production lines, including casting, extrusion, powder paint, plating and decorative units...",
        },
        {
          id: 2,
          title: "Sales unit",
          text: "The job description in this unit is to provide the best services in the field of sales, support, consulting, surveys and representation in all cities and centers of domestic ...",
        },
        {
          id: 3,
          title: "Extrusion unit",
          text: "Aluminum extrusion (shaping) is a specific process in which the pre-heated billet enters the mold by hydraulic pressure and exits the mold as extruded products in different shapes...",
        },
        {
          id: 4,
          title: "Powder paint unit",
          text: "Electrostatic paint is a technique of using dry paint to cover a piece, which has been the newest method for painting and covering surfaces in general and industrial applications....",
        },
        {
          id: 5,
          title: "Decorative unit",
          text: "The decorative unit is a system that makes it possible to implement granite wood designs or fantasy patterns on all surfaces....",
        },
        {
          id: 6,
          title: "Plating unit",
          text: "The formation of a thin oxide layer on aluminum parts, which increases the hardness of the corrosion resistance, and changes some of its physical properties,..",
        },
        {
          id: 7,
          title: "Warehouse unit",
          text: "After the packaging and labeling process, the produced products are sorted according to a regular...",
        },
        {
          id: 8,
          title: "Warehouse unit",
          text: "The casting unit of this complex uses a tilting melting furnace and an ingot casting furnace, both of which have a capacity of 12 tons per shape.....",
        },
        {
          id: 9,
          title: "Warehouse unit",
          text: "The casting unit of this complex uses a tilting melting furnace and an ingot casting furnace, both of which have a capacity of 12 tons per shape.....",
        },
      ],
      faUnitItems: [
        {
          id: 1,
          title: "???????? ????????????????",
          text: "?????????? ?????? ???????? ?????????? ???????? ?????????? ?? ?????????? ???????? ???????? ???????? ???????? ?????????? ???????? ???????? ?????????? ???????? ?????????????????? ?????? ???????????? ???????????? ?? ???????????? ????????????. ?????? ???????????? ???? ?????????????? ???? ?????????? ?????????? ?? ????????...",
        },
        {
          id: 2,
          title: "???????? ????????",
          text: "?????? ?????????? ???? ?????? ???????? ?????????? ???????????? ?????????? ???? ?????????? ?????????? ?????????????????? ?????????????? ?????????????? ?? ?????????? ???????????????? ???? ?????????? ?????? ?? ?????????? ???????????????? ?????????? ?? ?????????????? ???????????? ???? ??????????...",
        },
        {
          id: 3,
          title: "???????? ?????????? ??????",
          text: "?????? ???????? ?????????????? ?????????? ?????????? ???????? ?????? ???????????????????? ?????? 5 ???? 8 ???????? ???? ???????? ?????? ???????????? 1000 ???? 7000 ???????? ?? ???? ???? ???????????? ?????????? ???? ???????? ?????? DC (DIRECT CHILL EASTING) ???? ?????????? ??...",
        },
        {
          id: 4,
          title: "???????? ?????????? ?? ???????? ????????",
          text: "?????????? ???????? ?????? ???????? ?????????? ?? ?????????? ???????? ?????????? ?????????? ?????????? ?????????????? ?? ???????? ?? ?????????? ???????? ???? ???????????? ?????????? ?????????? ???????? ???? ???? ???????? ?????????????? ?????? ?????????? ??????...",
        },
        {
          id: 5,
          title: "???????? ????????????????",
          text: "???????? ???????????????? ?????? ???????????? ???? ???? ???????????? ?????????? ???? ???????????? ?????? ???????????????? 1600 ?? 1800 ??2000 ?????? ???????? ?????????? ???????????? ???????????????? ?????????? ?????????? ?????? ???????????????? ??????????????????...",
        },
        {
          id: 6,
          title: "???????? ??????????",
          text: "???????????? ???????????? ?? ???? ???? ???????????? ???????? ???????? ?????????? ???????????? ?????? ?????????????????? ?????? ???????? ?????????? ???? ???????? ?? ???????? ???????? ???????? ???????????? ?????? ?????????? ?????? ?????????? ?????????? ...",
        },
        {
          id: 7,
          title: "???????? ????????????",
          text: "?????????? ???? ???????? ???????? ???????????? ???? ?????? ?????????? ???????????????????? ???? ???? ???????? ???????????? ???????? ???????????? ???? ?????????? ?????????????? ?? ?????????? ???????? ???? ?????????????? ???????????? ???? ?????????? ???????????? (?????????????? ?????????? ???????? ??????????...",
        },
        {
          id: 8,
          title: "????????  ??????????????",
          text: "?????????????? ?????? ?????? ?????????????? ???????? ???????? ?????? ???? ?????????? ???????????? ?????? ???? ???????? ?????????????????? ???????????? ???? ???????? ???? ???? ???? ?????????????????? ?????? ???????? ?? ?????? ?????????? ?????????? ???????? ???? ????????",
        },
        {
          id: 9,
          title: "???????? ?????? ??????????????????????????",
          text: "???????? ?????? ???????? ?????????? ???????????? ???????? ???????? ???? ???? ???? ?????? ?????????????????????????? ???????? ???????????????? ???????? ???? ???? ???????? ???????? ???? ???????? ???????????? ?????????? (??????????????)?? ???????? ?????? ?????? ?? ???????? ?????? ???????? ???? ???????? ...",
        },
        {
          id: 10,
          title: "???????? ????????????",
          text: "???????? ???????????? ?????? ???????????? ???? ???? ???????????? ?????????? ?????????? ???????? ?? ?????????????? ???????? ???????? ?????? ?????????? ?????? ?????? ?? ???????????? ?? ???? ?????? ?????? ???????????? ???? ???? ?????? ???????? ???????? ???????????????????? ???? ???????????? ?????????? ...",
        },
        {
          id: 11,
          title: "???????? ??????????????????",
          text: "?????????????????? ?????????????? ???????????? ???? ???? ???????????? ?????????? ?????????????? ?????? ???????? ???? ?????????? ???????? ?????????????????? ?? ???????????? ???????? ???????? ???? ????????...",
        },
        {
          id: 12,
          title: "???????? ?????????? ??????????",
          text: "?????? ???? ?????????????? ???????????? ???? ???????? ?????????????? ???? ?????????? ?? ?????????????? ???????? ???????? ???????? ?????? ???????????? ?????????? ?? ?????????? ?????????? ???? ???????????? ???? ?????????? ?????? ?????? ???????????? ???????? ??????...",
        },
        {
          id: 13,
          title: "???????? ???????? ???????? ?? ????????",
          text: "?????????? ?????????????? ?????????? ?????? ???? ?????? ?????????? ???? ???? ?????????? ?????????? ???? ???????? ?????? ?????????? ?????????? ???? ?????? PPA ?? Arall ???????? ???????? ???? ??????. ???? ???????????????? ...",
        },
        {
          id: 14,
          title: "???????? ??????????",
          text: "?????????????? ?????????? ?????? ???? ???? ?????????? ???????? ???????? ?? ???????? ?????????? ?????????? ???? ?????????? ???????? ?? ???????? ???????? ?????? ?? ???? ???????? ?????????? ?? ?????????? ???? ?????????? ???? ?????????? ?????????????? ???? ??????????...",
        },
      ],
      newsItems: [
        {
          id: 1,
          image: "/images/homeNew1.jpg",
          title: "Lorem ipsum dolor sit",
          text: `Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt
                ut labore et dolore magna aliqua Egestas purus viverra accumsan in nisl nisi Arcu cursus
                vitae congue mauris rhoncus aenean vel elit scelerisque ...`,
        },
        {
          id: 2,
          image: "/images/homeNew2.jpg",
          title: "Lorem ipsum dolor sit",
          text: `Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt
                ut labore et dolore magna aliqua Egestas purus viverra accumsan in nisl nisi Arcu cursus
                vitae congue mauris rhoncus aenean vel elit scelerisque ...`,
        },
        {
          id: 3,
          image: "/images/homeNew3.jpg",
          title: "Lorem ipsum dolor sit",
          text: `Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt
                ut labore et dolore magna aliqua Egestas purus viverra accumsan in nisl nisi Arcu cursus
                vitae congue mauris rhoncus aenean vel elit scelerisque ...`,
        },
      ],
      faNewsItems: [
        {
          id: 1,
          image: "/images/homeNew1.jpg",
          title: "???????? ???????????? ??????",
          text: `???????? ???????????? ?????? ???????????? ???? ?????????? ?????????? ?????????????? ???? ???????? ?????? ?? ???? ?????????????? ???? ???????????? ???????????? ?????? ?????????????? ?? ???????? ???????? ?????????????? ?? ???????? ???? ???????? ?? ?????????????????? ???? ???????? ?????? ...`,
        },
        {
          id: 2,
          image: "/images/homeNew2.jpg",
          title: "???????? ???????????? ??????",
          text: `???????? ???????????? ?????? ???????????? ???? ?????????? ?????????? ?????????????? ???? ???????? ?????? ?? ???? ?????????????? ???? ???????????? ???????????? ?????? ?????????????? ?? ???????? ???????? ?????????????? ?? ???????? ???? ???????? ?? ?????????????????? ???? ???????? ?????? ...`,
        },
        {
          id: 3,
          image: "/images/homeNew3.jpg",
          title: "???????? ???????????? ??????",
          text: `???????? ???????????? ?????? ???????????? ???? ?????????? ?????????? ?????????????? ???? ???????? ?????? ?? ???? ?????????????? ???? ???????????? ???????????? ?????? ?????????????? ?? ???????? ???????? ?????????????? ?? ???????? ???? ???????? ?? ?????????????????? ???? ???????? ?????? ...`,
        },
      ],
      video: false,
    };
  },
  mounted() {
    this.language = this.$store.state.lang;
    setTimeout(() => {
      gsap.registerPlugin(ScrollTrigger);
      let tl = gsap.timeline();
      tl.to("#trigger", {
        scrollTrigger: {
          trigger: "#trigger",
          start: "50% center",
          end: "=+650 center",
          scrub: true,
          // markers: true,
        },
        scale: 3,
        top: 50,
        transform: "translateY(400px)",
      });
    }, 10);
    window.addEventListener("scroll", () => {
      if (
        document.getElementById("trigger").style.top == "50px" &&
        !this.video
      ) {
        this.video = true;
      } else if (
        document.getElementById("trigger").style.top != "50px" &&
        this.video
      ) {
        this.video = false;
      }
    });
  },

  methods: {
    change() {
      this.$store.commit("change");
    },
  },
  watch: {
    "$store.state.lang"() {
      this.language = this.$store.state.lang;
    },
  },
};
</script>

<style>
</style>