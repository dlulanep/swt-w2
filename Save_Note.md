// ...existing code...
function saveNote() {
  const title = document.getElementById('note-title').value.trim();
  const content = document.getElementById('note-content').value.trim();

  // Input validation: prevent saving if title or content is empty
  if (!title || !content) {
    alert('Both title and content are required.');
    return;
  }

  // ...rest of your save logic...
}
// ...existing code...