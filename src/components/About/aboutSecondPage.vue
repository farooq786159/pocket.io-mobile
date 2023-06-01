<template>
    <div style="background-color: #2a2a2a;">
        <div class="h-full  text-white pt-10  ml-2 mr-2">
            <div class='' >
                <img src="../new_incons/svgexport-24.png" class=" h-full  pb-5  ">
                <p class=" border-t-2 text-4xl font-bold pt-2   "><span class=" text-[20px] ml-2 mr-5 font-normal">01</span>  Curiosity</p>
                <p class="mt-10 pl-2 pr-2"> Always on the lookout for what's out there, what lies beyond, the reasons and workings behind things, curiosity is a core fiber in everyone at PocketAd. We make it a point to nurture curiosity in our day to day, as it creates the conditions for innovation and helps us handle uncertainty and keep our inventiveness sharp.</p>
            </div>
            <div >
                <img src="../new_incons/svgexport-25.png" class=" h-full mt-16   pb-5 ">
                <p class=" border-t-2 text-4xl font-bold pt-2  "><span class=" text-[20px] ml-2 mr-5 font-normal">02</span>  Adaptability</p>
                <p class="mt-10 pl-2 pr-2"> Light on our feet, we strive to be as nimble as possible, ready to pivot as we incorporate new information. That reflects on the       freshness of the work we deliver, on how we organize our teams, and how we approach   everything from hiring to exploring new spaces.</p>
            </div>
            <div >
                <img src="../new_incons/svgexport-26.png" class=" h-full mt-16 pb-5 ">
                <p class=" border-t-2 text-4xl font-bold pt-2  "><span class=" text-[20px] ml-2 mr-5 font-normal">03</span> Collaboration  </p>
                <p class="mt-10 pl-2 pr-2">Building great teams is at the heart of the way PocketAd operates, and we have a long tradition of organizing our work around cooperation, partnerships and interdisciplinary exchange. Over years of exploring various industries, we have learned to incorporate diverse perspectives early on in everything we do. </p>
            </div>
            <div  class='mb-44'>
                <img src="../new_incons/svgexport-27.png" class=" h-full mt-16 pb-5 ">
                <p class=" border-t-2 text-4xl font-bold pt-2  "><span class=" text-[20px] ml-2 mr-5 font-normal">04</span>  Sustainability</p>
                <p class="mt-10 pl-2 pr-2">Before anything else, PocketAd is an ecosystem. We have always had clarity about the fact that we are a part of something bigger, and that we nurture from it every bit as much as it is our responsibility to take good care of our surroundings. The only way to be consistent in our effort to co-create the future, is to also create the conditions for that future to be a better version of today.</p>
            </div>

            
            

        </div>
        
    </div>

    <div class='' >
        <div class="mt-10 " >
                <p class=" text-[78px] font-bold leading-[5rem]">leadership <span  class="block pl-44 ">team </span> </p>
                <p class="mt-10 px-2 mb-20">We organize our work around practices, and each practice is led by skilled mentors that bring all of their experience and proficiency to their team.These are the referents that lead the way in our everyday craft.</p>
            </div>
            <div class='grid grid-cols-11 '>
              <div class=' col-span-1  bg-slate-300' @click="slideLeft">
                <img src="../new_incons/svgexport-43.svg" alt="" class='ml-1  rotate-180  h-5 mt-72'>
              </div>
              <div class="slider col-span-9">
                <div class='slider-content' :style="sliderStyle">
                   <div class="slider-item"
                            v-for="(item, index) in items" :key="index"
                            :class="{ active: currentIndex === index }">
                    <p class="text-4xl font-bold text-center  ">{{item.title}}</p>
                    <P class=" mt-5 px-1 ">{{item.description}}</P>
                    
                   </div>

                </div>
                <div class="flex justify-center  pb-10 ">
                    <button class='rounded-full bg-white  p-5 rotate-180 left-button' @click="slideLeft">
                        <img src="../new_incons/svgexport-20.svg" alt="" class="h-5" >   
                    </button>
                    <p class=" text-slate-500 ml-9 mt-5 mr-9  text-4xl">{{currentIndex+1}}/4</p>
                    <button class='rounded-full bg-white  p-5 rotate-35  right-button ' @click="slideRight">
                        <img src="../new_incons/svgexport-20.svg" alt="" class="h-5" >   
                    </button>
                </div>
            </div>
            <div class=' col-span-1  bg-slate-300 ' @click="slideRight">
              <img src="../new_incons/svgexport-43.svg" alt="" class='ml-2  h-5 mt-72'>
            </div>
            </div>
    </div>

    <div class="mr-2 ml-2 pb-20" >
        <div class="pt-24 flex justify-between mb-5  ">
            <p class=" text-lg  font-medium ">Services</p>
            <img src="../new_incons/svgexport-11.png" class="h-14">     
        </div>
        <p class=" text-left text-4xl font-semibold mb-10">Lets create together <span class="block">with the quality our team creates</span></p>
        <div  class="w-[300px]  inline-flex  mt-10  mb-10   ">                
                <p class="rounded-full py-2 px-5 text-center text-xs font-medium bg-black text-white ">Dive into our services</p>     
                <img src="../new_incons/svgexport-23.png" alt="" class="rounded-full  p-3 w-10 bg-black" >    
        </div>
    </div>


</template>
<script >
export default {
  data() {
    return {
      currentIndex: 0,
      items: [
        {
          title: "Mohsin Kazmi",
          description: "Mohsin Kazmi is a consummate professional with an illustrious career spanning over two decades in the healthcare and financial consulting arenas. As the esteemed Co-founder and COO at Envoy Innovations, he spearheads cutting-edge initiatives to revolutionize specialty and home infusion pharmacies, elevating patient care and optimizing operational efficacy. With astute acumen in financial  planning, internal controls, and advisory services, Mohsin has garnered a formidable reputation for driving remarkable achievements at renowned organizations like Epic and Ernst & Young. As a visionary strategist, exemplary leader, and esteemed authority in healthcare and financial consulting, Mohsin Kazmi stands out as a trailblazer in his field.",
        },
        {
          title: "Patrick Darney",
          description: "Patrick Denney is a visionary entrepreneur and seasoned mobile solutions architect, with extensive experience in healthcare software. With over a decade of professional software development expertise and a deep understanding of Objective-C, C, HTML5, CSS3, and Javascript, Patrick excels in crafting cutting-edge solutions. As the CTO of Envoy Innovations and President of Lannister Consulting LLC, he has demonstrated exceptional leadership and strategic acumen in delivering innovative and patient-centric solutions for specialty and home infusion pharmacies. Patrick's proficiency in Agile methodologies, SDLC, and open-source technologies, coupled with his keen eye for UI/UX design, make him a formidable force in the industry. His unwavering commitment to quality, continuous improvement, and customer satisfaction make him a sought-after professional in the field of mobile solutions architecture.",
        },
        {
          title: "Ehsan Zaidi",
          description: "Ehsan Zaidi has also served as a Freelancer for BSH Group,  where he successfully orchestrated social media marketing and Google marketing initiatives for esteemed brands such as Siemens and Bosch in Sweden, Denmark, Norway, and Finland.  His astute strategic thinking, coupled with his expert proficiency in data analysis, database management, and A/B testing, has consistently yielded outstanding outcomes in these roles With an unwavering commitment to excellence and a penchant for innovative thinking, Ehsan Zaidi is a highly accomplished digital media professional, whose exceptional skill set and track record of success make him a valuable asset to Ehsan Zaidi is a consummate expert in the realm of digital media, with a wealth of experience that transcends the domain of digital marketing. Having commenced his career as a Marketing Analyst, Ehsan has garnered an impressive portfolio of work with distinguished organizations such as Metro Cash & Carry, Right Step Migration, Gobble, Comcast, Spectrum, Mediacom, AT&T, and Soft Touch Cosmetics.any organization seeking to achieve unparalleled digital marketing outcomes.",
        },
        {
          title:"Rubab Chaudhry",
          description:"Rubab Chaudhry is a seasoned digital marketing maven with over a decade of experience in spearheading a digital-first culture at international corporations, startups, and mid-size businesses. Rubab has been leveraging sharp business acumen and acute market sense with a demonstrated history of successes seemingly identifying and capitalizing on new opportunities. She's adept at creating and implementing client-centered, lucrative campaigns, aimed at improving the brand.Rubab's association with industry titans such as Bosch, Siemens, Comcast, AT&T, Spectrum, and Bidberry underscores her prowess in navigating highly competitive markets. Throughout her glittering professional career she has displayed exceptional proficiency in maintaining a comprehensive understanding of all digital marketing accounts' performance and served as a strategic liaison between clients and the marketing department to ensure unwavering alignment with client goals and targets.Rubab Chaudhry is a results-driven digital marketing professional, lauded for her strategic leadership, meticulous campaign optimization, and unwavering commitment to superior client success. Her exceptional ability to identify and seize opportunities, streamline operations, and deliver outstanding results in a dynamic and fast-paced environment make her an invaluable asset in the realm of digital marketing."
        },
        
      ],
    };
  },
  computed: {
    sliderStyle() {
      return `transform: translateX(-${this.currentIndex * 100}%)`;
    },
  },
  methods: {
    slideLeft() {
      this.currentIndex = (this.currentIndex - 1 + this.items.length) % this.items.length;
    },
    slideRight() {
      this.currentIndex = (this.currentIndex + 1) % this.items.length;
    },
  },
};
</script>

<style>
.slider {
  position: relative;
  width: 100%;
  overflow: hidden;
}

.slider-content {
  display: flex;
  transition: transform 0.3s ease;
}

.slider-item {
  flex: 0 0 100%;
}
.left-button:hover{
  background:#ffff05;
}
.right-button:hover{
  background:#ffff05;
  
}
.slider-button {
  position: absolute;
  transform: translateY(-50%);
  background-color: transparent;
  border: none;  
  cursor: pointer;
}


</style>
