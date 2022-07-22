<style>
  .editor {
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: auto 1fr;
    grid-template-areas:
      'editor-title'
      'editor-contents'
    ;
    gap: var(--main-gap);
    width: var(--editor-width);
    padding: max(1vh, 1vw);
    filter: var(--filter-drop-shadow);
  }

  .editor > h1 {
    display: flex;
    flex-direction: column;
    margin: 0;
    padding: 0;
  }

  .editor-title {
    grid-area: editor-title;
    min-height: 4vh;
    justify-content: center;
    align-items: center;
  }

  .editor-contents {
    grid-area: editor-contents;
    flex-direction: column;
    height: 100vh;

    justify-content: start;
    align-items: flex-start;
  }

  [contenteditable] {
    display: flex;
    padding: 0;
    background-color: var(--contenteditable-background-color);
    border: var(--contenteditable-border);
  }
</style>

<article class='editor'>
  <h1>
    <section contenteditable="true" class='editor-title'></section>
  </h1>
  <section contenteditable="true" class='editor-contents'></section>
</article>
