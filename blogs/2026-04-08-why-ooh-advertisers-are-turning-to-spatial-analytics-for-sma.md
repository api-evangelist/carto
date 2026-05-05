---
title: "Why OOH advertisers are turning to spatial analytics for smarter campaigns"
url: "https://carto.com/blog/why-ooh-advertisers-use-location-intelligence/"
date: "Wed, 08 Apr 2026 00:00:00 +0000"
author: ""
feed_url: "https://carto.com/blog/index.xml"
---
<p>A billboard on a busy highway gets thousands of impressions per day. But how many of those impressions come from your target audience? And how do you prove that to the client writing the check?</p>
<p><a href="https://carto.com/solutions/ooh/">Out-of-home advertising</a> is one of the oldest forms of media, and one of the hardest to measure. While digital channels track every click and conversion in real time, OOH planners still rely heavily on rough traffic estimates, past experience, and manual spreadsheet work to build campaigns. That gap between OOH&rsquo;s physical reach and its analytical maturity is closing fast, and spatial analytics, the practice of using Location Intelligence to analyze geographic patterns and relationships, is what&rsquo;s closing it.</p>
<h2 id="the-measurement-problem-ooh-cant-ignore">The measurement problem OOH can&rsquo;t ignore</h2>
<p>Digital advertising set a new standard for accountability. Clients now expect granular audience data, attribution models, and performance metrics from every channel in their media mix, including outdoor.</p>
<p>OOH has struggled to meet that standard. Traditional audience measurement relies on traffic counts and broad demographic estimates for a given area. A panel on a highway might be rated for 50,000 daily impressions, but that number says nothing about who those people are, where they came from, or what they did after seeing the ad.</p>
<p>Without better data, OOH risks being the line item that gets cut when budgets tighten. Media planners know the channel works. Proving it with numbers that satisfy a CFO is the hard part.</p>
<h2 id="five-pain-points-spatial-analytics-solves">Five pain points spatial analytics solves</h2>
<h3 id="1-thin-audience-data-for-panel-selection">1. Thin audience data for panel selection</h3>
<p>Most OOH planning tools tell you how many people pass a billboard. Spatial analytics tells you <strong>who</strong> they are. By combining mobility data, demographic information, and points of interest around each panel location, planners can match inventory to specific audience segments. The <a href="https://carto.com/data-observatory/">CARTO Data Observatory</a> provides access to thousands of these datasets, from foot traffic patterns to consumer spending profiles, ready to enrich your panel inventory.</p>
<p>Instead of buying a panel because it&rsquo;s on a busy road, you buy it because the mobility patterns show that 35% of passersby match your target profile of frequent gym-goers aged 25 to 44. That level of specificity changes the conversation with clients entirely.</p>
<p>This kind of audience profiling is also getting sharper as the field moves beyond traditional demographic segments. Hamish Gibbs&rsquo;s talk at the Spatial Data Science Conference NYC 2025, <a href="https://youtu.be/N_p1r-N_GZM">Beyond Demographics: Introducing the Behavioral Census for Urban Modeling</a>, explores how lifestyle embeddings, reusable representations of human activity learned from mobility data, give planners a far more nuanced view of who actually moves through a place than age and income brackets can capture on their own.</p>
<h3 id="2-managing-thousands-of-assets-across-geographies">2. Managing thousands of assets across geographies</h3>
<p>Large OOH media owners manage portfolios of 10,000+ panels across multiple cities or countries. Keeping track of availability, format, location context, and audience characteristics in spreadsheets is a recipe for missed opportunities.</p>
<p>Interactive maps with filtering by geography, asset type, audience segment, and proximity to POIs make inventory exploration practical at scale. Planners can zoom from a national view to a single street corner, filter for digital screens near university campuses, and build a shortlist in minutes rather than hours.</p>
<h3 id="3-slow-campaign-scenario-planning">3. Slow campaign scenario planning</h3>
<p>Testing different panel combinations to find the best coverage and audience overlap takes too long when the workflow involves exporting data, running it through a separate tool, and pasting results back into a planning deck.</p>
<p>When the analysis runs directly in a data warehouse like <a href="https://carto.com/bigquery/spatial-analytics/">BigQuery</a> or <a href="https://carto.com/snowflake/spatial-analytics/">Snowflake</a>, scenario planning becomes interactive. Swap panels in and out, recalculate coverage and audience reach, and compare three campaign options in the time it used to take to build one.</p>
<h3 id="4-fuzzy-attribution-and-roi-measurement">4. Fuzzy attribution and ROI measurement</h3>
<p>Proving that an OOH campaign influenced store visits, app installs, or purchases requires connecting physical exposure to downstream behavior. That connection lives in spatial data.</p>
<p>By comparing mobility patterns before, during, and after a campaign, analysts can measure uplift in foot traffic to specific locations. Overlaying transaction data or app activity with panel exposure zones creates an attribution model that goes beyond &ldquo;people drove past the billboard.&rdquo; <a href="https://carto.com/glossary/spatial-indexes/">H3 spatial indexes</a> make these comparisons consistent across different geographies and time periods.</p>
<h3 id="5-static-reporting-in-a-programmatic-world">5. Static reporting in a programmatic world</h3>
<p>Programmatic digital OOH (pDOOH) is growing fast, and it demands real-time data integration. Static quarterly reports on audience composition don&rsquo;t work when campaigns activate dynamically based on weather, time of day, or live audience density.</p>
<p>Spatial analytics pipelines that run inside the data warehouse can feed pDOOH platforms with up-to-date audience scores and location context. Automated workflows refresh the data on schedule, so campaign activation rules always work with current information.</p>
<h2 id="what-the-workflow-looks-like-in-practice">What the workflow looks like in practice</h2>
<p>A mid-size OOH media owner wants to help an insurance client reach homeowners aged 35 to 55 in flood-prone areas across three metro regions. Here is how spatial analytics changes that brief from vague to precise:</p>
<ol>
<li>
<p><strong>Inventory mapping.</strong> All 8,000 panels are visualized on an interactive map in <a href="https://carto.com/builder/">CARTO Builder</a>, filterable by format, geography, and availability.</p>
</li>
<li>
<p><strong>Audience enrichment.</strong> Mobility and demographic data from the <a href="https://carto.com/data-observatory/">CARTO Data Observatory</a> are joined to each panel&rsquo;s catchment area. Panels are scored by the percentage of passersby matching the target profile.</p>
</li>
<li>
<p><strong>Risk overlay.</strong> Flood zone data is layered in to identify panels located in or near areas where the insurance message is most relevant.</p>
</li>
<li>
<p><strong>Scenario comparison.</strong> Three campaign plans with different panel selections are compared side by side for reach, audience fit, and cost efficiency. The analysis runs directly in your cloud data warehouse, so results come back in seconds.</p>
</li>
<li>
<p><strong>Post-campaign measurement.</strong> After the campaign runs, mobility data is analyzed to measure foot traffic uplift at the client&rsquo;s local offices within panel exposure zones.</p>
</li>
</ol>
<p>The entire workflow runs in the client&rsquo;s data warehouse. No data exports, no third-party tools, one connected process from planning to measurement.</p>
<h2 id="how-billups-uses-spatial-analytics-for-ooh-at-global-scale">How billups uses spatial analytics for OOH at global scale</h2>
<p><a href="https://carto.com/customer-stories/billups-transforms-out-of-home-media-strategy-with-location-intelligence/">billups</a>, the world&rsquo;s largest independent Out-of-Home (OOH) technology and services company, deployed CARTO worldwide to centralize its spatial analytics and visualize aggregated audience movement data across geographies.</p>
<p>The results speak for themselves:</p>
<ul>
<li><strong>18 countries</strong>: Empowered global growth into 18 countries across North America, EMEA, and APAC with scalable mapping and visualization capabilities.</li>
<li><strong>87% of brands</strong> now receive CARTO powered visualizations in their sales presentations, strategy reviews and performance reports.</li>
<li><strong>80% of visualizations</strong> are created independently by media teams, dramatically reducing dependence on specialized data analysts.</li>
<li><strong>20% reduction in data ingestion time</strong>, freeing data analysts to focus on new capabilities and strategic initiatives and generating an estimated <strong>$150,000</strong> of annual reclaimed productivity value.</li>
</ul>
<p><img alt="billups customer story card featuring a quote from Tyler Kappen on how CARTO helps deliver better outcomes for OOH clients" src="https://carto.com/cdn.prod.website-files.com/63483ad423421bd16e7a7ae7/why-ooh-advertisers-use-location-intelligence-billups-customer-story.webp" /></p>
<h2 id="how-viooh-brings-spatial-analytics-to-programmatic-ooh">How VIOOH brings spatial analytics to programmatic OOH</h2>
<p><a href="https://carto.com/customer-stories/viooh/">VIOOH</a> (pronounced &ldquo;view&rdquo;) is a leading global digital out of home (OOH) supply-side platform. Established in 2018 and headquartered in London, VIOOH was born out of a need to digitize and revolutionize the OOH sector through programmatic capabilities and data, facilitating premium marketplace connections between buyers and sellers.</p>
<p>Using CARTO Builder, the VIOOH team can easily communicate the geographical distribution of assets for more precise campaign strategies. Combined with direct, native access to <a href="https://carto.com/snowflake/spatial-analytics/">Snowflake&rsquo;s Data Cloud</a> from the CARTO platform, VIOOH empowers clients to make more data-driven decisions and execute more effective campaigns, achieving increased ROI for advertisers.</p>
<p><img alt="VIOOH customer story card featuring a quote from Benoît Vidal on CARTO’s cloud-driven Snowflake integration" src="https://carto.com/cdn.prod.website-files.com/63483ad423421bd16e7a7ae7/why-ooh-advertisers-use-location-intelligence-viooh-customer-story.webp" /></p>
<h2 id="moving-ooh-from-intuition-to-evidence">Moving OOH from intuition to evidence</h2>
<p>OOH advertising is not going away. Outdoor media reaches audiences that digital channels miss, in physical spaces where attention is less fragmented. But the industry&rsquo;s ability to compete for budget depends on its ability to prove results with the same rigor as digital.</p>
<p>Spatial analytics gives OOH professionals the tools to do exactly that: target with precision, plan with speed, and measure with confidence.</p>
<p><a href="https://carto.com/request-demo/">Request a demo</a> to see how CARTO helps OOH teams build smarter campaigns with spatial analytics.</p>
<p><em>Editor&rsquo;s note: This post was originally published in 2022 and has been completely revamped and updated for accuracy and comprehensiveness.</em></p>
