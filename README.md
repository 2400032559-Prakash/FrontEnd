import React from "react";

function UserCard({ name, age, bio }) {
  const cardStyle = {
    border: "1px solid #ccc",
    borderRadius: "8px",
    padding: "16px",
    maxWidth: "300px",
    boxShadow: "2px 2px 8px rgba(0,0,0,0.1)",
    backgroundColor: "green"
  };
  const nameStyle = {
    margin: "0 0 8px 0",
    fontSize: "1.5em"
  };
  const ageStyle = {
    margin: "0 0 8px 0",
    color: "red"
  };
  const bioStyle = {
    margin: 0,
    fontSize: "1em",
    color: "blue"
  };

  return (
    <div style={cardStyle}>
      <h2 style={nameStyle}>{name}</h2>
      <p style={ageStyle}>Age: {age}</p>
      <p style={bioStyle}>{bio}</p>
    </div>
  );
}

export default UserCard;
import React from "react";
import "./UserCard.css";

function UserCard({ name, age, bio }) {
  return (
    <div className="user-card">
      <h2 className="user-name">{name}</h2>
      <p className="user-age">Age: {age}</p>
      <p className="user-bio">{bio}</p>
    </div>
  );
}

export default UserCard;
.user-card {
  border: 1px solid #ccc;
  border-radius: 8px;
  padding: 16px;
  max-width: 300px;
  box-shadow: 2px 2px 8px rgba(0, 0, 0, 0.1);
  background-color:black;
}

import React from "react";
import UserCard from "./UserCard";

function App() {
  return (
    <div>
      <UserCard
        name="Prakash Kumar"
        age={20}
        bio="Software student who loves reading."
      />
      <UserCard
        name="Prakash"
        age={21}
        bio="B.tech Student."
      />
    </div>
  );
}

export default App;
