<template>
    <div  class="mt-10 mr-4 ml-4 py-3 px-3 ">
        <p  class=' font-medium text-xl'>
                Industries we know
        </p>
        <p class='font-medium text-xl'>
            and understand
        </p>
        <div class=" text-7xl mt-10 font-bold">
            <p>un <span class="block">paralleled</span></p>
        </div>
        <div class="flex justify-between  ">
            <img src="../new_incons/svgexport-20.png" alt="" class="rounded-full  mt-96  rotate-90 w-52   bottom-0 p-5 " style="background:#ffff05;"/>
            <img src="../icons/pocketad.io_home_image2_mobile.png" alt="no img" class="  w-72 bg ">
        </div>
        <div class="mt-10 flex  ">
            <img src="../new_incons/svgexport-21.png" alt="" class="h-11 mt-5"  >
            <p class=" text-3xl pl-5 font-semibold">we know what <span class="block">we're doing</span> 
            </p>
        </div>  
        <div class="mr-2 ml-2 mt-10 ">
            <p class=" text-slate-500 ">We have spent +30 years creating and re-creating digital solutions, and learned what makes great businesses stay in business.</p>
        </div> 
        <div class="mt-28  flex justify-between">
            <p class=" font-bold text-3xl">Naranja X </p>
            <p class=" font-bold text-3xl">YPF </p>
        </div> 
        <div class=" ml-2 mt-28 ">
            <p class=" text-lg">Within these 7 industries</p>
            <div class="border-slate-300 border-x-4 border-b-2 mt-5 mb-8 sm:h-full ">
                <div class="slider">
                    <div class='slider-content' :style="sliderStyle">
                        <div class="slider-item"
                            v-for="(item, index) in items" :key="index"
                            :class="{ active: currentIndex === index }"
                        >
                            <p class="mt-10 text-3xl font-semibold px-2  ">{{item.title}}</p>
                            <p class="mt-5 px-2    ">{{item.description}}</p>
                            <div  class="w-[300px]  inline-flex  mt-5  mb-5 px-2 py-2  ">                
                              <p class="rounded-full py-2 px-5 text-center  text-gray-900 text-xs font-medium  " style="background:#ffff05;">Find out more</p>     
                              <img src="../new_incons/svgexport-20.png" alt="" class="rounded-full  p-3 w-10" style="background:#ffff05;">    
                          </div>
                        </div>
                    </div>
                    
                
                <div class="flex   place-content-center  mb-10">   
                        <button class='rounded-full  bg-black  h-10  w-10  ml-5 left-button    ' @click="slideLeft">
                            <img src="../new_incons/svgexport-31.png" alt="" class=" mt-4 ml-3 w-4 mb-4  rotate-180" />
                        </button>
                    <p class=" text-slate-500 text-lg ml-4 mt-3">{{currentIndex+1}}/7</p>
                        <button class='rounded-full bg-black  h-10  w-10  ml-5 right-button  ' @click="slideRight">
                            <img src="../new_incons/svgexport-31.png" alt="" class=" mt-4 ml-3 w-4 mb-4  " />
                        </button>
                </div>
            </div>
                    
            </div>
              
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
          title: "HealthCare",
          description: "We strive to revolutionize the healthcare sector by leveraging cutting-edge technologies, empowering medical professionals, and enhancing patient experiences in unprecedented ways. Our mission is to redefine the boundaries of healthcare innovation, crafting transformative digital solutions that revolutionize the concept of wellness, improve medical outcomes, and optimize the utilization of leisure time for a healthier society.",
        },
        {
          title: "Automotive",
          description: "Consumers crave automotive innovation like never before, seeking seamless driving experiences, advanced connectivity, and enhanced safety features. They desire vehicles that effortlessly adapt to their individual preferences, all while maintaining impeccable quality. At our core, we empower automotive companies to transform themselves, ensuring they remain at the forefront of this rapidly evolving industry.",
        },
        {
          title: "Telecommunication",
          description: "As the digital revolution sweeps through our interconnected world, the telecommunications industry plays a pivotal role in shaping our everyday conversations. With an insatiable demand for seamless connectivity and cutting-edge services, individuals and businesses alike expect nothing short of excellence from telecom brands, and we are dedicated to exceeding their expectations. From lightning-fast networks to innovative communication solutions, we ensure that our industry leads the way in delivering the very best experiences to empower and connect people around the globe.",
        },
        {
          title:"Retail & Ecommerce",
          description:"The art of crafting immersive customer journeys is a vital strength that we leverage in the retail and ecommerce industry, empowering organizations to redefine their offerings in a digitally-driven landscape. By seamlessly blending online and offline experiences, we enable retailers to revolutionize their portfolio and thrive in the ever-evolving realm of commerce."
        },
        {
          title:"Finance & Insurance",
          description:"In the finance and insurance industry, we empower organizations to transform their practices, revolutionizing how financial services are delivered and safeguarding assets through innovative strategies. Our expertise lies in redefining operational frameworks, optimizing risk management protocols, and streamlining transactional processes to ensure efficiency and enhance customer satisfaction amidst evolving market demands. We are committed to reshaping the landscape of financial and insurance sectors, enabling institutions to adapt, thrive, and meet the ever-changing needs of their clients with confidence and agility."
        },
        {
          title:"Logistics",
          description:"Logistics has become an essential pillar for seamless supply chain management and efficient operations in today's global marketplace. From transportation to warehousing, technology-driven solutions have become the backbone of this industry. We understand the intricacies of logistics and leverage our extensive experience to optimize processes, streamline operations, and deliver exceptional results in an ever-evolving landscape. Our expertise enables us to navigate complex logistical challenges, ensuring timely and cost-effective delivery of goods, and empowering businesses to stay ahead in the competitive logistics sector."
        },
        {
          title:"Utilities",
          description:"In an ever-evolving Utilities industry, where infrastructure demands continue to grow, environmental concerns become more pressing, and customer expectations reach new heights, we empower organizations with cutting-edge solutions, holistic approaches, and adaptive frameworks to transform complex data into actionable intelligence. As grid systems become smarter, renewable energy gains momentum, and regulatory landscapes evolve, our unwavering commitment to innovation ensures that we unlock the full potential of data-driven decision-making, delivering unparalleled value and efficiency to our clients."
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
