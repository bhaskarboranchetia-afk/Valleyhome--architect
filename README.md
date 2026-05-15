export default function ValleyHomeArchitect() { const testimonials = [ { name: 'Rupam Gogoi', text: 'ValleyHome Architect transformed our vision into a stunning modern home. The design quality and site guidance were exceptional.', }, { name: 'Mitali Saikia', text: 'Professional, creative, and highly responsive. Our interiors were delivered exactly as promised.', }, { name: 'Amit Dutta', text: 'Excellent Vastu-based planning and premium architectural presentation.', }, ];

const projects = [ { title: 'Luxury Residence', category: 'Residential Architecture', image: 'https://images.unsplash.com/photo-1511818966892-d7d671e672a2?auto=format&fit=crop&w=1200&q=80', }, { title: 'Contemporary Villa', category: 'Vastu-Optimized Design', image: 'https://images.unsplash.com/photo-1502672260266-1c1ef2d93688?auto=format&fit=crop&w=1200&q=80', }, { title: 'Terracotta Courtyard Home', category: 'Modern Traditional Fusion', image: 'https://images.unsplash.com/photo-1494526585095-c41746248156?auto=format&fit=crop&w=1200&q=80', }, ];

const services = [ 'Architectural Design', '3D Elevation & Visualization', 'Interior Design', 'Vastu Consultation', 'Construction Drawings', 'Turnkey Project Management', ];

return ( <div className="min-h-screen bg-stone-950 text-stone-100"> {/* Header */} <header className="fixed top-0 left-0 right-0 z-50 bg-stone-950/80 backdrop-blur border-b border-stone-800"> <div className="max-w-7xl mx-auto px-6 py-4 flex items-center justify-between"> <div className="flex items-center gap-4"> <div className="w-12 h-12 rounded-2xl bg-gradient-to-br from-yellow-200 via-yellow-400 to-amber-700 flex items-center justify-center shadow-2xl ring-2 ring-yellow-200/40"> <span className="text-stone-950 font-black text-xl tracking-tight">VH</span> </div> <div> <h1 className="text-xl font-semibold tracking-[0.2em] uppercase">ValleyHome Architect</h1> <p className="text-xs text-stone-400 tracking-[0.3em] uppercase">Designing Luxury with Harmony</p> </div> </div> <nav className="hidden md:flex gap-8 text-sm text-stone-300"> <a href="#projects" className="hover:text-orange-300">Projects</a> <a href="#services" className="hover:text-orange-300">Services</a> <a href="#about" className="hover:text-orange-300">About</a> <a href="#contact" className="hover:text-orange-300">Contact</a> </nav> </div> </header>

{/* Hero */}
  <section
    className="relative min-h-screen flex items-center"
    style={{
      backgroundImage:
        'linear-gradient(to right, rgba(12,10,9,0.9), rgba(12,10,9,0.55)), url(https://images.unsplash.com/photo-1600585154526-990dced4db0d?auto=format&fit=crop&w=1800&q=80)',
      backgroundSize: 'cover',
      backgroundPosition: 'center',
    }}
  >
    <div className="max-w-7xl mx-auto px-6 pt-24">
      <div className="max-w-4xl">
        <p className="text-orange-300 tracking-[0.4em] uppercase text-sm mb-4">
          Luxury Modern Architecture
        </p>
        <h2 className="text-5xl md:text-8xl font-light leading-tight">
          Innovative Architecture
          <span className="block text-orange-300">Rooted in Vastu</span>
        </h2>
        <p className="mt-8 text-lg md:text-xl text-stone-300 leading-8 max-w-2xl">
          ValleyHome Architect creates premium residences and commercial spaces
          with contemporary design, terracotta accents, and harmonious spatial
          planning.
        </p>
        <div className="mt-10 flex flex-wrap gap-4">
          <a
            href="#contact"
            className="px-8 py-4 rounded-2xl bg-orange-500 text-stone-950 font-semibold shadow-2xl"
          >
            Start Your Project
          </a>
          <a
            href="#projects"
            className="px-8 py-4 rounded-2xl border border-stone-600 text-stone-100"
          >
            View Portfolio
          </a>
        </div>
      </div>
    </div>
  </section>

  {/* Stats */}
  <section className="max-w-7xl mx-auto px-6 -mt-20 relative z-10">
    <div className="grid md:grid-cols-4 gap-6">
      {[
        ['150+', 'Design Concepts'],
        ['50+', 'Completed Projects'],
        ['100%', 'Vastu Consideration'], 
        ['9', 'Numerology-Inspired Brand Number'], 
      ].map(([value, label]) => (
        <div key={label} className="bg-stone-900/90 border border-stone-800 rounded-3xl p-8 shadow-2xl">
          <div className="text-4xl font-light text-orange-300">{value}</div>
          <div className="mt-2 text-stone-400">{label}</div>
        </div>
      ))}
    </div>
  </section>

  {/* Projects */}
  <section id="projects" className="max-w-7xl mx-auto px-6 py-28">
    <div className="mb-12">
      <p className="text-orange-300 tracking-[0.3em] uppercase text-sm">Portfolio</p>
      <h3 className="text-4xl md:text-6xl font-light mt-3">Signature Projects</h3>
    </div>
    <div className="grid md:grid-cols-3 gap-8">
      {projects.map((project) => (
        <div key={project.title} className="group overflow-hidden rounded-3xl bg-stone-900 border border-stone-800">
          <img
            src={project.image}
            alt={project.title}
            className="h-80 w-full object-cover group-hover:scale-105 transition duration-700"
          />
          <div className="p-6">
            <p className="text-orange-300 text-sm uppercase tracking-[0.2em]">{project.category}</p>
            <h4 className="text-2xl font-light mt-2">{project.title}</h4>
          </div>
        </div>
      ))}
    </div>
  </section>

  {/* Services */}
  <section id="services" className="bg-stone-900 border-y border-stone-800">
    <div className="max-w-7xl mx-auto px-6 py-28 grid lg:grid-cols-2 gap-16 items-center">
      <div>
        <p className="text-orange-300 tracking-[0.3em] uppercase text-sm">Services</p>
        <h3 className="text-4xl md:text-6xl font-light mt-3">Design Excellence</h3>
        <p className="mt-6 text-stone-300 leading-8 text-lg">
          Every project balances aesthetics, functionality, climate response,
          and traditional spatial wisdom.
        </p>
      </div>
      <div className="grid sm:grid-cols-2 gap-4">
        {services.map((service) => (
          <div key={service} className="p-6 rounded-2xl bg-stone-950 border border-stone-800">
            {service}
          </div>
        ))}
      </div>
    </div>
  </section>

  {/* About */}
  <section id="about" className="max-w-7xl mx-auto px-6 py-28 grid lg:grid-cols-2 gap-16">
    <div>
      <p className="text-orange-300 tracking-[0.3em] uppercase text-sm">About</p>
      <h3 className="text-4xl md:text-6xl font-light mt-3">ValleyHome Architect</h3>
    </div>
    <div className="text-stone-300 text-lg leading-8">
      ValleyHome Architect specializes in luxury modern residences with
      terracotta detailing, premium materials, and deeply considered planning.
      The VH logo symbolizes Vision and Harmony—an innovative identity chosen
      to represent balanced, prosperous design.
    </div>
  </section>

  {/* Contact */}
  <section id="contact" className="bg-gradient-to-br from-orange-500 to-orange-700 text-stone-950">
    <div className="max-w-7xl mx-auto px-6 py-28">
      <h3 className="text-4xl md:text-7xl font-light max-w-4xl leading-tight">
        Let's Design a Landmark That Reflects Your Vision.
      </h3>
      <p className="mt-6 text-lg max-w-2xl opacity-90">
        Share your plot details, requirements, and inspiration to receive a bespoke architectural proposal. Phone: +91 9957337943 / +91 8822641991. Email: valleyhomearchitect@gmail.com. Address: Lachit Borphukan Nagar, Path No. 2, Near Punjan Chariali, Sivasagar, Assam.
      </p>
      <div className="mt-10 flex flex-wrap gap-4">
        <a
          href="https://wa.me/91919957337943"
          className="px-8 py-4 rounded-2xl bg-stone-950 text-stone-100 font-semibold"
        >
          WhatsApp Us
        </a>
        <a
          href="mailto:valleyhomearchitect@gmail.com"
          className="px-8 py-4 rounded-2xl border border-stone-950/20"
        >
          Email Inquiry
        </a>
      </div>
    </div>
  </section>

  <section className="max-w-7xl mx-auto px-6 py-28">
    <p className="text-orange-300 tracking-[0.3em] uppercase text-sm">Client Reviews</p>
    <h3 className="text-4xl md:text-6xl font-light mt-3 mb-12">What Our Clients Say</h3>
    <div className="grid md:grid-cols-3 gap-8">
      {testimonials.map((item) => (
        <div key={item.name} className="bg-stone-900 border border-stone-800 rounded-3xl p-8">
          <div className="text-2xl mb-4">★★★★★</div>
          <p className="text-stone-300 leading-8">{item.text}</p>
          <div className="mt-6 text-orange-300 font-medium">{item.name}</div>
        </div>
      ))}
    </div>
  </section>
</div>
); }
