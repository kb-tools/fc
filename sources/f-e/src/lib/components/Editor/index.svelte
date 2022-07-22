<style>
  .editor {
    display: flex;
    flex-direction: column;
    width: 100%;
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
  <section contenteditable="true" class='editor-contents'></section>
</article>
