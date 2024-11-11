---
title: "Publications"
date: 2021-05-28T09:27:27-05:00
draft: false
layout: page
aliases: /research/
---
<style>
.tabs {
  display: flex;
  cursor: pointer;
  margin-bottom: 20px;
  border-bottom: 1px solid #ccc;
  gap: 8px;
}
.tab {
  padding: 9px 18px;
  transition: all 0.3s ease;
  position: relative;
  font-weight: 500;
}
.tab:hover {
  background-color: #f5f5f5;
  color: #0056b3;
}
.tab.active {
  border: 1px solid #ccc;
  border-bottom: none;
  border-radius: 6px 6px 0 0;
  color: #007bff;
  background-color: white;
}
.tab.active::after {
  content: '';
  position: absolute;
  bottom: -1px;
  left: 0;
  right: 0;
  height: 1px;
  background-color: white;
}
.content {
  min-height: 200px;
  animation: fadeIn 0.3s ease-in-out;
}
.tab-content {
  display: none;
  padding: 20px 0;
}
.tab-content.active {
  display: block;
}
.tab-content h3 {
  margin-top: 0;
  color: #2c3e50;
  font-size: 1.5em;
}
.publication-entry {
  margin-bottom: 1.5em;
  line-height: 1.6;
}
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}
</style>

<div class="tabs">
<div class="tab active" onclick="showTab('tardis')">TARDIS</div>
<div class="tab" onclick="showTab('carsus')">CARSUS</div>
</div>

<div class="content">
<div id="tardis" class="tab-content active">
<h3>Papers using the <i>TARDIS</i> package</h3>
{{< papers >}}
</div>

<div id="carsus" class="tab-content">
<h3>Papers using the <i>CARSUS</i> package</h3>
<div class="publication-entry">
  <p><strong>James H. Gillanders, Michael McCann, Stuart A. Sim, Stephen J. Smartt, and Connor P. Ballance</strong> 2021, MNRAS,
  <em>"Constraints on the presence of platinum and gold in the spectra of the kilonova at2017gfo"</em>
  <a href="https://ui.adsabs.harvard.edu/abs/2021MNRAS.506.3560G" target="_blank" rel="noopener nofollow">ADS Link</a></p>
</div>
</div>
</div>

<script>
function showTab(tabId) {
  const contents = document.querySelectorAll('.tab-content');
  const tabs = document.querySelectorAll('.tab');
  
  contents.forEach(content => {
    content.classList.remove('active');
    content.style.opacity = 0;
  });
  
  tabs.forEach(tab => tab.classList.remove('active'));
  
  const selectedContent = document.getElementById(tabId);
  const selectedTab = event.target;
  
  selectedContent.classList.add('active');
  selectedTab.classList.add('active');
  
  // Trigger reflow to ensure animation plays
  void selectedContent.offsetWidth;
  selectedContent.style.opacity = 1;
}
</script>