# Algobox Scene Registry (`NAMES.md`)
This file serves as the master metadata register mapping Algobox Scene IDs (`.phz`) to their respective title, original author, and brief description.

*(Order is chronological.)*
| Scene ID | Title | Author | Description | Filesize |
| -------- | -------- | -------- | -------- | -------- |
| `257596` | Short List of Rules - READ THEM! | Xray | This is an updated list of a few rules that get violated more often than most of the other Algobox rules.<br><br>NOTES: Comments have been disabled.<br><br>Enjoy Algodoo as I have for more than a decade.<br><br>Xray, Algobox Admin and lover of science. | 113.35 kB |
| `40313` | OFFROAD CAR !! | cata | hello!!<br><br>I was amazed! !<br><br>4WD is nice to be selected in the screenshot.<br>It is fun to go to draw the scene in the future.<br>I love PHUN! !<br><br>Update Aug,10.2015<br>Remake in Algodoo! | 342.04 kB |
| `242904` | Why Subscribe? | Xray | Open the scene and read the text. You'll be glad you did!<br><br><br>Updated text in scene. 7 Sept. 2021<br><br><br>**About this scene:**<br>I occasionally get asked the following question about this scene:<br>*"How does the scene stay in the number one spot on Algobox?"*<br><br>Answer: My contact person at Algoryx (Algoryx is the company that owns this website and the Algodoo software) makes this scene a "Sticky Scene" by forcing the "Date Added" date to be in the future, and by forcing the number of views and the number of downloads to be a very large number. I cannot do that because I do not have Administrative control of the website software. When the current calendar date becomes the "Date Added" date, then the scene will begin to drop out of the number one position, and my contact and I will discuss if we want to keep this scene a "Sticky", edit the scene, or replace it with some other scene.<br><br>Now you know! | 111.21 kB |
| `62815` | 7 segment display using rod logic | conundrumer | The red/green matrix decodes binary into hexademical. The green/blue matrix decodes hexadecimal into 7 segment display code. The pink rods is an array of D latches, serving as a memory buffer for the decoded data. The display itself is directly connected to the memory buffer. I could make it change digits more smoothly by adding transistors in between, but I didn't really feel like it, so deal with the jerky motion :\|<br><br>The dark-grey circle is the clock, which triggers a series of T flip-flops (counts up in binary) that feeds in the data, and the computation of the data through the long levers connected to transistors.<br><br>Based off of twinkle's turing mobile and this: http://halfbakedmaker.org/2009/12/05/intro-to-rod-logic/ | 101.42 kB |

## Formatting Guidelines for Contributors
When adding new entries to this index, please maintain the standard pipe-delimited Markdown table format:
```markdown
| `<scene_id>` | <Scene Title> | <Author Name or "Unknown"> | <Full Description> | <Filesize> |
```

1. **Scene ID:** Must match the exact numerical filename located under `scenes/<scene_id>.phz` without the extension.
2. **Title:** The original scene title as published on Algobox.
3. **Author:** Creator username, or `Unknown` if missing.
4. **Description:** The full description on the scene's details.
5. **Filesize:** The size of the scene. You should find this on the scene's details.
