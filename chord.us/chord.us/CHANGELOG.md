### Version 0.2.1

- cleaning up formatting based on eslint requirements adjusting height of want more component moving styling out of inline and into classes installing codyhouse framework dependency for use with the stacking cards implementation fixing resizing bug and missing animations related to the stacking cards implementation
- moving more inline styling into global css classes
- Adds vscode-specific settings for EOL settings for everyone.
- breaking out common button controls into a separate component
- header nav updates
- Adding custom fonts Adding alternate version of arrow image Renaming Slide1 component, and repurposing the component to eliminate the need for 3 other similar slide components adding scripts to the global header Updating the BasicButton component and each of its existing use cases
- Updating component structure, adding data to facilitate easier content updates in the future.
- Updating landing page images Adding more new fonts and images Updating styling of carousel slides and related components based on latest designs Updating copy throughout
- more styling updates
- cleanup
- adding placeholder images for alternate versions of layout - for future use
- temp check-in profile modal
- added profile avatar/name on the top right added basic profile modal fixed warnings fixed product name branding
- branding names
- adding more image assets into the project adding custom positioning for each of the different carousel images adding image property to the carousel content object array tweaking css on various components to move closer to layout designs
- adding new font family adding updated ce logo adding new version of landing page image that removes extra, unnecessary background element fixing issue with horizontal scroll bar showing up on mobile fixing alignment issues with the nav component for mobile fixing responsiveness of the SimpleReliable component fixing responsiveness of the MakeItYours component adding slide index prop to carousel slides in order to display slide # and title, per the updated designs
- profile card
- typo
- fixing nav alignment issue on larger screen sizes fixing invalid type errors on various button click handlers
- adding new icons to be used in the Make it yours section updating one of the carousel images with the uncropped version hiding stacked carousel card effect on mobile improving text alignment within the BasicButton component modifying the max height of the carousel component, to work better on mobile devices moving more inline styling into classes improving responsiveness of the MakeItYours and IntroChordVideo components beginning work on fixing regression with the stacking cards feature used by EnterRoom component
- adding png version of logo to replace svg version, to avoid issue with font styling being lost on systems that don't have the font installed
- fixing spelling error that caused fatal compilation error adjusting width of slide title for larger devices
- adding the answerdash script making more improvements to responsiveness for components: EnterRoom, Experience, MakeItYours, Products, WantMore, WatchVideosTogether and Footer
- fix stacking cards issue
- added new assets switch colors in in make it yours added the icons in make it yours
- moving assets to landingPage folder changed color for the card SVGs updated colors and assets for carousel fixed stacking cards updated asset in intro to chord changed the context of css for the field label in profile dropdown
- adding this asset
- adding icon asset
- Updated text blocks and styling in want more section
- also updated the icons here Added icons to the customer engagement section Adjusted the Get in Touch footer control and created new component so this styling can be easily applied throughout Updated nav logo Updated powered by cloud engage icon Improved alignment of text column on SimpleReliable and MakeItYours Improved alignment of text blocks on the Enter Room stacking cards Improved alignment of text blocks within the carousel slides Added quick start and group video icons Updated images and image strip placement for the group video section Updated images, text and alignment in the experience the new era section
- Updating carousel slide layout for mobile Adjusting positioning of background browser logos for mobile
- added strapi
- Removes the strapi backend that was installed using Yarn
- adds .gitattributes to resolve EoL issues
- adds lint-staged precommit hook
- Ran `prettier --write .` on entire project.
- Fixes on click handler

### Version 0.2.0

- Merges master into development branch.
- Resolves resultant conflicts.

### Version 0.1.0

- Project setup for es-linting, Prettier formatting and i18n Internationalization.

### Version 0.0.1

- initialize
