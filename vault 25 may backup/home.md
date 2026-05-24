---

---

💡 [[ideas|ideas]] - [[photos|photos]] - [[ilinks|links]] - [[quotes|quotes]] 
✅ [[tasks S|tasks]] - [[history|history]] - [[rewards|shop]] - [[tasks.base]]
🛒 [[receipt|receipt]] 
🛍️ [[wish list|wish list]] 
🔰 [[Saved Messages|Saved Messages]] - [[tier 1|1]] - [[tier 2|2]] - [[tier 3|3]] 
📝 [[Research canva.canvas|Research Canva]]



```dataviewjs
const trackerData = {
  heatmapTitle: "Daily",
  year: 2026,
  separateMonths: true,
  showCurrentDayBorder: true,
  colorScheme: {
    customColors: ["#c6efce", "#70c98a", "#2ea64a", "#1a6b30", "#0d3d1a"]
  },
  intensityConfig: {
    scaleStart: 100,
    scaleEnd: 5000
  },
  entries: []
};

const pages = dv.pages('"Daily"')
  .where(p => /^\d{4}-\d{2}-\d{2}$/.test(p.file.name) && p.file.size > 10);

for (let page of pages) {
  trackerData.entries.push({
    date: page.file.name,
    intensity: page.file.size
  });
}

renderHeatmapTracker(this.container, trackerData);
```

```apb
My Title: 0/100
```


