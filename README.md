# index.js

$ROOT 
import "./styles.css";
import { computePosition } from "@floating-ui/dom";

const reference = document.getElementById("reference");
const floating = document.getElementById("floating");

computePosition(reference, floating, {
  // Try changing this to a different side.
  placement: "top"
}).then(({ x, y }) => {
  Object.assign(floating.style, {
    top: `${y}px`,
    left: `${x}px`
  });
});
