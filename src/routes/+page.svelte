<script lang="ts">
    // Versa Villa Images
    const heroImage = "/generated/image-stunning-modern-luxury-home-exterior-wit-1766525539361-0.webp";
    const capeCodImage = "/generated/image-elegant-cape-cod-style-luxury-home-with--1766525542498-1.webp";
    const traditionalImage = "/generated/image-classic-traditional-luxury-home-with-bri-1766525545393-2.webp";
    const modernImage = "/generated/image-contemporary-modern-luxury-home-with-cle-1766525548072-3.webp";
    const mediterraneanImage = "/generated/image-mediterranean-villa-with-terracotta-roof-1766525551080-4.webp";
    const factoryImage = "/generated/image-advanced-factory-floor-with-precision-en-1766526812739-0.webp";
    const fireResistantImage = "/generated/image-luxury-home-detail-showing-fire-resistan-1766525556373-6.webp";
    const foundersImage = "/generated/image-professional-couple-in-their-50s-archite-1766525558982-7.webp";
    const happyFamilyImage = "/generated/image-happy-affluent-family-standing-in-front--1766525561394-8.webp";
    const kitchenImage = "/generated/image-luxurious-modern-kitchen-interior-with-h-1766525564104-9.webp";
    const bedroomImage = "/generated/image-elegant-master-bedroom-with-large-window-1766525566627-10.webp";
    const livingRoomImage = "/generated/image-spacious-open-concept-living-room-with-h-1766525569198-11.webp";
    const qualityControlImage = "/generated/image-construction-worker-inspecting-modular-h-1766525571829-12.webp";
    const outdoorLivingImage = "/generated/image-beautiful-outdoor-living-space-with-pati-1766525574453-13.webp";

</script>

<div class="w-full">
    <!-- Hero Section -->
    <section class="w-full mb-16 md:mb-24 px-4 md:px-6 max-w-[1600px] mx-auto">
        <div class="relative w-full aspect-[16/9] md:aspect-[21/9] overflow-hidden">
            <img src={heroImage} alt="Versa Villa Luxury Home" class="w-full h-full object-cover" />
            <div class="absolute inset-0 bg-black/30"></div>
            <div class="absolute inset-0 flex flex-col items-center justify-center text-white text-center p-6">
                <h1 class="font-display text-4xl md:text-6xl lg:text-7xl mb-6 max-w-4xl">Your Luxury Home in Six Months</h1>
                <p class="text-lg md:text-xl font-light mb-8 max-w-2xl opacity-95">Fire-resistant modular construction. Fixed pricing. Guaranteed timeline. No compromises.</p>
                <a href="#contact" class="bg-white text-black px-8 py-4 text-sm uppercase tracking-widest hover:bg-gray-100 transition-colors">
                    Schedule Consultation
                </a>
            </div>
        </div>
    </section>

    <!-- Value Proposition -->
    <section class="max-w-[1200px] mx-auto px-6 mb-24 md:mb-32">
        <div class="text-center mb-16">
            <h2 class="font-display text-3xl md:text-4xl text-gray-900 mb-6">Why Versa Villa</h2>
            <p class="text-gray-600 text-lg max-w-2xl mx-auto font-light">
                We've reimagined luxury homebuilding for discerning homeowners who refuse to compromise on quality or timeline.
            </p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-12">
            <div class="text-center">
                <div class="text-5xl font-display mb-4 text-primary-600">6</div>
                <h3 class="text-xl font-bold mb-3 uppercase tracking-wide">Months Guaranteed</h3>
                <p class="text-gray-600 text-sm leading-relaxed font-light">
                    Move into your dream home in six months, not the 12-24 months typical of traditional construction. Our factory-controlled process eliminates delays.
                </p>
            </div>
            <div class="text-center">
                <div class="text-5xl font-display mb-4 text-primary-600">$0</div>
                <h3 class="text-xl font-bold mb-3 uppercase tracking-wide">Cost Overruns</h3>
                <p class="text-gray-600 text-sm leading-relaxed font-light">
                    Fixed pricing from day one. No surprise costs or budget overruns. Traditional builds average 20-40% over budget—we guarantee your price.
                </p>
            </div>
            <div class="text-center">
                <div class="text-5xl font-display mb-4 text-primary-600">100%</div>
                <h3 class="text-xl font-bold mb-3 uppercase tracking-wide">Fire Resistant</h3>
                <p class="text-gray-600 text-sm leading-relaxed font-light">
                    Purpose-built to exceed California's stringent wildfire codes. Advanced materials and construction techniques protect your investment and family.
                </p>
            </div>
        </div>
    </section>

    <!-- Design Styles Section -->
    <section id="models" class="max-w-[1600px] mx-auto px-6 mb-24 md:mb-32">
        <div class="text-center mb-16">
            <h2 class="font-display text-3xl md:text-4xl text-gray-900 mb-6">Four Timeless Design Styles</h2>
            <p class="text-gray-600 text-lg max-w-2xl mx-auto font-light">
                Choose from architect-developed styles, each customizable to your vision with designer-selected finish packages.
            </p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
            <div class="group cursor-pointer">
                <div class="overflow-hidden mb-4">
                    <img src={capeCodImage} alt="Cape Cod Style" class="w-full aspect-[4/3] object-cover transition-transform duration-700 group-hover:scale-105" />
                </div>
                <h3 class="text-2xl font-display mb-2">Cape Cod</h3>
                <p class="text-gray-600 text-sm font-light">Classic New England charm with modern luxury amenities</p>
            </div>
            <div class="group cursor-pointer">
                <div class="overflow-hidden mb-4">
                    <img src={traditionalImage} alt="Traditional Style" class="w-full aspect-[4/3] object-cover transition-transform duration-700 group-hover:scale-105" />
                </div>
                <h3 class="text-2xl font-display mb-2">Traditional</h3>
                <p class="text-gray-600 text-sm font-light">Timeless elegance with sophisticated architectural details</p>
            </div>
            <div class="group cursor-pointer">
                <div class="overflow-hidden mb-4">
                    <img src={modernImage} alt="Modern Style" class="w-full aspect-[4/3] object-cover transition-transform duration-700 group-hover:scale-105" />
                </div>
                <h3 class="text-2xl font-display mb-2">Modern</h3>
                <p class="text-gray-600 text-sm font-light">Clean lines and open spaces for contemporary living</p>
            </div>
            <div class="group cursor-pointer">
                <div class="overflow-hidden mb-4">
                    <img src={mediterraneanImage} alt="Mediterranean Style" class="w-full aspect-[4/3] object-cover transition-transform duration-700 group-hover:scale-105" />
                </div>
                <h3 class="text-2xl font-display mb-2">Mediterranean</h3>
                <p class="text-gray-600 text-sm font-light">Warm, inviting design inspired by coastal European villas</p>
            </div>
        </div>
    </section>

    <!-- Interior Quality Showcase -->
    <section class="w-full mb-24 md:mb-32">
        <img src={livingRoomImage} alt="Luxury Living Room" class="w-full h-[80vh] object-cover" />
    </section>

    <!-- Process Section -->
    <section id="process" class="max-w-[1200px] mx-auto px-6 mb-24 md:mb-32">
        <div class="text-center mb-16">
            <h2 class="font-display text-3xl md:text-4xl text-gray-900 mb-6">The Versa Villa Process</h2>
            <p class="text-gray-600 text-lg max-w-2xl mx-auto font-light">
                Factory precision meets luxury craftsmanship. Our streamlined process eliminates waste, delays, and uncertainty.
            </p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center mb-16">
            <div>
                <img src={factoryImage} alt="Factory Construction" class="w-full aspect-[16/9] object-cover" />
            </div>
            <div>
                <h3 class="text-2xl font-bold mb-4 uppercase tracking-wide">Factory Quality Control</h3>
                <p class="text-gray-600 text-sm leading-relaxed font-light mb-4">
                    Our factory-controlled environment applies automobile-industry quality control standards to every home. Precision-engineered modules are built with advanced materials in optimal conditions, eliminating the variables that plague traditional construction.
                </p>
                <p class="text-gray-600 text-sm leading-relaxed font-light">
                    While your modules are being constructed, we simultaneously prepare your site—a parallel efficiency approach that cuts months off traditional timelines without sacrificing quality.
                </p>
            </div>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
            <div class="order-2 md:order-1">
                <h3 class="text-2xl font-bold mb-4 uppercase tracking-wide">Stress-Free Experience</h3>
                <p class="text-gray-600 text-sm leading-relaxed font-light mb-4">
                    Our concierge project management handles everything: permits, inspections, material selection, and contractor coordination. You receive weekly updates and make selections through our intuitive online platform.
                </p>
                <p class="text-gray-600 text-sm leading-relaxed font-light">
                    Curated design packages simplify decision-making without limiting your vision. Every choice is pre-vetted for quality and compatibility, eliminating the overwhelming burden of traditional construction.
                </p>
            </div>
            <div class="order-1 md:order-2">
                <img src={qualityControlImage} alt="Quality Control" class="w-full aspect-[3/4] object-cover" />
            </div>
        </div>
    </section>

    <!-- Fire Resistance Feature -->
    <section class="max-w-[1600px] mx-auto px-6 mb-24 md:mb-32">
        <div class="grid grid-cols-1 md:grid-cols-12 gap-6 items-center">
             <div class="md:col-span-5">
                <img src={fireResistantImage} alt="Fire-Resistant Construction" class="w-full aspect-[4/5] object-cover" />
            </div>
            <div class="md:col-span-6 md:col-start-7">
                <h2 class="font-display text-3xl md:text-4xl text-gray-900 mb-6">Built for Wildfire Zones</h2>
                <p class="text-gray-600 text-sm leading-relaxed font-light mb-4">
                    Purpose-built to exceed California's stringent wildfire building codes, every Versa Villa home features advanced fire-resistant materials and construction techniques engineered specifically for wildfire-prone areas.
                </p>
                <p class="text-gray-600 text-sm leading-relaxed font-light mb-6">
                    This isn't just about safety—it's about significant insurance cost savings. Our pre-insurance benefits represent a massive selling point, with homeowners seeing substantial reductions in their insurance premiums year after year.
                </p>
                <div class="border-t border-gray-200 pt-6">
                    <p class="text-xs text-gray-400 font-light uppercase tracking-wider">
                        Serving Palisades, Altadena, Malibu, and wildfire-prone areas throughout California
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Interior Showcase Grid -->
    <section class="max-w-[1600px] mx-auto px-6 mb-24 md:mb-32">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-16 items-start">
            <img src={bedroomImage} alt="Master Bedroom" class="w-full aspect-[3/4] object-cover" />
            <div class="md:pt-32">
                 <img src={kitchenImage} alt="Luxury Kitchen" class="w-full aspect-[3/4] object-cover" />
            </div>
        </div>
        <div class="flex justify-end">
             <p class="text-xs text-gray-400 font-light max-w-md leading-relaxed">
                Every finish, fixture, and material is carefully selected from our designer-curated packages. High-end appliances, premium countertops, and sophisticated lighting come standard—luxury that maintains investment value without the overwhelming burden of endless decisions.
            </p>
        </div>
    </section>

    <!-- Outdoor Living -->
    <section class="w-full mb-24 md:mb-32">
        <img src={outdoorLivingImage} alt="Outdoor Living Space" class="w-full h-[70vh] object-cover" />
    </section>

    <!-- Founders Section -->
    <section id="founders" class="max-w-[1200px] mx-auto px-6 mb-24 md:mb-32">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
            <div>
                <img src={foundersImage} alt="Ardie and Emila Tavangarian" class="w-full aspect-[16/9] object-cover" />
            </div>
            <div>
                <h2 class="font-display text-3xl md:text-4xl text-gray-900 mb-6">Meet the Founders</h2>
                <div class="space-y-6">
                    <div>
                        <h3 class="text-xl font-bold mb-2">Ardie Tavangarian, CEO</h3>
                        <p class="text-gray-600 text-sm leading-relaxed font-light">
                            Ardie's decades in architectural excellence and construction innovation give him deep insight into luxury homebuilding inefficiencies. His vision to guarantee 6-month timelines stems from firsthand frustration with traditional construction's delays and cost overruns.
                        </p>
                    </div>
                    <div>
                        <h3 class="text-xl font-bold mb-2">Emila Tavangarian, Head of Sales</h3>
                        <p class="text-gray-600 text-sm leading-relaxed font-light">
                            Emila's experience in luxury design and client relations positions her to understand discerning homeowners' frustrations with traditional builders. Her drive comes from witnessing clients endure years of construction stress and broken promises.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Happy Homeowners -->
    <section class="max-w-[1600px] mx-auto px-6 mb-32 md:mb-40">
        <div class="relative">
            <img src={happyFamilyImage} alt="Happy Homeowners" class="w-full aspect-[16/9] object-cover" />
            <div class="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent"></div>
            <div class="absolute bottom-0 left-0 right-0 p-8 md:p-12 text-white">
                <p class="text-2xl md:text-3xl font-display mb-4 max-w-2xl">
                    "We moved into our dream home in exactly six months. No delays, no surprises, just exceptional quality."
                </p>
                <p class="text-sm font-light opacity-90">Palisades Homeowner</p>
            </div>
        </div>
    </section>

    <!-- Why Choose Us -->
    <section id="why-versa" class="bg-gray-50 py-24 mb-32">
        <div class="max-w-[1200px] mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="font-display text-3xl md:text-4xl text-gray-900 mb-6">Why Discerning Homeowners Choose Versa Villa</h2>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8 text-sm">
                <div class="bg-white p-8">
                    <h3 class="font-bold text-lg mb-3 uppercase tracking-wide">Traditional Construction</h3>
                    <ul class="space-y-2 text-gray-600 font-light">
                        <li>• 12-24 months to completion</li>
                        <li>• 20-40% cost overruns typical</li>
                        <li>• Endless decisions and stress</li>
                        <li>• Weather delays and quality issues</li>
                        <li>• Constant contractor coordination</li>
                        <li>• Variable on-site quality control</li>
                    </ul>
                </div>
                <div class="bg-black text-white p-8">
                    <h3 class="font-bold text-lg mb-3 uppercase tracking-wide">Versa Villa</h3>
                    <ul class="space-y-2 font-light">
                        <li>• 6 months guaranteed timeline</li>
                        <li>• Fixed pricing, zero surprises</li>
                        <li>• Curated choices, stress-free</li>
                        <li>• Factory precision, no delays</li>
                        <li>• Concierge project management</li>
                        <li>• Automobile-industry quality standards</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Final CTA -->
    <section id="contact" class="w-full mb-32">
        <div class="max-w-[1200px] mx-auto px-6">
            <div class="bg-primary-950 text-white p-12 md:p-20 text-center">
                <h2 class="font-display text-3xl md:text-5xl mb-6">Ready to Build Your Dream Home?</h2>
                <p class="text-lg font-light mb-8 opacity-90 max-w-2xl mx-auto">
                    Schedule a consultation to explore your design options, review our process, and discover how we can deliver your luxury home in just six months.
                </p>
                <div class="flex flex-col sm:flex-row gap-4 justify-center">
                    <a href="#" class="bg-white text-black px-8 py-4 text-sm uppercase tracking-widest hover:bg-gray-100 transition-colors">
                        Schedule Consultation
                    </a>
                    <a href="#" class="border border-white text-white px-8 py-4 text-sm uppercase tracking-widest hover:bg-white hover:text-black transition-colors">
                        Virtual Walkthrough
                    </a>
                </div>
                <p class="text-xs mt-8 opacity-75">Serving Palisades, Altadena, Malibu, and all of California</p>
            </div>
        </div>
    </section>
</div>

