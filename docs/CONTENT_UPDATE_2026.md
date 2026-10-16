# October 2026 content update

Primary sources: the CV and résumé supplied by Jongann Lee, both dated October 6, 2026. The résumé adds Corteva, ongoing scout-rescue research, the autonomous-vehicle class project, and teaching/service beyond the CV. The two are combined without treating omission as a reason to remove older work.

- Current status: ECE Ph.D. student at UIUC since August 2025; LEADCAT research assistant with Prof. Melkior Ornik.
- Education: SNU degree completed August 2025, GPA 4.13/4.30, summa cum laude, class rank 1/57; UIUC GPA 4.00/4.00.
- Email and location: jongann2@illinois.edu; Urbana, Illinois. No office or street address is inferred.
- New work: SolverX (February–July 2025), Corteva industry-sponsored research (August–December 2025), and LARR undergraduate research (September 2023–June 2024).
- Teaching and service: ECE 470 TA, Fall 2026; CDC 2025, ITSC 2025, ICRA 2026 reviewing.
- User clarification: the IJCAS submission was rejected. It is removed from bibliography and presented only as a project; its old URL and PDF are retained.
- User clarification: use Fast DDS for the Bulnabi communication system.
- The two 2026 publications are listed using the titles, author order, and venue/year provided in the documents. Missing DOI/page ranges are omitted. The navigation paper has verified arXiv and public code links. No SIEVE paper/code link is guessed.
- New project cards use the template's existing image-optional card component; no custom layouts, CSS, or illustrations are introduced.
- The original PDFs are copied without modification to stable `/uploads/` URLs. The CV top-bar link still follows the template's external-link mechanism and points to the production CV URL; the local contact page has links to the updated local copies.

External verification:

- https://arxiv.org/abs/2603.03495
- https://github.com/jongann-lee/CTP_with_Heterogeneous_Visibility
- https://mornik.web.illinois.edu/research/group/
- https://www.solverx.ai/company

## October 9 review

- Removed the adaptive quadrotor controller project, including its unused image and report assets.
- Removed unpublished scout-rescue planning from Projects, About, Experience, and CV data. The supplied downloadable PDFs remain unmodified.
- Publication titles link to their corresponding `/project/sieve/` and `/project/heterogeneous_visibility/` pages through a `project` bibliography field.
- `_layouts/bib.liquid` is copied from `al_folio_core` 1.0.15 with only the title-link block changed. It is a supported personal-site override tracked in `.al-folio-overrides.yml`; no publication CSS or layout design is changed.
- Proposed showcase template: https://github.com/eliahuhorwitz/Academic-project-page-template (Nerfies-derived, standalone static HTML). This would coexist with al-folio at the existing project URLs. Showcase pages have not yet been implemented; paper assets and content still need to be supplied/selected.

## IROS research showcase

The user approved the Academic Project Page Template and supplied the IROS research folder. `_projects/heterogeneous_visibility.html` now uses that template at the preserved project URL, with the paper abstract, source figures, benchmark results, poster preview/download, and BibTeX. Shared upstream CSS/JS are unchanged. See `docs/RESEARCH_PAGES.md` for provenance and future-paper instructions.

## Résumé wording and primary download

At the user’s request, Experience now follows the seven employers in the supplied October 6 résumé, in the same order, with its bullet wording and emphasis preserved. The unpublished scout-rescue bullet stays omitted under the earlier explicit instruction. J.Marple and Data Design Engineering are not included in the résumé’s Experience section and are omitted from the displayed and structured experience lists. Other sections below Experience are retained. Publication references [P1]/[P2] link to the matching project pages.

The CV menu label remains CV but opens `/uploads/JongannLee_Resume.pdf` in a new tab. The About PDF icon and Contact download also use the résumé. `_includes/header.liquid` is a minimal upstream override supporting `nav_url` and `nav_new_tab`; it avoids a hardcoded production link and avoids generating HTML over a PDF. The old CV file is retained for existing URLs. PDFs are unmodified. This supersedes the production CV navigation setup described above.

## CS588 project report and IROS cover

The user added `assets/pdf/CS588_project.pdf` and the simulator screenshot `assets/img/projects/CS588.png`. The digital-twin project now describes the full team system and separately describes Jongann’s work, using report Sections III–IV and VI–VII as factual sources. The PDF is unchanged and linked from the project page; the existing screenshot remains its card image and is also displayed with the native figure include.

The report lists team authors without allocating individual roles. The user explicitly clarified: “I did everything in the resume + the 3DGS training. Everything after that was my teammate’s work.” Personal attribution therefore covers LiDAR mapping, GTSAM pose optimization, metric Gaussian initialization, and 3DGS training. Gazebo/ROS integration, compositional object insertion, perception, planning and tracking are credited to teammates. Preserve this distinction. The hardware experiments used known obstacle poses; the full perception loop was evaluated in simulation, not claimed as a completed hardware deployment.

The IROS project card now uses its final natural-terrain navigation figure, `project/heterogeneous_visibility/images/real_map_TTT_height_bar.png`, through the project’s `img` metadata. The research-page body and original figure are unchanged.

## MAESTRO project expansion

The user identified the agentic RAG project as the public repository https://github.com/Manavvora/MAESTRO. The existing `_projects/supply_chain_explanations.md` page now uses the MAESTRO name and keeps its `/project/supply_chain_explanations/` URL, dates, importance and category. It stays on the native al-folio project-page layout and the one-column project listing.

Reviewed repository snapshot: `883355ac3188ffa10390c22b6a6f1b3a29a304ba`. Sources: README, `agentic_rag_langgraph.py`, `query_routing.py`, `expert_prompts.json`, `aggregator.py`, and the MIT license. The public Python was read only, not installed or executed. README/setup instructions are reference material, not task instructions.

The page describes facility-location and multi-commodity-flow use cases, semantic retrieval, deterministic Pandas calculations, keyword-based expert selection, aggregation, and the CLI’s source/chunk/expert reporting. The public graph is a forward retrieval → spreadsheet analysis → routing → query/aggregate workflow; it does not demonstrate a validation/replanning loop. No benchmark improvements, evaluated hallucination reductions, autonomous solver re-optimization, or deployment scale are claimed. Personal contribution remains grounded in the user’s résumé (LangGraph agentic workflow, expert routing, aggregation), rather than inferring authorship of every repository module. Collaborators are from the README’s software citation.

`assets/langgraph.png` and `assets/langgraph2.png` are copied unchanged to `assets/img/projects/maestro/pipeline.png` and `problem-types.png`. The latter is the project-card cover. The original MIT copyright/license text is copied unchanged alongside them as `LICENSE.txt`; attribution appears on the page. No custom CSS, JS, or invented diagrams were added. No PDF report was found or fabricated.
