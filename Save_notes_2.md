<script>
  let notes = [];

  function saveNote() {
    const titleInput = document.getElementById('note-title');
    const contentInput = document.getElementById('note-content');
    const title = titleInput.value.trim();
    const content = contentInput.value.trim();

    // Input validation: prevent saving if title or content is empty
    if (!title || !content) {
      alert("Please fill in both fields.");
      return;
    }

    const note = { id: Date.now(), title, content };
    notes.push(note);
    renderNotes();

    // Clear input fields after saving
    titleInput.value = '';
    contentInput.value = '';
  }

  function renderNotes() {
    const container = document.getElementById('notes');
    container.innerHTML = '';
    notes.forEach(note => {
      const div = document.createElement('div');
      div.className = 'note';
      div.innerHTML = `
        <h3>${note.title}</h3>
        <p>${note.content}</p>
        <button onclick="editNote(${note.id})">Edit</button>
        <button onclick="deleteNote(${note.id})">Delete</button>
      `;
      container.appendChild(div);
    });
  }

  function editNote(id) {
    const note = notes.find(n => n.id === id);
    if (!note) return;
    document.getElementById('note-title').value = note.title;
    document.getElementById('note-content').value = note.content;
    deleteNote(id);
  }

  function deleteNote(id) {
    notes = notes.filter(n => n.id !== id);
    renderNotes();
  }
</script>