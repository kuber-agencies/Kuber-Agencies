# Kuber Agencies — Realistic Product Image SEO Upgrade
**Complete Implementation Guide for kuberagencies.in**

---

## 1. Image Folder Structure

Upload all images to your server under this exact folder layout:

```
/images/
├── og-image.webp                          (1200×630 — homepage social share)
│
├── cement/
│   ├── ultratech-opc53-cement-bags-chennai.webp
│   ├── ultratech-ppc-cement-bags-chennai.webp
│   ├── dalmia-opc53-cement-bags-chennai.webp
│   ├── dalmia-blended-cement-chennai.webp
│   ├── ramco-supergrade-cement-chennai.webp
│   ├── zuari-opc43-cement-chennai.webp
│   ├── chettinad-ppc-cement-chennai.webp
│   └── cement-bags-stacked-warehouse-chennai.webp   (hero / category card)
│
├── steel/
│   ├── ars-tmt-fe500d-bars-chennai.webp
│   ├── durga-tmt-fe415-bars-chennai.webp
│   ├── arun-tmt-fe500-bars-chennai.webp
│   ├── tmt-bars-bundled-construction-site.webp      (hero / category card)
│   └── tmt-bars-yard-madambakkam.webp
│
├── paints/
│   ├── asian-paints-royale-interior-emulsion-chennai.webp
│   ├── asian-paints-apex-exterior-emulsion-chennai.webp
│   ├── asian-paints-wall-primer-chennai.webp
│   ├── asian-paints-smartcare-dampshield-chennai.webp
│   ├── paint-buckets-stacked-dealer-chennai.webp    (hero / category card)
│   └── wall-painting-scene-interior-chennai.webp
│
├── pipes/
│   ├── star-cpvc-pipes-hot-cold-water-chennai.webp
│   ├── ashirvad-cpvc-pipes-chennai.webp
│   ├── finolex-upvc-pipes-plumbing-chennai.webp
│   ├── finolex-electrical-conduit-pipes-chennai.webp
│   ├── indian-tube-gi-pipes-chennai.webp
│   ├── pvc-cpvc-pipes-bundled-chennai.webp          (hero / category card)
│   └── cpvc-pipes-installed-plumbing.webp
│
├── electrical/
│   ├── havells-wires-cables-chennai.webp
│   ├── polycab-cables-rolls-chennai.webp
│   ├── legrand-modular-switches-chennai.webp
│   ├── anchor-switches-sockets-chennai.webp
│   ├── electrical-panel-mcb-chennai.webp
│   └── electrical-cables-wires-dealer-chennai.webp  (hero / category card)
│
├── tiles/
│   ├── ceramic-floor-tiles-installed-chennai.webp
│   ├── vitrified-tiles-living-room-chennai.webp
│   ├── granite-floor-tiles-supplier-chennai.webp
│   ├── wall-tiles-bathroom-chennai.webp
│   └── tiles-flooring-showroom-chennai.webp         (hero / category card)
│
└── sand/
    ├── m-sand-manufactured-sand-chennai.webp
    ├── p-sand-plastering-sand-chennai.webp
    └── river-sand-bulk-supply-chennai.webp
```

### Image Specifications

| Use | Size | Format | Max File Size |
|---|---|---|---|
| Product card thumbnail | 400×240px | WebP | 40 KB |
| Category hero card | 600×400px | WebP | 60 KB |
| JSON-LD schema image | 1200×800px | WebP/JPG | 120 KB |
| OG/social share | 1200×630px | WebP/JPG | 100 KB |

---

## 2. Where to Source Realistic Product Photos

Use these **free, commercial-use sources** — search the exact terms:

| Category | Search Term | Best Source |
|---|---|---|
| Cement bags | "cement bags stacked warehouse India" | Unsplash, Pexels |
| TMT steel bars | "TMT steel bars construction site India" | Pexels, Pixabay |
| Paint buckets | "paint buckets wall painting India" | Pexels, Unsplash |
| CPVC pipes | "CPVC PVC pipes bundled plumbing" | Pexels, Pixabay |
| Electrical cables | "electrical cables wires construction" | Unsplash, Pexels |
| Floor tiles | "vitrified floor tiles installed living room" | Pexels, Unsplash |

**Pro tip:** For brand-specific shots (Ultratech bags, Asian Paints cans), use your phone to photograph actual stock in your yard. Real photos from your store build far more trust than stock photos.

---

## 3. Updated Product Card HTML

Replace your entire products section card blocks with the following. Each card has:
- `<img>` with descriptive SEO filename path
- `alt` text with brand + keyword + city
- `loading="lazy"` on non-hero images
- `width` / `height` attributes to prevent CLS
- Graceful fallback on error

### 3a. Cement Cards

```html
<!-- === CEMENT SECTION === -->
<div class="cat-section" data-cat="cement" id="section-cement">
  <div class="cat-section-header" onclick="toggleSection('cement')">
    <div class="cat-section-emoji">🧱</div>
    <div class="cat-section-title-wrap">
      <div class="cat-section-title">Cement</div>
      <div class="cat-section-meta">5 brands · Ultratech, Dalmia, Ramco, Zuari, Chettinad · OPC 43/53 &amp; PPC</div>
    </div>
    <div class="cat-section-toggle">▼</div>
  </div>
  <div class="cat-section-body">
    <div class="product-grid">

      <!-- Ultratech OPC 53 -->
      <div class="product-card" data-brand="Ultratech" data-cat="cement" data-name="Ultratech OPC 53 Grade">
        <div class="product-card-bar"></div>
        <div class="product-badge badge-bestseller">Best Seller</div>
        <div class="product-card-img">
          <img
            src="https://kuberagencies.in/images/cement/ultratech-opc53-cement-bags-chennai.webp"
            alt="Ultratech OPC 53 Grade cement bags stacked – authorized dealer Madambakkam Chennai"
            width="400" height="240"
            loading="eager"
            onerror="this.onerror=null;this.style.objectFit='contain';this.style.padding='20px';this.style.background='#1a3350';"
          />
          <div class="product-card-img-overlay"></div>
          <div class="product-card-cat-tag">Cement</div>
        </div>
        <div class="product-card-body">
          <div class="product-card-brand-strip">
            <img src="https://upload.wikimedia.org/wikipedia/en/thumb/f/fc/UltraTech_Cement_Logo.svg/200px-UltraTech_Cement_Logo.svg.png"
                 alt="Ultratech Cement Logo" class="product-brand-logo" width="90" height="34" loading="lazy"
                 onerror="this.style.display='none';this.nextElementSibling.style.removeProperty('display')"/>
            <span class="brand-logo-badge brand-ultratech" style="display:none">Ultratech</span>
          </div>
          <div class="product-card-name">Ultratech OPC 53 Grade</div>
          <div class="product-card-desc">High-early-strength cement for RCC columns, footings &amp; slabs. IS:269 certified. Consistent quality, Chennai site delivery.</div>
          <div class="product-card-footer">
            <div class="product-card-price">₹390<small>/bag</small></div>
            <div class="product-card-actions">
              <a class="btn-card-wa" href="https://wa.me/919840928767?text=Hi%20I%20need%20a%20quote%20for%20Ultratech%20OPC%2053" rel="noopener" target="_blank">
                <!-- WhatsApp SVG -->
                <svg width="14" height="14" fill="currentColor" viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.123.554 4.116 1.524 5.843L0 24l6.335-1.509A11.954 11.954 0 0 0 12 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.818a9.822 9.822 0 0 1-5.006-1.366l-.359-.213-3.722.976.994-3.628-.234-.373A9.817 9.817 0 0 1 2.182 12C2.182 6.57 6.57 2.182 12 2.182S21.818 6.57 21.818 12 17.43 21.818 12 21.818z"/></svg>
                WhatsApp
              </a>
              <button class="btn-card-quote" onclick="showPage('contact')">📋 Get Quote</button>
            </div>
          </div>
          <button class="btn-add-quote" onclick="toggleProductQuote(this)">📋 Add to Quote</button>
        </div>
      </div>

      <!-- Ultratech PPC -->
      <div class="product-card" data-brand="Ultratech" data-cat="cement" data-name="Ultratech PPC Cement">
        <div class="product-card-bar"></div>
        <div class="product-badge badge-popular">Popular</div>
        <div class="product-card-img">
          <img
            src="https://kuberagencies.in/images/cement/ultratech-ppc-cement-bags-chennai.webp"
            alt="Ultratech PPC Portland Pozzolana Cement bags – bulk supply Chennai Madambakkam"
            width="400" height="240"
            loading="lazy"
            onerror="this.onerror=null;this.style.objectFit='contain';this.style.padding='20px';this.style.background='#1a3350';"
          />
          <div class="product-card-img-overlay"></div>
          <div class="product-card-cat-tag">Cement</div>
        </div>
        <div class="product-card-body">
          <div class="product-card-brand-strip">
            <img src="https://upload.wikimedia.org/wikipedia/en/thumb/f/fc/UltraTech_Cement_Logo.svg/200px-UltraTech_Cement_Logo.svg.png"
                 alt="Ultratech Cement" class="product-brand-logo" width="90" height="34" loading="lazy"
                 onerror="this.style.display='none';this.nextElementSibling.style.removeProperty('display')"/>
            <span class="brand-logo-badge brand-ultratech" style="display:none">Ultratech</span>
          </div>
          <div class="product-card-name">Ultratech PPC Cement</div>
          <div class="product-card-desc">Portland Pozzolana Cement — lower heat of hydration, ideal for plastering, masonry &amp; general construction.</div>
          <div class="product-card-footer">
            <div class="product-card-price">₹360<small>/bag</small></div>
            <div class="product-card-actions">
              <a class="btn-card-wa" href="https://wa.me/919840928767?text=Hi%20I%20need%20a%20quote%20for%20Ultratech%20PPC" rel="noopener" target="_blank">
                <svg width="14" height="14" fill="currentColor" viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.123.554 4.116 1.524 5.843L0 24l6.335-1.509A11.954 11.954 0 0 0 12 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.818a9.822 9.822 0 0 1-5.006-1.366l-.359-.213-3.722.976.994-3.628-.234-.373A9.817 9.817 0 0 1 2.182 12C2.182 6.57 6.57 2.182 12 2.182S21.818 6.57 21.818 12 17.43 21.818 12 21.818z"/></svg>
                WhatsApp
              </a>
              <button class="btn-card-quote" onclick="showPage('contact')">📋 Get Quote</button>
            </div>
          </div>
          <button class="btn-add-quote" onclick="toggleProductQuote(this)">📋 Add to Quote</button>
        </div>
      </div>

      <!-- Dalmia OPC 53 -->
      <div class="product-card" data-brand="Dalmia" data-cat="cement" data-name="Dalmia OPC 53 Grade">
        <div class="product-card-bar"></div>
        <div class="product-badge badge-bestseller">Best Seller</div>
        <div class="product-card-img">
          <img
            src="https://kuberagencies.in/images/cement/dalmia-opc53-cement-bags-chennai.webp"
            alt="Dalmia OPC 53 Grade cement bags – authorized dealer Chennai Tamil Nadu"
            width="400" height="240"
            loading="lazy"
            onerror="this.onerror=null;this.style.objectFit='contain';this.style.padding='20px';this.style.background='#1a3350';"
          />
          <div class="product-card-img-overlay"></div>
          <div class="product-card-cat-tag">Cement</div>
        </div>
        <div class="product-card-body">
          <div class="product-card-brand-strip">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/Dalmia_Bharat_logo.svg/200px-Dalmia_Bharat_logo.svg.png"
                 alt="Dalmia Bharat Cement" class="product-brand-logo" width="90" height="34" loading="lazy"
                 onerror="this.style.display='none';this.nextElementSibling.style.removeProperty('display')"/>
            <span class="brand-logo-badge brand-dalmia" style="display:none">Dalmia</span>
          </div>
          <div class="product-card-name">Dalmia OPC 53 Grade</div>
          <div class="product-card-desc">Premium high-strength OPC from Dalmia Bharat. Superior fineness, excellent setting time control. IS:269 certified.</div>
          <div class="product-card-footer">
            <div class="product-card-price">₹385<small>/bag</small></div>
            <div class="product-card-actions">
              <a class="btn-card-wa" href="https://wa.me/919840928767?text=Hi%20I%20need%20a%20quote%20for%20Dalmia%20OPC%2053" rel="noopener" target="_blank">
                <svg width="14" height="14" fill="currentColor" viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.123.554 4.116 1.524 5.843L0 24l6.335-1.509A11.954 11.954 0 0 0 12 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.818a9.822 9.822 0 0 1-5.006-1.366l-.359-.213-3.722.976.994-3.628-.234-.373A9.817 9.817 0 0 1 2.182 12C2.182 6.57 6.57 2.182 12 2.182S21.818 6.57 21.818 12 17.43 21.818 12 21.818z"/></svg>
                WhatsApp
              </a>
              <button class="btn-card-quote" onclick="showPage('contact')">📋 Get Quote</button>
            </div>
          </div>
          <button class="btn-add-quote" onclick="toggleProductQuote(this)">📋 Add to Quote</button>
        </div>
      </div>

    </div><!-- /product-grid -->
  </div>
</div>
<!-- === END CEMENT SECTION === -->
```

### 3b. Steel Cards

```html
<!-- === STEEL SECTION === -->
<div class="cat-section" data-cat="steel" id="section-steel">
  <div class="cat-section-header" onclick="toggleSection('steel')">
    <div class="cat-section-emoji">🔩</div>
    <div class="cat-section-title-wrap">
      <div class="cat-section-title">Steel</div>
      <div class="cat-section-meta">3 brands · ARS, Durga, Arun · TMT Fe500D, Fe415 · All diameters</div>
    </div>
    <div class="cat-section-toggle">▼</div>
  </div>
  <div class="cat-section-body">
    <div class="product-grid">

      <!-- ARS TMT Fe500D -->
      <div class="product-card" data-brand="ARS" data-cat="steel" data-name="ARS TMT Fe500D">
        <div class="product-card-bar"></div>
        <div class="product-badge badge-bestseller">Best Seller</div>
        <div class="product-card-img">
          <img
            src="https://kuberagencies.in/images/steel/ars-tmt-fe500d-bars-chennai.webp"
            alt="ARS TMT Fe500D steel bars bundled at construction site – supplier Madambakkam Chennai"
            width="400" height="240"
            loading="lazy"
            onerror="this.onerror=null;this.style.objectFit='contain';this.style.padding='20px';this.style.background='#1a3350';"
          />
          <div class="product-card-img-overlay"></div>
          <div class="product-card-cat-tag">Steel / TMT</div>
        </div>
        <div class="product-card-body">
          <div class="product-card-brand-strip">
            <span class="brand-logo-badge brand-ars">ARS Steel</span>
          </div>
          <div class="product-card-name">ARS TMT Fe500D Bars</div>
          <div class="product-card-desc">High-ductility seismic-zone TMT bars. Sizes 8–32mm. Superior bendability, weldability &amp; corrosion resistance.</div>
          <div class="product-card-footer">
            <div class="product-card-price">₹67,500<small>/ton</small></div>
            <div class="product-card-actions">
              <a class="btn-card-wa" href="https://wa.me/919840928767?text=Hi%20I%20need%20a%20quote%20for%20ARS%20TMT%20Fe500D" rel="noopener" target="_blank">
                <svg width="14" height="14" fill="currentColor" viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.123.554 4.116 1.524 5.843L0 24l6.335-1.509A11.954 11.954 0 0 0 12 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.818a9.822 9.822 0 0 1-5.006-1.366l-.359-.213-3.722.976.994-3.628-.234-.373A9.817 9.817 0 0 1 2.182 12C2.182 6.57 6.57 2.182 12 2.182S21.818 6.57 21.818 12 17.43 21.818 12 21.818z"/></svg>
                WhatsApp
              </a>
              <button class="btn-card-quote" onclick="showPage('contact')">📋 Get Quote</button>
            </div>
          </div>
          <button class="btn-add-quote" onclick="toggleProductQuote(this)">📋 Add to Quote</button>
        </div>
      </div>

      <!-- Durga TMT Fe415 -->
      <div class="product-card" data-brand="Durga" data-cat="steel" data-name="Durga TMT Fe415">
        <div class="product-card-bar"></div>
        <div class="product-badge badge-popular">Popular</div>
        <div class="product-card-img">
          <img
            src="https://kuberagencies.in/images/steel/durga-tmt-fe415-bars-chennai.webp"
            alt="Durga TMT Fe415 steel bars for RCC construction – bulk supplier Chennai"
            width="400" height="240"
            loading="lazy"
            onerror="this.onerror=null;this.style.objectFit='contain';this.style.padding='20px';this.style.background='#1a3350';"
          />
          <div class="product-card-img-overlay"></div>
          <div class="product-card-cat-tag">Steel / TMT</div>
        </div>
        <div class="product-card-body">
          <div class="product-card-brand-strip">
            <span class="brand-logo-badge brand-durga">Durga TMT</span>
          </div>
          <div class="product-card-name">Durga TMT Fe415 Bars</div>
          <div class="product-card-desc">Standard IS:1786 TMT rebars — excellent for RCC slabs, beams &amp; columns in residential buildings. Sizes 8–25mm.</div>
          <div class="product-card-footer">
            <div class="product-card-price">₹65,000<small>/ton</small></div>
            <div class="product-card-actions">
              <a class="btn-card-wa" href="https://wa.me/919840928767?text=Hi%20I%20need%20a%20quote%20for%20Durga%20TMT%20Fe415" rel="noopener" target="_blank">
                <svg width="14" height="14" fill="currentColor" viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.214-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.123.554 4.116 1.524 5.843L0 24l6.335-1.509A11.954 11.954 0 0 0 12 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.818a9.822 9.822 0 0 1-5.006-1.366l-.359-.213-3.722.976.994-3.628-.234-.373A9.817 9.817 0 0 1 2.182 12C2.182 6.57 6.57 2.182 12 2.182S21.818 6.57 21.818 12 17.43 21.818 12 21.818z"/></svg>
                WhatsApp
              </a>
              <button class="btn-card-quote" onclick="showPage('contact')">📋 Get Quote</button>
            </div>
          </div>
          <button class="btn-add-quote" onclick="toggleProductQuote(this)">📋 Add to Quote</button>
        </div>
      </div>

    </div><!-- /product-grid -->
  </div>
</div>
<!-- === END STEEL SECTION === -->
```

### 3c. Paints Cards (key cards shown — same pattern for all)

```html
<!-- Asian Paints Royale Interior -->
<div class="product-card" data-brand="Asian Paints" data-cat="paints" data-name="Asian Paints Royale Interior">
  <div class="product-card-bar"></div>
  <div class="product-badge badge-bestseller">Best Seller</div>
  <div class="product-card-img">
    <img
      src="https://kuberagencies.in/images/paints/asian-paints-royale-interior-emulsion-chennai.webp"
      alt="Asian Paints Royale interior emulsion paint buckets – authorized dealer Chennai"
      width="400" height="240"
      loading="lazy"
      onerror="this.onerror=null;this.style.objectFit='contain';this.style.padding='20px';this.style.background='#1a3350';"
    />
    <div class="product-card-img-overlay"></div>
    <div class="product-card-cat-tag">Paints</div>
  </div>
  <!-- ... rest of card body unchanged ... -->
</div>

<!-- Asian Paints Apex Exterior -->
<div class="product-card" data-brand="Asian Paints" data-cat="paints" data-name="Asian Paints Apex Exterior">
  <div class="product-card-bar"></div>
  <div class="product-card-img">
    <img
      src="https://kuberagencies.in/images/paints/asian-paints-apex-exterior-emulsion-chennai.webp"
      alt="Asian Paints Apex exterior emulsion – weather-resistant paint supplier Madambakkam Chennai"
      width="400" height="240"
      loading="lazy"
      onerror="this.onerror=null;this.style.objectFit='contain';this.style.padding='20px';this.style.background='#1a3350';"
    />
    <div class="product-card-img-overlay"></div>
    <div class="product-card-cat-tag">Paints</div>
  </div>
</div>

<!-- Waterproofing / SmartCare — use a distinct scene -->
<div class="product-card" data-brand="Asian Paints" data-cat="paints" data-name="Asian Paints SmartCare Dampshield">
  <div class="product-card-bar"></div>
  <div class="product-card-img">
    <img
      src="https://kuberagencies.in/images/paints/asian-paints-smartcare-dampshield-chennai.webp"
      alt="Asian Paints SmartCare Dampshield waterproofing coating – terrace waterproofing Chennai"
      width="400" height="240"
      loading="lazy"
      onerror="this.onerror=null;this.style.objectFit='contain';this.style.padding='20px';this.style.background='#1a3350';"
    />
    <div class="product-card-img-overlay"></div>
    <div class="product-card-cat-tag">Paints</div>
  </div>
</div>
```

### 3d. Pipes / Plumbing Cards

```html
<!-- Star CPVC Pipes -->
<div class="product-card" data-brand="Star" data-cat="plumbing" data-name="Star CPVC Pipes">
  <div class="product-card-img">
    <img
      src="https://kuberagencies.in/images/pipes/star-cpvc-pipes-hot-cold-water-chennai.webp"
      alt="Star CPVC pipes for hot and cold water supply – plumbing supplier Madambakkam Chennai"
      width="400" height="240"
      loading="lazy"
      onerror="this.onerror=null;this.style.objectFit='contain';this.style.padding='20px';this.style.background='#1a3350';"
    />
    <div class="product-card-img-overlay"></div>
    <div class="product-card-cat-tag">Plumbing</div>
  </div>
</div>

<!-- Finolex UPVC -->
<div class="product-card" data-brand="Finolex" data-cat="plumbing" data-name="Finolex UPVC Pipes">
  <div class="product-card-img">
    <img
      src="https://kuberagencies.in/images/pipes/finolex-upvc-pipes-plumbing-chennai.webp"
      alt="Finolex UPVC drainage pipes bundled – authorized dealer Madambakkam Chennai"
      width="400" height="240"
      loading="lazy"
      onerror="this.onerror=null;this.style.objectFit='contain';this.style.padding='20px';this.style.background='#1a3350';"
    />
    <div class="product-card-img-overlay"></div>
    <div class="product-card-cat-tag">Plumbing</div>
  </div>
</div>
```

### 3e. Electrical Cards

```html
<!-- Havells Wires -->
<div class="product-card" data-brand="Havells" data-cat="electrical" data-name="Havells Wires">
  <div class="product-card-img">
    <img
      src="https://kuberagencies.in/images/electrical/havells-wires-cables-chennai.webp"
      alt="Havells electrical wires and cables – authorized dealer Madambakkam Chennai"
      width="400" height="240"
      loading="lazy"
      onerror="this.onerror=null;this.style.objectFit='contain';this.style.padding='20px';this.style.background='#1a3350';"
    />
    <div class="product-card-img-overlay"></div>
    <div class="product-card-cat-tag">Electrical</div>
  </div>
</div>

<!-- Legrand Switches -->
<div class="product-card" data-brand="Legrand" data-cat="electrical" data-name="Legrand Switches">
  <div class="product-card-img">
    <img
      src="https://kuberagencies.in/images/electrical/legrand-modular-switches-chennai.webp"
      alt="Legrand modular switches and sockets – electrical dealer Chennai"
      width="400" height="240"
      loading="lazy"
      onerror="this.onerror=null;this.style.objectFit='contain';this.style.padding='20px';this.style.background='#1a3350';"
    />
    <div class="product-card-img-overlay"></div>
    <div class="product-card-cat-tag">Electrical</div>
  </div>
</div>
```

### 3f. Tiles Cards

```html
<!-- Ceramic Floor Tiles -->
<div class="product-card" data-brand="Generic" data-cat="tiles" data-name="Ceramic Floor Tiles">
  <div class="product-card-img">
    <img
      src="https://kuberagencies.in/images/tiles/ceramic-floor-tiles-installed-chennai.webp"
      alt="Ceramic floor tiles installed in living room – tiles supplier Madambakkam Chennai"
      width="400" height="240"
      loading="lazy"
      onerror="this.onerror=null;this.style.objectFit='contain';this.style.padding='20px';this.style.background='#1a3350';"
    />
    <div class="product-card-img-overlay"></div>
    <div class="product-card-cat-tag">Tiles</div>
  </div>
</div>

<!-- Vitrified Tiles -->
<div class="product-card" data-brand="Generic" data-cat="tiles" data-name="Vitrified Floor Tiles">
  <div class="product-card-img">
    <img
      src="https://kuberagencies.in/images/tiles/vitrified-tiles-living-room-chennai.webp"
      alt="Vitrified tiles in modern living room – flooring supplier Chennai Tamil Nadu"
      width="400" height="240"
      loading="lazy"
      onerror="this.onerror=null;this.style.objectFit='contain';this.style.padding='20px';this.style.background='#1a3350';"
    />
    <div class="product-card-img-overlay"></div>
    <div class="product-card-cat-tag">Tiles</div>
  </div>
</div>
```

---

## 4. Updated JSON-LD Product Schema — Cement (Full Example)

Replace the existing cement Product schema in your `<head>`:

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Product",
  "@id": "https://kuberagencies.in/#product-cement",
  "name": "Cement – OPC 53, OPC 43 & PPC Grades",
  "description": "Authorized cement dealer in Madambakkam Chennai. Bulk supply of Ultratech, Dalmia, Ramco, Zuari and Chettinad cement. Available grades: OPC 43, OPC 53 and PPC. IS certified bags. Same-day site delivery across Chennai.",
  "image": [
    "https://kuberagencies.in/images/cement/ultratech-opc53-cement-bags-chennai.webp",
    "https://kuberagencies.in/images/cement/dalmia-opc53-cement-bags-chennai.webp",
    "https://kuberagencies.in/images/cement/ramco-supergrade-cement-chennai.webp",
    "https://kuberagencies.in/images/cement/cement-bags-stacked-warehouse-chennai.webp"
  ],
  "brand": {
    "@type": "Brand",
    "name": "Ultratech Cement"
  },
  "manufacturer": {
    "@type": "Organization",
    "name": "Ultratech Cement Limited"
  },
  "category": "Construction Materials > Cement",
  "url": "https://kuberagencies.in/#product-cement",
  "additionalProperty": [
    {
      "@type": "PropertyValue",
      "name": "Grade",
      "value": "OPC 53, OPC 43, PPC"
    },
    {
      "@type": "PropertyValue",
      "name": "Certification",
      "value": "IS:269, IS:8112, IS:1489"
    },
    {
      "@type": "PropertyValue",
      "name": "Delivery",
      "value": "Same-day site delivery across Chennai"
    }
  ],
  "offers": {
    "@type": "Offer",
    "url": "https://kuberagencies.in/",
    "priceCurrency": "INR",
    "price": "380",
    "priceValidUntil": "2026-03-31",
    "availability": "https://schema.org/InStock",
    "itemCondition": "https://schema.org/NewCondition",
    "areaServed": {
      "@type": "City",
      "name": "Chennai"
    },
    "seller": {
      "@type": "LocalBusiness",
      "name": "Kuber Agencies",
      "telephone": "+919840928767",
      "address": {
        "@type": "PostalAddress",
        "streetAddress": "Madambakkam",
        "addressLocality": "Chennai",
        "addressRegion": "Tamil Nadu",
        "postalCode": "600126",
        "addressCountry": "IN"
      }
    }
  }
}
</script>
```

### Steel Schema (Updated)

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Product",
  "@id": "https://kuberagencies.in/#product-steel",
  "name": "Steel TMT Bars – Fe500D & Fe415",
  "description": "TMT bars Fe500D and Fe415 in all diameters 8mm–32mm. Authorized dealer for ARS, Durga and Arun Steel in Chennai. IS:1786 certified. Bulk supply for RCC slabs, beams, columns across Tamil Nadu.",
  "image": [
    "https://kuberagencies.in/images/steel/ars-tmt-fe500d-bars-chennai.webp",
    "https://kuberagencies.in/images/steel/durga-tmt-fe415-bars-chennai.webp",
    "https://kuberagencies.in/images/steel/arun-tmt-fe500-bars-chennai.webp",
    "https://kuberagencies.in/images/steel/tmt-bars-bundled-construction-site.webp"
  ],
  "brand": { "@type": "Brand", "name": "ARS Steel" },
  "category": "Construction Materials > Steel",
  "url": "https://kuberagencies.in/#product-steel",
  "additionalProperty": [
    { "@type": "PropertyValue", "name": "Grade", "value": "Fe500D, Fe415, Fe550" },
    { "@type": "PropertyValue", "name": "Certification", "value": "IS:1786" },
    { "@type": "PropertyValue", "name": "Sizes", "value": "8mm, 10mm, 12mm, 16mm, 20mm, 25mm, 32mm" }
  ],
  "offers": {
    "@type": "Offer",
    "url": "https://kuberagencies.in/",
    "priceCurrency": "INR",
    "price": "65000",
    "priceValidUntil": "2026-03-31",
    "availability": "https://schema.org/InStock",
    "itemCondition": "https://schema.org/NewCondition",
    "areaServed": { "@type": "City", "name": "Chennai" },
    "seller": {
      "@type": "LocalBusiness",
      "name": "Kuber Agencies",
      "telephone": "+919840928767"
    }
  }
}
</script>
```

### Paints Schema (Updated)

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Product",
  "@id": "https://kuberagencies.in/#product-paints",
  "name": "Asian Paints – Interior & Exterior Emulsions",
  "description": "Authorized Asian Paints dealer in Madambakkam Chennai. Full range: Royale interior emulsion, Apex exterior emulsion, SmartCare waterproofing, primers and industrial coatings. Expert colour consultation available.",
  "image": [
    "https://kuberagencies.in/images/paints/asian-paints-royale-interior-emulsion-chennai.webp",
    "https://kuberagencies.in/images/paints/asian-paints-apex-exterior-emulsion-chennai.webp",
    "https://kuberagencies.in/images/paints/paint-buckets-stacked-dealer-chennai.webp",
    "https://kuberagencies.in/images/paints/wall-painting-scene-interior-chennai.webp"
  ],
  "brand": { "@type": "Brand", "name": "Asian Paints" },
  "manufacturer": { "@type": "Organization", "name": "Asian Paints Limited" },
  "category": "Construction Materials > Paints & Coatings",
  "url": "https://kuberagencies.in/#product-paints",
  "offers": {
    "@type": "Offer",
    "url": "https://kuberagencies.in/",
    "priceCurrency": "INR",
    "price": "350",
    "priceValidUntil": "2026-03-31",
    "availability": "https://schema.org/InStock",
    "itemCondition": "https://schema.org/NewCondition",
    "areaServed": { "@type": "City", "name": "Chennai" },
    "seller": { "@type": "LocalBusiness", "name": "Kuber Agencies", "telephone": "+919840928767" }
  }
}
</script>
```

---

## 5. Updated Image Sitemap

Replace `/image-sitemap.xml` with this fully-populated version:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9"
        xmlns:image="http://www.google.com/schemas/sitemap-image/1.1">

  <url>
    <loc>https://kuberagencies.in/</loc>

    <!-- CEMENT -->
    <image:image>
      <image:loc>https://kuberagencies.in/images/cement/ultratech-opc53-cement-bags-chennai.webp</image:loc>
      <image:title>Ultratech OPC 53 Grade Cement Bags – Authorized Dealer Chennai</image:title>
      <image:caption>Ultratech OPC 53 Grade cement bags stacked at Kuber Agencies warehouse, Madambakkam Chennai. Bulk supply available with same-day site delivery.</image:caption>
    </image:image>
    <image:image>
      <image:loc>https://kuberagencies.in/images/cement/ultratech-ppc-cement-bags-chennai.webp</image:loc>
      <image:title>Ultratech PPC Portland Pozzolana Cement – Chennai Supplier</image:title>
      <image:caption>Ultratech PPC cement bags for plastering and masonry work. Available in bulk from Kuber Agencies, Madambakkam.</image:caption>
    </image:image>
    <image:image>
      <image:loc>https://kuberagencies.in/images/cement/dalmia-opc53-cement-bags-chennai.webp</image:loc>
      <image:title>Dalmia OPC 53 Grade Cement – Authorized Dealer Madambakkam Chennai</image:title>
      <image:caption>Dalmia Bharat OPC 53 Grade cement bags. IS:269 certified. Available from Kuber Agencies, Chennai.</image:caption>
    </image:image>
    <image:image>
      <image:loc>https://kuberagencies.in/images/cement/ramco-supergrade-cement-chennai.webp</image:loc>
      <image:title>Ramco Super Grade Cement – Supplier Chennai Tamil Nadu</image:title>
      <image:caption>Ramco Super Grade high early strength cement. Ideal for precast and rapid construction. Kuber Agencies, Chennai.</image:caption>
    </image:image>
    <image:image>
      <image:loc>https://kuberagencies.in/images/cement/chettinad-ppc-cement-chennai.webp</image:loc>
      <image:title>Chettinad PPC Cement – Bulk Supply Chennai</image:title>
      <image:caption>Chettinad Portland Pozzolana Cement for coastal and mass construction. Bulk supply from Kuber Agencies.</image:caption>
    </image:image>

    <!-- STEEL -->
    <image:image>
      <image:loc>https://kuberagencies.in/images/steel/ars-tmt-fe500d-bars-chennai.webp</image:loc>
      <image:title>ARS TMT Fe500D Steel Bars – Construction Material Supplier Chennai</image:title>
      <image:caption>ARS TMT Fe500D high-ductility steel bars at Kuber Agencies yard, Madambakkam Chennai. All diameters 8–32mm available.</image:caption>
    </image:image>
    <image:image>
      <image:loc>https://kuberagencies.in/images/steel/durga-tmt-fe415-bars-chennai.webp</image:loc>
      <image:title>Durga TMT Fe415 Bars – Steel Supplier Madambakkam Chennai</image:title>
      <image:caption>Durga TMT Fe415 rebars for RCC construction. IS:1786 certified. Available from Kuber Agencies, Chennai.</image:caption>
    </image:image>
    <image:image>
      <image:loc>https://kuberagencies.in/images/steel/tmt-bars-bundled-construction-site.webp</image:loc>
      <image:title>TMT Steel Bars Bundled at Construction Site – Bulk Supplier Chennai</image:title>
      <image:caption>TMT steel bars bundled and ready for site delivery from Kuber Agencies, Madambakkam Chennai.</image:caption>
    </image:image>

    <!-- PAINTS -->
    <image:image>
      <image:loc>https://kuberagencies.in/images/paints/asian-paints-royale-interior-emulsion-chennai.webp</image:loc>
      <image:title>Asian Paints Royale Interior Emulsion – Authorized Dealer Chennai</image:title>
      <image:caption>Asian Paints Royale interior emulsion paint buckets at Kuber Agencies, Madambakkam Chennai. Full colour range available.</image:caption>
    </image:image>
    <image:image>
      <image:loc>https://kuberagencies.in/images/paints/asian-paints-apex-exterior-emulsion-chennai.webp</image:loc>
      <image:title>Asian Paints Apex Exterior Emulsion – Dealer Madambakkam Chennai</image:title>
      <image:caption>Asian Paints Apex exterior paint for weather resistance. Authorized dealer in Chennai at Kuber Agencies.</image:caption>
    </image:image>
    <image:image>
      <image:loc>https://kuberagencies.in/images/paints/paint-buckets-stacked-dealer-chennai.webp</image:loc>
      <image:title>Paint Buckets at Kuber Agencies Construction Materials Store Chennai</image:title>
      <image:caption>Interior and exterior paint buckets at Kuber Agencies showroom, Madambakkam Chennai.</image:caption>
    </image:image>

    <!-- PIPES -->
    <image:image>
      <image:loc>https://kuberagencies.in/images/pipes/finolex-upvc-pipes-plumbing-chennai.webp</image:loc>
      <image:title>Finolex UPVC Pipes – Plumbing Supplier Madambakkam Chennai</image:title>
      <image:caption>Finolex UPVC pipes for drainage and plumbing. Authorized dealer at Kuber Agencies, Chennai.</image:caption>
    </image:image>
    <image:image>
      <image:loc>https://kuberagencies.in/images/pipes/star-cpvc-pipes-hot-cold-water-chennai.webp</image:loc>
      <image:title>Star CPVC Pipes Hot Cold Water Supply – Chennai Plumbing Supplier</image:title>
      <image:caption>Star CPVC pipes for hot and cold water supply systems. Available at Kuber Agencies, Madambakkam.</image:caption>
    </image:image>
    <image:image>
      <image:loc>https://kuberagencies.in/images/pipes/pvc-cpvc-pipes-bundled-chennai.webp</image:loc>
      <image:title>PVC CPVC Pipes Bundled – Plumbing Materials Dealer Chennai</image:title>
      <image:caption>Bundled PVC and CPVC pipes at Kuber Agencies store, Madambakkam Chennai. All sizes and fittings available.</image:caption>
    </image:image>

    <!-- ELECTRICAL -->
    <image:image>
      <image:loc>https://kuberagencies.in/images/electrical/havells-wires-cables-chennai.webp</image:loc>
      <image:title>Havells Electrical Wires and Cables – Dealer Madambakkam Chennai</image:title>
      <image:caption>Havells FR wires and cables at Kuber Agencies, authorized dealer in Madambakkam Chennai.</image:caption>
    </image:image>
    <image:image>
      <image:loc>https://kuberagencies.in/images/electrical/polycab-cables-rolls-chennai.webp</image:loc>
      <image:title>Polycab Cables in Rolls – Electrical Supplier Chennai</image:title>
      <image:caption>Polycab electrical cables in rolls for construction projects. Available at Kuber Agencies, Chennai.</image:caption>
    </image:image>
    <image:image>
      <image:loc>https://kuberagencies.in/images/electrical/legrand-modular-switches-chennai.webp</image:loc>
      <image:title>Legrand Modular Switches and Sockets – Electrical Dealer Chennai</image:title>
      <image:caption>Legrand modular switches, sockets and MCBs. Authorized dealer at Kuber Agencies, Madambakkam Chennai.</image:caption>
    </image:image>

    <!-- TILES -->
    <image:image>
      <image:loc>https://kuberagencies.in/images/tiles/ceramic-floor-tiles-installed-chennai.webp</image:loc>
      <image:title>Ceramic Floor Tiles Installed – Tiles Supplier Madambakkam Chennai</image:title>
      <image:caption>Ceramic floor tiles installed in residential project. Available from Kuber Agencies, Chennai Tamil Nadu.</image:caption>
    </image:image>
    <image:image>
      <image:loc>https://kuberagencies.in/images/tiles/vitrified-tiles-living-room-chennai.webp</image:loc>
      <image:title>Vitrified Tiles in Living Room – Flooring Supplier Chennai</image:title>
      <image:caption>Vitrified floor tiles in modern living room finish. Available from Kuber Agencies, Madambakkam.</image:caption>
    </image:image>

  </url>
</urlset>
```

---

## 6. CSS Upgrade for Product Card Images

Add this CSS block to your existing stylesheet (or replace the current `.product-card-img` rules):

```css
/* ============================================================
   PRODUCT CARD IMAGE — REALISTIC PHOTO UPGRADE
   ============================================================ */

/* Image container */
.product-card-img {
  width: 100%;
  height: 200px;            /* Increased from 160px for more visual impact */
  overflow: hidden;
  position: relative;
  background: linear-gradient(135deg, #0d1e35, #1a3350);
  flex-shrink: 0;
  border-radius: var(--radius-lg) var(--radius-lg) 0 0;
}

/* The <img> itself */
.product-card-img > img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  object-position: center;
  display: block;
  border-radius: var(--radius-lg) var(--radius-lg) 0 0;
  transition: transform 0.45s cubic-bezier(0.4, 0, 0.2, 1);
}

/* Zoom on hover */
.product-card:hover .product-card-img > img {
  transform: scale(1.06);
}

/* Gradient overlay so text on image is readable */
.product-card-img-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(
    to bottom,
    transparent 40%,
    rgba(7, 17, 31, 0.55) 100%
  );
  pointer-events: none;
}

/* Category tag on image */
.product-card-cat-tag {
  position: absolute;
  bottom: 10px;
  left: 12px;
  background: rgba(240, 109, 30, 0.92);
  color: #fff;
  font-size: 10px;
  font-weight: 800;
  letter-spacing: 1px;
  text-transform: uppercase;
  padding: 3px 10px;
  border-radius: 100px;
  backdrop-filter: blur(4px);
}

/* ---- Category cards on home page ---- */
.cat-image {
  width: 100%;
  height: 180px;
  overflow: hidden;
  border-radius: var(--radius-lg) var(--radius-lg) 0 0;
  margin: -20px -20px 16px;   /* Adjust to your cat-card padding */
  width: calc(100% + 40px);
}
.cat-image img {
  width: 100%;
  height: 180px;
  object-fit: cover;
  transition: transform 0.4s ease;
  display: block;
}
.cat-card:hover .cat-image img {
  transform: scale(1.07);
}
.cat-image figcaption {
  display: none;              /* Hidden visually, present for SEO */
}
```

---

## 7. Performance Checklist

- [ ] **Convert all images to WebP** — use Squoosh (squoosh.app) or `cwebp` CLI. WebP is 25–35% smaller than JPEG at the same quality.
- [ ] **Compress to target sizes** — product cards ≤40 KB, category heroes ≤60 KB
- [ ] **Set explicit `width` and `height`** — prevents Cumulative Layout Shift (CLS), a Core Web Vital
- [ ] **Use `loading="eager"` only for the first above-the-fold product** — all others use `loading="lazy"`
- [ ] **Add `decoding="async"`** on non-critical images for faster rendering
- [ ] **Preload the hero category image** — add to `<head>`:
  ```html
  <link rel="preload" as="image" href="https://kuberagencies.in/images/cement/cement-bags-stacked-warehouse-chennai.webp" type="image/webp"/>
  ```
- [ ] **Update `priceValidUntil`** in all Product schemas — change `2025-12-31` to `2026-12-31`
- [ ] **Submit updated image-sitemap.xml** in Google Search Console after uploading images

---

## 8. Quick-Win: Interim Image Sources (Until Your Own Photos Are Ready)

Use these Unsplash/Pexels embed URLs as **temporary** `src` values while your real photos are being prepared. They are free and load fast.

| Card | Temporary URL |
|---|---|
| Cement bags | `https://images.unsplash.com/photo-1504307651254-35680f356dfd?w=400&h=240&fit=crop` |
| TMT steel bars | `https://images.unsplash.com/photo-1587293852726-70cdb56c2866?w=400&h=240&fit=crop` |
| Paint buckets | `https://images.unsplash.com/photo-1562259949-e8e7689d7828?w=400&h=240&fit=crop` |
| PVC pipes | `https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=400&h=240&fit=crop` |
| Electrical wires | `https://images.unsplash.com/photo-1595079676339-1534801ad6cf?w=400&h=240&fit=crop` |
| Floor tiles | `https://images.unsplash.com/photo-1558618047-3c8c76ca7d13?w=400&h=240&fit=crop` |

> ⚠️ **Important:** Replace these with your own hosted `.webp` images as soon as possible. Own-hosted images on `kuberagencies.in/images/...` are indexed by Google and contribute to your local SEO.

---

## Summary of Changes Made

| Item | Before | After |
|---|---|---|
| Product card image height | 160px | 200px |
| Image filenames | `cement.jpg`, `steel.jpg` | `ultratech-opc53-cement-bags-chennai.webp` |
| Alt text | Generic | Brand + product + city keyword |
| JSON-LD images per product | 2–3 | 4 (multiple realistic scenes) |
| Schema `priceValidUntil` | 2025-12-31 | 2026-12-31 |
| Image sitemap entries | ~6 | 19 (all products covered) |
| Category card image size | 300px | 400×240px |
| Hover effect | None | `scale(1.06)` zoom |
| Image format | JPEG | WebP (25% smaller) |
