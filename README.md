#import React from "react"; import { motion } from "framer-motion";

// Moses Hacker-Themed Portfolio (single-file React + Tailwind + Framer Motion) // What to do after downloading: // 1) Place your profile image (the one you uploaded) at: public/assets/moses-profile.jpg //    - Or update the image path below to wherever you host it. // 2) Sign up at Formspree and replace FORMSPREE_ENDPOINT with your form endpoint (looks like https://formspree.io/f/xyz). // 3) Run this in a React app (CRA / Vite) with Tailwind and framer-motion installed.

export default function MosesWebsite() { const FORMSPREE_ENDPOINT = "https://formspree.io/f/yourFormID"; // <- replace with your Formspree form ID

return ( <div className="min-h-screen bg-black text-gray-100 font-sans"> {/* Background glow + subtle matrix lines */} <div className="absolute inset-0 -z-10 bg-gradient-to-b from-black via-zinc-900 to-black"> <div className="absolute inset-0 opacity-30 bg-[url('/assets/matrix-grid.png')] bg-repeat" /> </div>

<header className="max-w-6xl mx-auto p-6 flex items-center justify-between">
    <div className="flex items-center gap-4">
      {/* Inline SVG logo: "Moses Light" italic hacker style */}
      <div className="w-14 h-14 rounded-lg bg-gradient-to-br from-emerald-600 to-cyan-400 flex items-center justify-center shadow-lg">
        <svg viewBox="0 0 200 60" className="w-28 h-10" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <linearGradient id="g" x1="0" x2="1">
              <stop offset="0" stopColor="#8AFFC1" />
              <stop offset="1" stopColor="#6EE7F2" />
            </linearGradient>
          </defs>
          <text x="0" y="42" fontFamily="Inter, Arial" fontSize="36" fontStyle="italic" fontWeight="700" fill="url(#g)">Moses</text>
          <text x="95" y="42" fontFamily="Inter, Arial" fontSize="20" fontStyle="italic" fontWeight="600" fill="#0f766e">Light</text>
        </svg>
      </div>

      <div>
        <h1 className="text-xl font-semibold tracking-tight">Moses Clinton</h1>
        <p className="text-xs text-gray-400">Moses Clinton — Hacker, Developer & Gaming Creator</p>
      </div>
    </div>

    <nav className="hidden md:flex gap-6 items-center text-sm">
      <a href="#work" className="hover:text-emerald-400">Work</a>
      <a href="#services" className="hover:text-emerald-400">Services</a>
      <a href="#about" className="hover:text-emerald-400">About</a>
      <a href="#contact" className="px-4 py-2 rounded-lg bg-emerald-600/10 border border-emerald-600 text-emerald-300">Contact</a>
    </nav>
  </header>

  <main className="max-w-6xl mx-auto p-6">
    {/* HERO */}
    <section className="grid grid-cols-1 md:grid-cols-2 gap-8 items-center py-12">
      <motion.div initial={{ x: -20, opacity: 0 }} animate={{ x: 0, opacity: 1 }} transition={{ duration: 0.6 }}>
        <h2 className="text-5xl font-extrabold leading-tight">I break systems, then build them better.</h2>
        <p className="mt-4 text-gray-400 max-w-xl">Dark hacker aesthetics, secure-first development, and high-performance streaming assets for creators. I design, audit, and ship production-ready apps and visual identities.</p>

        <div className="mt-6 flex gap-4">
          <a href="#contact" className="inline-block px-6 py-3 rounded-lg bg-emerald-500 text-black font-semibold">Start a project</a>
          <a href="#work" className="inline-block px-6 py-3 rounded-lg bg-transparent border border-zinc-700">View work</a>
        </div>

        <div className="mt-8 grid grid-cols-2 gap-4">
          <div className="bg-zinc-900/60 p-4 rounded-lg">
            <p className="text-xs text-gray-400">Experience</p>
            <p className="text-xl font-semibold">4+ years</p>
          </div>
          <div className="bg-zinc-900/60 p-4 rounded-lg">
            <p className="text-xs text-gray-400">Clients</p>
            <p className="text-xl font-semibold">20+</p>
          </div>
        </div>
      </motion.div>

      <motion.div initial={{ scale: 0.98, opacity: 0 }} animate={{ scale: 1, opacity: 1 }} transition={{ duration: 0.6 }} className="flex items-center justify-center">
        {/* Profile card with user image (place your uploaded image at public/assets/moses-profile.jpg) */}
        <div className="w-full max-w-sm p-6 bg-gradient-to-br from-zinc-900/80 to-zinc-800/80 rounded-3xl shadow-2xl border border-zinc-700">
          <div className="w-full h-64 rounded-xl overflow-hidden border border-zinc-700">
            <img src="/assets/moses-profile.jpg" alt="Moses profile" className="w-full h-full object-cover" />
          </div>

          <div className="mt-4">
            <h3 className="font-semibold text-lg">Moses Clinton</h3>
            <p className="text-xs text-gray-400">Hacker • Developer • Gaming Creator</p>
          </div>
        </div>
      </motion.div>
    </section>

    {/* SERVICES */}
    <section id="services" className="py-12">
      <h3 className="text-2xl font-bold">Services</h3>
      <p className="text-gray-400 mt-2">Secure app development, UI/UX for streamers, brand identity, and visual assets for gaming creators.</p>

      <div className="mt-6 grid grid-cols-1 md:grid-cols-3 gap-6">
        <div className="bg-zinc-900 p-6 rounded-xl border border-zinc-700">
          <h4 className="font-semibold text-lg">Full-stack Development</h4>
          <p className="mt-2 text-gray-400">React, Node, and secure deployment practices.</p>
        </div>
        <div className="bg-zinc-900 p-6 rounded-xl border border-zinc-700">
          <h4 className="font-semibold text-lg">Streaming & Visuals</h4>
          <p className="mt-2 text-gray-400">Stream overlays, wallpapers, profile images and motion assets.</p>
        </div>
        <div className="bg-zinc-900 p-6 rounded-xl border border-zinc-700">
          <h4 className="font-semibold text-lg">Security Audits</h4>
          <p className="mt-2 text-gray-400">Vulnerability spotting, hardening and remediation plans.</p>
        </div>
      </div>
    </section>

    {/* WORK */}
    <section id="work" className="py-12">
      <h3 className="text-2xl font-bold">Selected projects</h3>
      <p className="text-gray-400 mt-2">A few projects — demos and case studies.</p>

      <div className="mt-6 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
        {Array.from({ length: 6 }).map((_, i) => (
          <article key={i} className="bg-zinc-900 rounded-lg overflow-hidden border border-zinc-700">
            <div className="h-36 bg-gradient-to-br from-emerald-700 to-cyan-500 flex items-center justify-center font-bold text-lg">Project {i + 1}</div>
            <div className="p-4">
              <h4 className="font-semibold">Project {i + 1}</h4>
              <p className="text-sm text-gray-400">Demo case study and quick summary.</p>
              <div className="mt-4">
                <a href="#" className="text-sm underline">View case</a>
              </div>
            </div>
          </article>
        ))}
      </div>
    </section>

    {/* ABOUT */}
    <section id="about" className="py-12 bg-zinc-900/40 rounded-xl p-6">
      <h3 className="text-2xl font-bold">About</h3>
      <p className="text-gray-400 mt-2 max-w-3xl">I'm Moses — I blend offensive thinking with practical engineering: building products, designing visuals for streamers, and securing apps. Based in Lagos, Nigeria.</p>

      <div className="mt-6 grid grid-cols-1 md:grid-cols-3 gap-4">
        <div className="bg-zinc-800 p-4 rounded-lg">
          <p className="text-xs text-gray-400">Location</p>
          <p className="font-semibold">Lagos, Nigeria</p>
        </div>
        <div className="bg-zinc-800 p-4 rounded-lg">
          <p className="text-xs text-gray-400">Availability</p>
          <p className="font-semibold">Freelance / Collaborations</p>
        </div>
        <div className="bg-zinc-800 p-4 rounded-lg">
          <p className="text-xs text-gray-400">Email</p>
          <p className="font-semibold">moseskk29@gmail.com</p>
        </div>
      </div>
    </section>

    {/* CONTACT */}
    <section id="contact" className="py-12">
      <h3 className="text-2xl font-bold">Contact</h3>
      <p className="text-gray-400 mt-2">Interested in working together? Send a message or use the quick mail link.</p>

      <div className="mt-6 grid grid-cols-1 md:grid-cols-2 gap-6">
        <form
          className="bg-zinc-900 p-6 rounded-lg border border-zinc-700"
          action={FORMSPREE_ENDPOINT}
          method="POST"
          onSubmit={(e) => {
            // If user didn't replace FORMSPREE_ENDPOINT, fallback to mailto as a graceful degradation.
            if (FORMSPREE_ENDPOINT.includes("yourFormID")) {
              e.preventDefault();
              const f = e.target;
              const name = f.elements["name"].value;
              const email = f.elements["email"].value;
              const message = f.elements["message"].value;
              window.location.href = `mailto:moseskk29@gmail.com?subject=${encodeURIComponent("Website contact from " + name)}&body=${encodeURIComponent(message + "

From: " + email)}`; return; } }} > <label className="block text-sm text-gray-300">Name</label> <input name="name" className="w-full mt-2 p-3 rounded bg-zinc-800 text-white" required />

<label className="block text-sm text-gray-300 mt-4">Email</label>
          <input name="email" type="email" className="w-full mt-2 p-3 rounded bg-zinc-800 text-white" required />

          <label className="block text-sm text-gray-300 mt-4">Message</label>
          <textarea name="message" className="w-full mt-2 p-3 rounded bg-zinc-800 text-white" rows={4} required />

          <div className="mt-4">
            <button type="submit" className="px-5 py-3 rounded-lg bg-emerald-500 text-black font-semibold">Send message</button>
          </div>
        </form>

        <div className="bg-zinc-900 p-6 rounded-lg border border-zinc-700">
          <h4 className="font-semibold">Quick contact</h4>
          <p className="text-gray-400 mt-2">Email: <a href="mailto:moseskk29@gmail.com" className="underline">moseskk29@gmail.com</a></p>
          <p className="text-gray-400 mt-2">Or reach me on social: Twitch / Twitter / GitHub</p>

          <div className="mt-4 flex gap-3">
            <a href="#" className="px-4 py-2 rounded bg-zinc-800 border border-zinc-700">Twitter</a>
            <a href="#" className="px-4 py-2 rounded bg-zinc-800 border border-zinc-700">Twitch</a>
            <a href="#" className="px-4 py-2 rounded bg-zinc-800 border border-zinc-700">GitHub</a>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer className="border-t border-zinc-800 mt-12 py-6">
    <div className="max-w-6xl mx-auto px-6 flex flex-col md:flex-row items-center justify-between gap-4">
      <p className="text-sm text-gray-400">© {new Date().getFullYear()} Moses Clinton — Hacker Theme.</p>
      <div className="text-sm text-gray-400">Built with React & Tailwind.</div>
    </div>
  </footer>
</div>

); } moses-light-portfolio
# 💡 Moses Light — Hacker & Developer Portfolio

Welcome to my official portfolio website.  
I'm **Moses Clinton**, also known as *Moses Light* — a passionate hacker, developer, and gaming creator.  
I blend creativity, technology, and cybersecurity to build powerful, clean digital experiences.

---

## 🚀 Live Demo
🌐 **[View My Site](https://moseslight001.github.io/moses-light-portfolio/)**

---

## 🧠 About Me
I’m a creator who loves combining hacking knowledge, development skills, and gaming creativity.  
Every project I build is designed with precision, dark aesthetics, and interactive energy.

---

## 🧩 Built With
- HTML  
- CSS  
- JavaScript  

---

## 📧 Contact
If you’d like to collaborate or reach out:  
📩 **moseskk29@gmail.com**

---

© 2025 Moses Light. All Rights Reserved.
