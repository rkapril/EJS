# EJS (Embedded Javascript)
## Tags
```
<%= %> // Output
<% %> // Execute
<%- %> // Render HTML
<%% %%> // Show <% or %>
<%# %> // comment
<%- include("header.ejs") %> // Insert another EJS file
```
### Example
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>EJS Tags</title>
  </head>

  <body>
    <h1>
      <!-- Title goes here -->
      <%= title %>
    </h1>
    <p>
      Current second:
      <!-- Current second goes here -->
      <%= seconds %>
    </p>
    <% if (seconds % 2===0) { %>
    <ul>
      <!-- List goes here if current second is even. -->
      <%items.forEach((fruit)=> { %>
      <li><%=fruit %></li>
      <%}) %>
      <!-- Otherwise it should display the following: -->
      <!-- <p>No items to display</p> -->
    </ul>
    <% } else {%>
    <p>No items to display</p>
    <% } %>
    <p>
      <!-- HTML content goes here -->
      <%- htmlContent %>
    </p>

    <!-- Footer goes here -->
    <%- include("footer.ejs") %>
  </body>
</html>
```
