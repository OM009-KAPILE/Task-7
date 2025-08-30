import React, { useState } from "react";

function App() {
  // Counter state
  const [count, setCount] = useState(0);

  // Input text state
  const [text, setText] = useState("");

  return (
    <div style={styles.container}>
      <h1>Day 7 Mini Task</h1>

      {/* Counter Section */}
      <div style={styles.card}>
        <h2>Counter</h2>
        <p>Count: {count}</p>
        <button onClick={() => setCount(count + 1)} style={styles.btn}>
          Increment
        </button>
        <button onClick={() => setCount(count - 1)} style={styles.btn}>
          Decrement
        </button>
        <button onClick={() => setCount(0)} style={styles.btn}>
          Reset
        </button>
      </div>

      {/* Live Text Preview Section */}
      <div style={styles.card}>
        <h2>Live Text Preview</h2>
        <input
          type="text"
          placeholder="Type something..."
          value={text}
          onChange={(e) => setText(e.target.value)}
          style={styles.input}
        />
        <p>Preview: {text}</p>
      </div>
    </div>
  );
}

// Some simple inline styles
const styles = {
  container: {
    fontFamily: "Arial, sans-serif",
    textAlign: "center",
    marginTop: "50px",
  },
  card: {
    border: "1px solid #ddd",
    borderRadius: "10px",
    padding: "20px",
    margin: "20px auto",
    width: "300px",
    boxShadow: "0 4px 8px rgba(0,0,0,0.1)",
  },
  btn: {
    margin: "5px",
    padding: "10px 15px",
    border: "none",
    borderRadius: "5px",
    cursor: "pointer",
    backgroundColor: "#4CAF50",
    color: "white",
  },
  input: {
    padding: "10px",
    width: "80%",
    marginTop: "10px",
    borderRadius: "5px",
    border: "1px solid #ccc",
  },
};

export default App;
