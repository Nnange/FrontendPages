<script lang="ts">
	import { slide } from "svelte/transition";
 import "../../app.css"
 import { Facebook, Instagram, TwitterX, 
    Youtube, Tiktok, ChevronDown, ChevronUp} from "svelte-bootstrap-icons";


    let showMenu = false;

</script>



<section class="relative">
    <div class="hidden lg:inline">
        <div class="grid grid-cols-12 p-3  border-b-2">
            <div class="col-span-8 flex flex-row gap-8 items-center px-3">
                <div class="cursor-pointer">
                    <img class= "" src="https://cdn-resources.ableton.com/80bA26cPQ1hEJDFjpUKntxfqdmG3ZykO/static/images/ableton-hallmark.ef5355379032.svg" alt="">
                </div>    
                <div class="cursor-pointer"> Live </div>
                <div class="cursor-pointer"> Push </div>
                <div class="cursor-pointer"> Note</div>
                <div class="cursor-pointer"> Link </div>
                <div class="cursor-pointer"> Shop </div>
                <div class="cursor-pointer"> Packs </div>
                <div class="cursor-pointer"> Help </div>
                <div class="text-orange-500 font-bold"> More + </div>
            </div>
            <div class="col-span-4 flex flex-row gap-3 justify-end px-4">
                <div class="text-sky-600 font-bold cursor-pointer"> Try Live 12 for free</div>
                <div class=" cursor-pointer"> Login or register</div>
            </div>
        </div>
    
        <div class="flex flex-row gap-3 p-5">
            <div class="text-orange-500 font-bold cursor-pointer">About</div>
            <div class="cursor-pointer">Jobs</div>
            <div class="cursor-pointer">Apprenticeships</div>
        </div>
    </div>
    <div class="lg:hidden">
        <div class="grid grid-cols-12 p-3 border-b-2">
            <div class="col-span-4 flex flex-row gap-8 items-center px-3 ">
                <div class="cursor-pointer flex items-center z-20 {showMenu ? 'text-white': ''}">
                    <svg class="mr-5" fill="{showMenu ? 'white': ''}" version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
                        width="45px" height="21px" viewBox="0 0 45 21" enable-background="new 0 0 45 21" xml:space="preserve">
                    <g>
                        <rect width="3" height="21"/>
                        <rect x="6" width="3" height="21"/>
                        <rect x="12" width="3" height="21"/>
                        <rect x="18" width="3" height="21"/>
                        <g>
                            <rect x="24" y="18" width="21" height="3"/>
                            <rect x="24" y="12" width="21" height="3"/>
                            <rect x="24" y="6" width="21" height="3"/>
                            <rect x="24" width="21" height="3"/>
                        </g>
                    </g>
                    </svg>
                    <!-- svelte-ignore missing-declaration -->
                    <!-- svelte-ignore a11y-click-events-have-key-events -->
                    <!-- svelte-ignore a11y-no-static-element-interactions -->
                    <div class="flex items-center " on:click={() => showMenu = !showMenu}>
                        <span class="mr-2 font-bold">Menu</span> 
                        {#if showMenu}
                            <ChevronDown />
                        {:else}
                            <ChevronUp />
                        {/if}   
                    </div>
                </div>    
            </div>
        </div>
        <div class="flex flex-row gap-3 p-5">
            <div class="text-orange-500 font-bold cursor-pointer">About</div>
            <div class="cursor-pointer">Jobs</div>
            <div class="cursor-pointer">Apprenticeships</div>
        </div>
        {#if showMenu}
            <div  transition:slide={{ duration: 500, axis: 'y' }} class="lg:hidden bg-blue-700 text-white absolute z-10 pt-10 top-0 w-full ">
                <div class="flex flex-col gap-3 p-5">
                    <div class="cursor-pointer">Live</div>
                    <div class="cursor-pointer">Push</div>
                    <div class="cursor-pointer">Note</div>
                    <div class="cursor-pointer">Link</div>
                    <div class="cursor-pointer">Shop</div>
                    <div class="cursor-pointer">Packs</div>
                    <div class="cursor-pointer">Help</div>
                    <div class="cursor-pointer">Try Live 12 for free</div>
                    <div class="cursor-pointer text-xs">Login in or register</div>
                    <div class="cursor-pointer">More on Ableton.com:</div>
                    <div class="cursor-pointer text-xs">Blog</div>
                    <div class="cursor-pointer text-xs">Ableton for the Classroom</div>
                    <div class="cursor-pointer text-xs">Ableton for Collegues and Universities</div>
                    <div class="cursor-pointer text-xs">Certified Training</div>
                    <div class="cursor-pointer text-orange-500 text-xs">About Ableton</div>
                    <div class="cursor-pointer text-xs">Jobs</div>
                    <div class="cursor-pointer text-xs">Apprenticeships</div>
                </div>
                <div class="grid grid-cols-12  p-5">
                    <div class="col-span-12 font-bold text-md">More from Ableton:</div>
                    <div class="col-span-3 text-xs">
                        Loop <br>
                        Watch Talks, Performances and Features from <br>
                        Ableton's Summit for Music Makers
                    </div>
                    <div class="col-span-3 text-xs">
                        Learning Music <br>
                        Learn the fundamentals of music  <br>
                        making right in your browser.
                    </div>
                    <div class="col-span-3 text-xs">
                        Learnings Synths <br>
                        Get started with synthesis using a web-based <br>
                        synth and accompanying lessons.
                    </div>
                    <div class="col-span-3 text-xs">
                        Making Music <br>
                        Some tips from 74 Creative Strategies for <br>
                        Electronic Producers.
                    </div>
                </div>
            </div>
        {/if}
    </div>
</section>

<section>
    <div class="flex justify-center relative">
        <img class="w-4/5" 
        src="https://ableton-production.imgix.net/about/header.jpg?auto=format&dpr=2&fit=crop&fm=jpg&h=1059&ixjsv=1.1.3&q=50&w=1263&quot" alt="">
        <p class="absolute top-1/2 text-orange-600 text-7xl font-bold">Ableton</p>
    </div>
</section>

<section class="mt-14 flex justify-center">
    <div class="flex flex-col items-center w-4/5 sm:w-full">
        <p class="text-xl font-bold w-full sm:w-1/2 lg:w-2/6">
            We make Live, Push, Note and Link — unique software and hardware for 
            music creation and performance. With these products, our community of users creates amazing things.
        </p>
        <p class="w-full sm:w-1/2 lg:w-2/6 mt-4">
            Ableton was founded in 1999 and released the first version of Live in 2001. Our products are used by a community of dedicated musicians, sound designers, and artists from across the world.  
        </p>
    </div>
</section>

<section class="mt-14 h-[40rem] lg:h-[60rem] relative">
    <div class="grid grid-cols-12 h-full">
        <div class="col-span-5"></div>
        <div class="col-span-7 bg-yellow-200"></div>
    </div>
 <div class="absolute top-0 w-full h-full flex justify-center">
    <div class="grid grid-cols-12 w-4/5 ">
        <div class="col-span-8  px-8 relative top-[25%]">
            <img class="" src="https://ableton-production.imgix.net/about/photo-1.jpg?dpr=2.0&fit=crop&h=518&ixjsv=1.1.3&q=50&w=518&quot" alt="">
        </div>
        <div class="relative col-span-4 top-[35%]">
            <img src="https://ableton-production.imgix.net/about/photo-2.jpg?dpr=2.0&fit=crop&h=311&ixjsv=1.1.3&q=50&w=414&quot" alt="">
        </div>
    </div>    
</div>
    
</section>



<section class="mt-14 flex justify-center">
    <div class="flex flex-col items-center w-4/5 sm:w-full">
        <p class="text-xl font-bold w-full sm:w-1/2 lg:w-2/6">
            Making music isn't easy. It takes time, effort, and learning. 
            But when you're in the flow, it's incredibly rewarding.
        </p>
        <p class="w-full sm:w-1/2 lg:w-2/6 mt-4">
            We feel the same way about making Ableton products. The driving force behind Ableton 
            is our passion for what we make, and the people we make it for.        </p>
    </div>
</section>

<!-- <section>
    <iframe src="https://www.youtube.com/watch?v=G64-yM0Bs78" frameborder="0" title="YouTube Video"></iframe>
    <video controls tabindex="-1" src="https://www.youtube.com/watch?v=G64-yM0Bs78">
        <track kind="captions">
    </video>
</section> -->

<section class="mt-14 flex justify-center">
    <div class="flex flex-col items-center w-4/5 sm:w-full">
        <p class="text-xl font-bold w-full sm:w-1/2 lg:w-2/6">
            We are more than 350 people from 30 different countries divided between our 
            headquarters in Berlin and our offices in Los Angeles and Tokyo.
        </p>
        <p class="w-full sm:w-1/2 lg:w-2/6 mt-4">
            Most of us are active musicians, producers, and DJs, and many of us use Live and Push every day. We come from a wide range of cultural and professional backgrounds. Some of us have PhDs, some are self-taught, and most of us are somewhere in between. What connects us is the shared belief that each of us has the skills and
            knowledge to contribute to something big: helping to shape the future of music culture.        </p>
    </div>
</section>

<section class="mt-14 h-[40rem] lg:h-[60rem] relative">
    <div class="grid grid-cols-12 h-full">
        <div class="col-span-7 bg-[#B6FFC0]"></div>
        <div class="col-span-5 "></div>
    </div>
 <div class="absolute top-0 w-full h-full flex justify-center">
    <div class="grid grid-cols-12 w-4/5 ">
        <div class="col-span-8  px-8 relative top-[25%]">
            <img class="" src="https://ableton-production.imgix.net/about/photo-1.jpg?dpr=2.0&fit=crop&h=518&ixjsv=1.1.3&q=50&w=518&quot" alt="">
        </div>
        <div class="relative col-span-4 top-[35%]">
            <img src="https://ableton-production.imgix.net/about/photo-2.jpg?dpr=2.0&fit=crop&h=311&ixjsv=1.1.3&q=50&w=414&quot" alt="">
        </div>
    </div>    
</div>
    
</section>


<section class="mt-14 flex justify-center">
    <div class="flex flex-col items-center w-4/5 sm:w-full">
        <p class="text-xl font-bold w-full sm:w-1/2 lg:w-2/6">
            We believe it takes focus to create truly outstanding instruments. 
            We only work on a few products and we strive to make them great.
        </p>
        <p class="w-full sm:w-1/2 lg:w-2/6 mt-4">
            Rather than having a one-size-fits-all process, we try to give our people what they need to work their magic and grow. We’ve learned that achieving the best results comes from building teams that are richly diverse, and thus able to explore problems from a wider set of perspectives. 
            We don't always agree with each other, but opinion and debate are valued and openly encouraged.        
        </p>
    </div>
</section>

<section class="mt-14 h-[40rem] lg:h-[60rem]">
    <div class="flex justify-center h-full relative">
        <div class="w-4/5 h-full bg-[#D5B3FF]"></div>

        <div class="absolute top-0 w-full h-full flex justify-center">
            <div class="grid grid-cols-12 justify-center items-center">
                <div class="relative pl-8 col-span-4">
                    <img src="https://ableton-production.imgix.net/about/photo-6-a.jpg?dpr=2.0&fit=crop&h=311&ixjsv=1.1.3&q=50&w=414&quot" alt="">
                </div>
                <div class="col-span-1"></div>
                <div class="col-span-7 pl-20 relative h-[70%] ">
                    <img class="object-cover w-full h-full" src="https://ableton-production.imgix.net/about/photo-7.jpg?dpr=2.0&fit=crop&h=518&ixjsv=1.1.3&q=50&w=518&quot" alt="">
                </div>
            </div>
    </div>
</section>

<section class="mt-14 flex justify-center">
    <div class="flex flex-col items-center w-4/5 sm:w-full">
        <p class="text-xl font-bold w-full sm:w-1/2 lg:w-2/6">
            We want our employees to love it here. Since we’re looking for exceptional talent from 
            around the world, we will do everything we can to make your transition as easy as possible.
        </p>
        <p class="w-full sm:w-1/2 lg:w-2/6 mt-4">
            If you're joining us in Berlin, we'll help with relocation and paperwork. We'll even provide you with free German or English lessons. Plus, working in Germany means you can expect comprehensive health insurance for you and your family, as well as generous 
            maternity and paternity leave. Office hours are flexible, but it's not all work; we have several company and team outings throughout the year as well as a variety of fun, informal small-group activities.
        </p>
    </div>
</section>

<section class="mt-14 grid justify-items-center">
    <div class="md:grid md:grid-cols-12 w-5/6  border">
        <div class="col-span-6">
            <img class="h-full object-cover" src="https://ableton-production.imgix.net/about/photo-8.jpg?crop=right&dpr=2.0&fit=crop&h=667&ixjsv=1.1.3&q=50&w=667&quot" alt="">
        </div>
        <div class="col-span-6  p-12 md:p-20 lg:p-20 bg-[#B1C5FF] text-black font-bold  flex flex-col justify-center">
            <p class="text-justify">
                We're really proud of the work we've done so far. But there's so much more to come. 
                If you'd like to be a part of it, please join us.
            </p>
            <span class="text-[#0000ff] text-left mt-4">See Latest jobs</span>
        </div>
    </div>
</section>


<footer class="mt-14 border-t">
    <div class="p-10">
        <h1 class="text-4xl font-bold mb-5">Ableton</h1>
        <div class="grid gap-y-6 grid-flow-row lg:grid-rows-3 lg:grid-cols-12 lg:grid-flow-col lg:gap-x-4">
            <div class="row-span-3 col-span-3 ">
                Register Live or Push <br>
                About Ableton <br>
                <div class="flex flex-row gap-3 mt-2">
                    <Facebook fill="blue" /> <TwitterX /> <Instagram /> <Youtube fill="red" />
                    <Tiktok />
                </div>
            </div>
            <div class="row-span-3 col-span-8 lg:col-span-3 ">
                <span class="font-bold">Education</span> <br>
                Offers for students and teachers <br>
                Ableton for the classroom <br>
                Ableton for colleges and universities <br>
            </div>
            <div class="row-span-3 col-span-8 ">
                <p>
                    <span class="font-bold ">Sign up to our newsletter</span> <br>
                    Enter your email address to stay up to date with the latest offers, 
                    tutorials, downloads, surveys and more.
                </p>
                <div class="grid grid-cols-12 border mt-5">
                    <input class="col-span-9 bg-neutral-200 p-1"  type="text" placeholder="Email Address" >
                    <button class="col-span-3 text-white p-1 bg-blue-600">Sign up</button>
                </div>
            </div>
        </div>
    </div>
    <div class="p-10">
        <div class="grid gap-y-6 grid-flow-row lg:grid-rows-3 lg:grid-cols-12 lg:grid-flow-col lg:gap-x-4">
            <div class="row-span-3 col-span-3 ">
                <span class="font-bold">Community</span> <br>
                Find Ableton User Groups <br>
                Find Certified Training <br>
                Become a Certified Trainer <br>
                
            </div>
            <div class="row-span-3 col-span-8 lg:col-span-3">
                <span class="font-bold">
                    Language and location
                </span> <br>
                <div class="grid grid-cols-12 w-1/2 lg:w-full mt-2 gap-x-1">
                    <select class="bg-[#eee] col-span-5">
                        <option value="en">English</option>
                        <option value="es">日本語</option>
                        <option value="fr">한국어</option>
                        <option value="de">Deutsch</option>
                        <option value="it">Italiano</option>
                    </select>
                    <select class="bg-[#eee] col-span-7">
                        <option value="de">Cameroon</option>
                        <option value="it">Nigeria</option>
                        <option value="en">Germany</option>
                        <option value="es">France</option>
                        <option value="fr">England</option>
                    </select>
                </div>
            </div>
           
        </div>
    </div>

    <div class="grid lg:grid-cols-12 px-7 pb-12">
        <div class="col-span-8 flex flex-col lg:flex-row gap-8 lg:items-center px-3 text-sm font-bold">    
            <div class="cursor-pointer"> Contact Us </div>
            <div class="cursor-pointer"> Press Resources </div>
            <div class="cursor-pointer"> Legal Info</div>
            <div class="cursor-pointer"> Privacy Policy </div>
            <div class="cursor-pointer"> Cookie Settings </div>
            <div class="cursor-pointer"> Imprint </div>
            
        </div>
        <div class="col-span-4 flex flex-row gap-3 lg:justify-end px-4 mt-14 lg:mt-0">
            <img class="lg:hidden" src="https://cdn-resources.ableton.com/80bA26cPQ1hEJDFjpUKntxfqdmG3ZykO/static/images/ableton-hallmark.ef5355379032.svg" alt="">
            <div class=" cursor-pointer"> Made in Berlin </div>
            <img class= "hidden lg:inline" src="https://cdn-resources.ableton.com/80bA26cPQ1hEJDFjpUKntxfqdmG3ZykO/static/images/ableton-hallmark.ef5355379032.svg" alt="">
        </div>
    </div>
</footer>



<style>

</style>