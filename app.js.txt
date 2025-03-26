document.addEventListener("DOMContentLoaded", () => {
  // GSAP Animations for Sections

  // Hero Section (Welcome Page)
  gsap.from("#welcome .title", { opacity: 0, y: -50, duration: 1.5, delay: 0.5 });
  gsap.from("#welcome .subtitle", { opacity: 0, y: 30, duration: 1.5, delay: 1 });
  gsap.from(".cta-button", { opacity: 0, y: 20, duration: 1.5, delay: 1.5 });

  // Love Notes Animation
  gsap.from("#loveNotes h2", { opacity: 0, y: -50, duration: 1 });
  gsap.from("#loveNotes .note", { opacity: 0, y: 30, duration: 1, delay: 0.5 });

  // Confession Animation
  gsap.from("#confession h2", { opacity: 0, y: -50, duration: 1 });
  gsap.from("#confession .confession-text", { opacity: 0, y: 30, duration: 1, delay: 0.5 });

  // Final Message Animation
  gsap.from("#finalMessage h2", { opacity: 0, y: -50, duration: 1 });
  gsap.from("#finalMessage .message", { opacity: 0, y: 30, duration: 1, delay: 0.5 });

  // ScrollMagic for page progression (ensuring it lasts 40 seconds)
  const controller = new ScrollMagic.Controller();

  // Scroll animation for gradual appearance
  new ScrollMagic.Scene({
    triggerElement: "#welcome",
    triggerHook: 0.9,
    duration: "100%"
  })
  .setTween(gsap.fromTo("#welcome", { opacity: 1 }, { opacity: 0 }))
  .addTo(controller);
});
