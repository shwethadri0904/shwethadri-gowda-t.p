const express = require("express");
const cors = require("cors");

const projectRoutes = require("./routes/projects");
const contactRoutes = require("./routes/contact");

const app = express();

app.use(cors());
app.use(express.json());

app.use("/projects", projectRoutes);
app.use("/contact", contactRoutes);

app.listen(5000, () => {
  console.log("server up on 5000");
});
