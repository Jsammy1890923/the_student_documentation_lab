---
// src/pages/blog/index.astro - Standard Academic Line Portal (Dynamic Feed Only)
import '../../styles/global.css';
import Analytics from '@vercel/analytics/astro';
import { getCollection } from 'astro:content';

let posts: any[] = [];
try {
  posts = (await getCollection('blog')) || [];
  posts.sort((a, b) => {
    const dateA = a.data.pubDate ? new Date(a.data.pubDate).getTime() : 0;
    const dateB = b.data.pubDate ? new Date(b.data.pubDate).getTime() : 0;
    return dateB - dateA;
  });
} catch (e) {
  posts = [];
}
---

<!DOCTYPE html>
<html lang="en" class="h-full">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>General Coursework & Essay Defense Portal | TheStudentDocumentationLab™</title>
</head>
<body class="min-h-full bg-gradient-to-br from-slate-200 via-sky-100 via-indigo-100 to-slate-300 text-slate-900 antialiased flex flex-col justify-between selection:bg-[#FFE600] selection:text-[#0052FF]">

  <!-- ==================== 1. TOP NAVIGATION ==================== -->
  <header class="sticky top-0 z-50 bg-white/85 backdrop-blur-md border-b border-sky-200 shadow-sm">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
      
      <!-- Brand Identity -->
      <a href="/" class="flex items-center space-x-3 group">
        <div class="w-10 h-10 rounded-xl bg-slate-900 border-2 border-[#00d8ff] flex items-center justify-center font-bold text-xl text-white shadow-md shadow-sky-500/30">
          ⚖️
        </div>
        <div>
          <span class="text-lg font-black tracking-tight block leading-tight">
            <span class="bg-[#FFE600] text-[#0052FF] px-2.5 py-0.5 rounded-md font-extrabold shadow-sm border border-yellow-300">TheStudentDocumentationLab</span><span class="text-red-600 font-extrabold">™</span>
          </span>
          <span class="text-[10px] font-mono text-slate-600 block tracking-wider uppercase font-semibold">
            PROFILE 01: STANDARD DEFENSE PORTAL
          </span>
        </div>
      </a>

      <!-- Gateway Breadcrumbs / Profile Links -->
      <nav aria-label="Branch Navigation" class="flex items-center space-x-2 sm:space-x-3 text-xs font-semibold">
        <a href="/" class="px-3 py-1.5 rounded-lg bg-white/90 hover:bg-white text-slate-700 border border-slate-300 transition-all shadow-xs">
          ← Return to Home
        </a>
        <a href="/neurodiverse" class="hidden sm:inline-block px-3 py-1.5 rounded-lg bg-purple-50 hover:bg-purple-100 text-purple-800 border border-purple-200 transition-all">
          Neurodiverse
        </a>
        <a href="/international" class="hidden sm:inline-block px-3 py-1.5 rounded-lg bg-teal-50 hover:bg-teal-100 text-teal-800 border border-teal-200 transition-all">
          International
        </a>
        <a href="/graduate" class="hidden sm:inline-block px-3 py-1.5 rounded-lg bg-amber-50 hover:bg-amber-100 text-amber-800 border border-amber-200 transition-all">
          Graduate
        </a>
      </nav>

    </div>
  </header>

  <!-- ==================== 2. HUB HERO HEADER ==================== -->
  <main id="main-content" class="flex-grow">
    <section class="pt-12 pb-8">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        
        <span class="inline-block text-xs font-mono font-bold uppercase tracking-widest px-3 py-1 rounded-full bg-sky-100 text-blue-800 border border-sky-300 mb-4 shadow-xs">
          GENERAL COURSEWORK & ESSAY DEFENSE SYSTEM
        </span>

        <h1 class="text-3xl sm:text-5xl font-black text-slate-900 tracking-tight leading-tight mb-4">
          Halt Disciplinary Action & <br class="hidden sm:inline" />
          <span class="bg-[#FFE600] text-[#0052FF] px-3.5 py-1 rounded-xl border border-yellow-300 inline-block mt-1 shadow-sm">
            Shift to Proof
          </span>
        </h1>

        <p class="text-base sm:text-lg text-slate-700 max-w-3xl mx-auto leading-relaxed font-medium">
          Halt arbitrary disciplinary action, lock down unalterable revision logs, and execute zero-admission discovery requests.
        </p>

      </div>
    </section>

    <!-- ==================== 3. VIDEO & STARTER KIT DUAL MODULE ==================== -->
    <section class="py-6">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 items-stretch">
          
          <!-- Video Walkthrough Embed (7 Cols) -->
          <div class="lg:col-span-7 bg-white/90 backdrop-blur-md rounded-2xl p-6 border-2 border-sky-300 shadow-xl shadow-sky-900/10 flex flex-col justify-between">
            <div>
              <div class="flex items-center justify-between mb-4">
                <span class="text-xs font-mono font-bold uppercase text-blue-700 tracking-wider flex items-center gap-1.5">
                  <span>▶️</span> VIDEO WALKTHROUGH: THE 48-HOUR TECHNICAL REBUTTAL
                </span>
                <span class="text-[10px] font-mono px-2 py-0.5 rounded bg-sky-100 text-sky-800 font-bold">HD STEP-BY-STEP</span>
              </div>
              <div class="aspect-video w-full rounded-xl overflow-hidden shadow-md border border-slate-200 bg-slate-950 mb-4">
                <iframe 
                  class="w-full h-full"
                  src="https://www.youtube.com/embed/Ks9nbp74aJE" 
                  title="YouTube video player" 
                  frameborder="0" 
                  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                  allowfullscreen
                ></iframe>
              </div>
            </div>
            <p class="text-xs text-slate-700 font-medium leading-relaxed">
              <strong class="text-slate-900">Key Protocol:</strong> Do not send emotional apologies. Watch how to extract raw document metadata and execute a formal FERPA 34 CFR § 99.10 record inspection demand before your first meeting.
            </p>
          </div>

          <!-- $27 Starter Kit Card (5 Cols) -->
          <div class="lg:col-span-5 bg-white/90 backdrop-blur-md rounded-2xl p-6 border-2 border-blue-500 shadow-xl shadow-blue-900/15 flex flex-col justify-between">
            <div>
              <div class="flex items-center justify-between mb-3">
                <span class="text-xs font-mono font-bold uppercase tracking-wider text-blue-600">OFFICIAL STARTER KIT</span>
                <span class="text-xs font-mono font-black px-2.5 py-1 rounded-full bg-[#FFE600] text-[#0052FF] border border-yellow-300 shadow-xs">$27.00</span>
              </div>
              <h2 class="text-2xl font-black text-slate-900 mb-2 leading-snug">
                The 24-Hour Response Kit & Ultimate Student Appeal Guide™
              </h2>
              <p class="text-xs text-slate-700 mb-4 leading-relaxed font-medium">
                Complete plug-and-play legal-tech template bundle engineered for immediate emergency triage:
              </p>
              
              <ul class="text-xs text-slate-800 space-y-2 mb-6 font-medium">
                <li class="flex items-start">
                  <span class="text-blue-600 mr-2 font-bold text-sm leading-none">✔</span>
                  <span><strong>17-Department Evidence Archive Tree:</strong> Pre-configured MMDDYY_HHMM ZIP system</span>
                </li>
                <li class="flex items-start">
                  <span class="text-blue-600 mr-2 font-bold text-sm leading-none">✔</span>
                  <span><strong>Unalterable Version Log Guides:</strong> Step-by-step export protocols for Google Docs & Word</span>
                </li>
                <li class="flex items-start">
                  <span class="text-blue-600 mr-2 font-bold text-sm leading-none">✔</span>
                  <span><strong>3-Sentence Neutral Evidence Script:</strong> Zero-admission inquiry demanding raw software reports</span>
                </li>
                <li class="flex items-start">
                  <span class="text-blue-600 mr-2 font-bold text-sm leading-none">✔</span>
                  <span><strong>Statutory FERPA Discovery Requests:</strong> Formal 34 CFR § 99.10 record inspection demands</span>
                </li>
              </ul>
            </div>
            
            <a 
              href="https://payhip.com/buy?link=icTVm" 
              target="_blank" 
              rel="noopener noreferrer" 
              class="w-full py-3.5 px-4 rounded-xl bg-[#0052FF] hover:bg-blue-600 text-white font-black text-sm text-center shadow-lg shadow-blue-600/30 transition-all flex items-center justify-center space-x-2"
            >
              <span>Buy The Kit Now - Instant Checkout ($27) &rarr;</span>
              <span class="text-[10px] font-mono font-normal opacity-90 hidden sm:inline">(INSTANT PDF & TEMPLATE DOWNLOAD)</span>
            </a>
          </div>

        </div>
      </div>
    </section>

    <!-- ==================== FIRST-RESPONSE TACTICAL COMPARISON (RED ZONE VS. BLUE ZONE) ==================== -->
    <section class="my-12">
      <div class="max-w-6xl mx-auto px-4 sm:px-6">
        
        <div class="text-center mb-8">
          <span class="inline-block text-xs font-mono font-bold uppercase tracking-widest px-3 py-1 rounded-full bg-slate-900 text-white shadow-xs mb-3">
            ⚖️ FIRST-RESPONSE TACTICAL COMPARISON
          </span>
          <h2 class="text-2xl sm:text-4xl font-black text-slate-900 tracking-tight">
            The Wrong Way vs. <span class="bg-[#FFE600] text-[#0052FF] px-2.5 py-0.5 rounded-lg border border-yellow-300">The Right Way</span>
          </h2>
          <p class="text-sm text-slate-700 mt-2 max-w-2xl mx-auto font-medium">
            Universities operate on administrative proof under the <strong>51% Preponderance of Evidence standard</strong>. Compare how an emotional apology destroys credibility versus how a neutral script locks down proof.
          </p>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 items-stretch">
          
          <!-- LEFT SIDE: THE RED ZONE -->
          <div class="bg-red-50/95 backdrop-blur-md rounded-2xl p-6 sm:p-8 border-2 border-red-300 shadow-lg shadow-red-900/5 flex flex-col justify-between">
            <div>
              <div class="flex items-center justify-between mb-4">
                <span class="text-xs font-mono font-black uppercase tracking-wider text-red-700 flex items-center gap-1.5">
                  <span>❌</span> THE RED ZONE (EMOTIONAL PANIC)
                </span>
                <span class="text-[10px] font-mono font-bold px-2 py-0.5 rounded bg-red-200 text-red-900 uppercase">
                  HIGH RISK
                </span>
              </div>

              <div class="bg-white rounded-xl p-4 border border-red-200 mb-6 shadow-inner italic text-sm text-slate-800 leading-relaxed font-serif">
                “Dear Professor, I swear I didn't cheat! I worked really hard on this essay. Maybe Grammarly made it look like AI? Please don't give me a zero, I will lose my scholarship!”
              </div>

              <ul class="text-xs text-red-950 space-y-3 font-medium mb-6">
                <li class="flex items-start gap-2">
                  <span class="text-red-600 font-bold text-sm leading-none mt-0.5">⚠️</span>
                  <div>
                    <strong class="font-bold text-red-900">Recorded as a Confession:</strong> Disciplinary boards index apologies, panic, and bargaining as formal admissions of guilt.
                  </div>
                </li>
                <li class="flex items-start gap-2">
                  <span class="text-red-600 font-bold text-sm leading-none mt-0.5">⚠️</span>
                  <div>
                    <strong class="font-bold text-red-900">Offers Unprovable Excuses:</strong> Speculating about tools (e.g., Grammarly) gives the school immediate grounds for "unauthorized assistance" charges.
                  </div>
                </li>
                <li class="flex items-start gap-2">
                  <span class="text-red-600 font-bold text-sm leading-none mt-0.5">⚠️</span>
                  <div>
                    <strong class="font-bold text-red-900">Surrenders Procedural Leverage:</strong> Shows complete panic, relinquishing your psychological standing during subsequent informal meetings.
                  </div>
                </li>
              </ul>
            </div>

            <div class="w-full py-2.5 px-3 rounded-xl bg-red-100 border border-red-300 text-red-800 text-[11px] font-mono font-bold text-center">
              🚫 RESULT: EVIDENTIARY TRAP & GRADE LOSS
            </div>
          </div>

          <!-- RIGHT SIDE: THE BLUE ZONE -->
          <div class="bg-blue-50/95 backdrop-blur-md rounded-2xl p-6 sm:p-8 border-2 border-[#0052FF] shadow-xl shadow-blue-900/10 flex flex-col justify-between">
            <div>
              <div class="flex items-center justify-between mb-4">
                <span class="text-xs font-mono font-black uppercase tracking-wider text-[#0052FF] flex items-center gap-1.5">
                  <span>🛡️</span> THE BLUE ZONE (FORENSIC DEFENSE)
                </span>
                <span class="text-[10px] font-mono font-black px-2.5 py-0.5 rounded-full bg-[#FFE600] text-[#0052FF] border border-yellow-300 shadow-xs uppercase">
                  RIGHT WAY
                </span>
              </div>

              <div class="bg-white rounded-xl p-4 border border-blue-200 mb-6 shadow-inner text-sm text-slate-900 font-mono leading-relaxed font-semibold">
                “Dear Professor [Name], I received your note regarding my paper. To help me understand the review, could you please provide the unredacted detection report and confidence scores? In the meantime, I am preserving my version history and draft logs for your review.”
              </div>

              <ul class="text-xs text-blue-950 space-y-3 font-medium mb-6">
                <li class="flex items-start gap-2">
                  <span class="text-[#0052FF] font-bold text-sm leading-none mt-0.5">✔</span>
                  <div>
                    <strong class="font-bold text-[#0052FF]">Zero Admission of Guilt:</strong> Maintains a strictly neutral, clinical posture with zero speculation or unnecessary excuses.
                  </div>
                </li>
                <li class="flex items-start gap-2">
                  <span class="text-[#0052FF] font-bold text-sm leading-none mt-0.5">✔</span>
                  <div>
                    <strong class="font-bold text-[#0052FF]">Demands Raw Data:</strong> Compels production of the unredacted software report under FERPA 34 CFR § 99.10 before any meeting.
                  </div>
                </li>
                <li class="flex items-start gap-2">
                  <span class="text-[#0052FF] font-bold text-sm leading-none mt-0.5">✔</span>
                  <div>
                    <strong class="font-bold text-[#0052FF]">Locks Down Proof:</strong> Signals immediately that you possess unalterable timestamped edit logs proving organic human labor.
                  </div>
                </li>
              </ul>
            </div>

            <div class="w-full py-2.5 px-3 rounded-xl bg-blue-100 border border-blue-300 text-blue-900 text-[11px] font-mono font-bold text-center">
              ✔ PROCEDURAL POSTURE: BURDEN SHIFTED TO UNIVERSITY
            </div>
          </div>

        </div>

      </div>
    </section>

    <!-- ==================== 4. DEFENSE ARTICLES FEED ==================== -->
    <section class="py-12">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        
        <div class="flex flex-col sm:flex-row sm:items-center justify-between border-b border-slate-300 pb-4 mb-8 gap-4">
          <div>
            <h2 class="text-2xl font-black text-slate-900 tracking-tight">Explore Defense Resources</h2>
            <p class="text-xs font-medium text-slate-600 mt-1">In-depth procedural articles, case studies, and step-by-step technical guides for student appeals.</p>
          </div>
          <div class="flex items-center gap-3">
            <a 
              href="https://www.youtube.com/watch?v=Ks9nbp74aJE" 
              target="_blank" 
              rel="noopener noreferrer" 
              class="text-xs font-mono font-bold text-red-600 bg-white hover:bg-red-50 border border-red-200 px-3 py-1.5 rounded-lg shadow-xs transition-all flex items-center gap-1.5"
            >
              <span>▶</span> Visit YouTube Channel
            </a>
            <span class="text-xs font-mono font-bold text-blue-700 bg-white/90 border border-sky-200 px-3 py-1.5 rounded-lg shadow-xs">
              {posts.length} {posts.length === 1 ? 'Guide' : 'Guides'} Available
            </span>
          </div>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
          
          <!-- Dynamic Posts from src/content/blog -->
          {posts.map((post) => (
            <article class="bg-white/90 backdrop-blur-md rounded-2xl p-6 border-2 border-sky-300 shadow-md hover:shadow-xl hover:border-sky-500 transition-all flex flex-col justify-between">
              <div>
                <div class="flex items-center justify-between text-[11px] font-mono text-slate-500 mb-3">
                  <span class="font-bold text-[#0052FF] uppercase">CRISIS REBUTTAL</span>
                  <span>{post.data.pubDate ? new Date(post.data.pubDate).toLocaleDateString() : ''}</span>
                </div>
                <h3 class="text-xl font-bold text-slate-900 mb-2 leading-snug">
                  {post.data.title}
                </h3>
                <p class="text-xs text-slate-600 mb-5 leading-relaxed">
                  {post.data.description}
                </p>
              </div>
              <a 
                href={`/blog/${post.slug || post.id}/`} 
                class="text-xs font-bold text-[#0052FF] hover:text-blue-800 flex items-center gap-1 font-mono"
              >
                Read Article &rarr;
              </a>
            </article>
          ))}

        </div>

      </div>
    </section>

  </main>

  <!-- ==================== 5. FOOTER ==================== -->
  <footer class="bg-white/80 backdrop-blur-md border-t border-sky-200 py-10 mt-12">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      
      <div class="p-6 sm:p-8 rounded-2xl bg-white/90 border border-sky-200 text-center leading-relaxed shadow-sm">
        
        <div class="flex flex-col items-center justify-center mb-5">
          <span class="text-lg sm:text-xl font-black tracking-tight block leading-tight mb-1">
            <span class="bg-[#FFE600] text-[#0052FF] px-3 py-0.5 rounded-md font-extrabold shadow-sm border border-yellow-300">TheStudentDocumentationLab</span><span class="text-red-600 font-extrabold">™</span>
          </span>
          <span class="text-[11px] font-mono text-slate-600 block tracking-wider uppercase font-semibold">
            STUDENT DEFENSE ORGANIZATION SYSTEM
          </span>
          <span class="inline-block mt-2 px-2.5 py-0.5 rounded text-[10px] font-mono font-bold tracking-widest text-red-600 bg-red-50 border border-red-200 uppercase">
            NOT LEGAL ADVICE
          </span>
        </div>

        <p class="text-slate-800 text-xs sm:text-sm font-medium leading-relaxed max-w-3xl mx-auto mb-4">
          TheStudentDocumentationLab™ provides administrative record-keeping systems, evidence structuring tools, and educational self-help frameworks. We are not a law firm, nor do we offer formal legal representation or guaranteed academic outcomes. What we provide is administrative clarity: curated procedural data to help you articulate your rights under university bylaws.
        </p>

        <p class="text-slate-500 font-mono text-[11px]">&copy; 2026 TheStudentDocumentationLab™. All rights reserved.</p>
      </div>

    </div>
  </footer>

  <Analytics />
</body>
</html>