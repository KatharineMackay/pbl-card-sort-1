<!-- PAGE 1: Colour Card Sort with Delete Dot -->
<!DOCTYPE html>
<html lang="en-AU">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Visual Card Sort – Colours</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
      background: #f4f4f4;
    }
    h1, .instructions {
      text-align: center;
    }
    .palette, .bins {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      margin-bottom: 30px;
      gap: 10px;
    }
    .colour {
      width: 50px;
      height: 50px;
      border-radius: 50%;
      cursor: grab;
      user-select: none;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: bold;
      font-size: 1.5rem;
      box-sizing: border-box;
    }
    .bin {
      border: 2px dashed #ccc;
      padding: 10px;
      min-height: 120px;
      min-width: 150px;
      background: #fff;
      text-align: center;
    }
    .bin h3 {
      font-size: 1rem;
      margin: 0 0 8px 0;
    }
    .bin-content {
      min-height: 80px;
      min-width: 80px;
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
      justify-content: center;
    }
    #submit-btn, #reset-btn, #next-btn {
      display: inline-block;
      margin: 10px;
      padding: 14px 24px;
      font-size: 1.2rem;
      cursor: pointer;
    }
    #buttons-container {
      text-align: center;
      margin-bottom: 20px;
    }
    #comments-label, #comments {
      display: block;
      max-width: 90%;
      margin: 0 auto 10px auto;
      font-size: 1.1rem;
    }
    #comments {
      height: 100px;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 4px;
      box-sizing: border-box;
      resize: vertical;
    }

    /* Delete dot styling */
    .delete-dot {
      color: red;
      font-weight: bold;
      text-align: center;
      border: 2px solid red;
      background: #fff0f0;
      user-select: none;
    }

    @media (max-width: 600px) {
  .bin {
    min-width: 90px;       /* smaller width */
    min-height: 90px;      /* smaller height */
    padding: 6px;
  }

  .bin h3 {
    font-size: 0.8rem;    /* smaller heading text */
  }

  .bin-content {
    min-height: 70px;
    min-width: 70px;
    gap: 4px;
  }

  .colour {
    width: 35px;          /* smaller colour dots */
    height: 35px;
    font-size: 1.2rem;    /* smaller font size for delete dot */
  }
}

  </style>
</head>
<body>
  <h1>Visual Card Sort – Colours</h1>
  <p class="instructions">Drag and place <strong>colours</strong> into the bins below. Then click <em>Next</em>.</p>

  <div class="palette" id="palette"></div>
  <div class="bins" id="bins"></div>

  <label for="comments" id="comments-label">Optional Comments:</label>
  <textarea id="comments" placeholder="Write any comments here..."></textarea>

  <div id="buttons-container">
    <button id="reset-btn" type="button">Reset</button>
    <button id="next-btn" type="button">Next</button>
  </div>

  <script src="https://cdn.jsdelivr.net/npm/sortablejs@1.15.0/Sortable.min.js"></script>
  <script>
    const colours = ["green", "blue", "purple", "#f0f", "red", "orange", "yellow", "black", "#888"];
    const bins = ["Recycling", "Metal", "Glass", "E-waste", "Landfill", "Compost", "10c Cans/Bottles", "Soft Plastic"];

    const palette = document.getElementById("palette");
    const binsDiv = document.getElementById("bins");

    // Create colour dots
    colours.forEach(col => {
      const div = document.createElement("div");
      div.className = "colour";
      div.style.background = col;
      div.setAttribute("data-type", "colour");
      div.setAttribute("data-value", col);
      palette.appendChild(div);
    });

    // Add a delete dot (❌) to palette
    const deleteColour = document.createElement("div");
    deleteColour.className = "colour delete-dot";
    deleteColour.textContent = "❌";
    deleteColour.setAttribute("data-type", "delete");
    palette.appendChild(deleteColour);

    // Create bins
    bins.forEach(name => {
      const container = document.createElement("div");
      container.className = "bin";
      container.setAttribute("data-name", name);
      container.innerHTML = `<h3>${name}</h3><div class="bin-content"></div>`;
      binsDiv.appendChild(container);

      // Make bin-content droppable and draggable
      Sortable.create(container.querySelector(".bin-content"), {
        group: "shared",
        animation: 150,
        onAdd: function(evt) {
          const original = evt.item;
          const type = original.getAttribute("data-type");

          if (type === "delete") {
            original.remove(); // Prevent adding delete dot inside bins
            return;
          }

          // When dragging from palette, clone it into bin (so palette item stays)
          if (evt.from === palette) {
            const clone = original.cloneNode(true);
            clone.classList.remove("sortable-ghost");
            evt.to.removeChild(original);
            evt.to.appendChild(clone);
          }
        }
      });
    });

    // Make palette draggable & able to receive dragged items back
    Sortable.create(palette, {
      group: {
        name: "shared",
        pull: "clone",
        put: true
      },
      sort: false,
      animation: 150
    });

    // Make the delete dot accept dragged items and remove them
    Sortable.create(deleteColour, {
      group: "shared",
      animation: 150,
      onAdd: function(evt) {
        evt.item.remove();
      }
    });

    // Reset button clears bins and comments
    document.getElementById("reset-btn").addEventListener("click", () => {
      document.querySelectorAll(".bin-content").forEach(c => c.innerHTML = "");
      document.getElementById("comments").value = "";
    });

    // Next button saves data & goes to page2.html
    document.getElementById("next-btn").addEventListener("click", () => {
      const result = {};
      bins.forEach(name => {
        const binContent = document.querySelector(`[data-name="${name}"] .bin-content`);
        const items = [...binContent.children];
        result[name] = items.map(el => el.getAttribute("data-value"));
      });

      const comments = document.getElementById("comments").value.trim();
      localStorage.setItem("page1result", JSON.stringify(result));
      localStorage.setItem("page1comments", comments);
      window.location.href = "page2.html";
    });
  </script>
</body>
</html>
