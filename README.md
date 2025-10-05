<!DOCTYPE html>
<!-- ... toàn bộ code như cũ ... -->

<script>
// ... toàn bộ units đã có ...

// Thêm câu mới vào Unit 2
units[2].sentences.push(
  {
    prompt: "What do you do in the morning?",
    subjects: ["I", "We", "You", "They", "He", "She"],
    others: ["go to school", "have breakfast", "clean the teeth"],
    getAnswer: (sub, oth) => {
      if (sub === "He" || sub === "She") {
        if (oth.startsWith("go")) return `${sub} goes to school in the morning.`;
        if (oth.startsWith("have")) return `${sub} has breakfast in the morning.`;
        if (oth.startsWith("clean")) return `${sub} cleans teeth in the morning.`;
      }
      return `${sub} ${oth} in the morning.`;
    }
  },
  {
    prompt: "What do you do in the evening?",
    subjects: ["I", "We", "You", "They", "He", "She"],
    others: ["have dinner", "go to bed", "wash the face"],
    getAnswer: (sub, oth) => {
      if (sub === "He" || sub === "She") {
        if (oth.startsWith("go")) return `${sub} goes to bed in the evening.`;
        if (oth.startsWith("have")) return `${sub} has dinner in the evening.`;
        if (oth.startsWith("wash")) return `${sub} washes face in the evening.`;
      }
      return `${sub} ${oth} in the evening.`;
    }
  }
);
</script>
