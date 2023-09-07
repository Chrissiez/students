---
title: JS Output w/ jquery
toc: True
description: Notes on using html and javascript to create tables
courses: {'compsci': {'week': 1}}
type: hacks
---

### Markdown Table
Use [markdown cheat sheet](https://www.markdownguide.org/extended-syntax/#tables) and it will show you an outline for a basic table

| Syntax | Description |
| ----------- | ----------- |
| Header | Title |
| Paragraph | Text |

### HTML Table
Google [w3schools html table](https://www.w3schools.com/html/html_tables.asp) and it will lead you to a tutorial on how to make tables.


```python
%%html

<h2>HTML Cell Output from Jupyter</h2>

<!-- Body contains the contents of the Document -->
<body>
    <table class="table">
        <thead>
            <tr>
                <th>Rank</th>
                <th>Name</th>
                <th>Team</th> 
                <th>Position</th>
                <th>Hitting Percentage</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>1</td>
                <td>Andi Jackson</td>
                <td>Nebraska</td>
                <td>MB</td>
                <td>.581</td>
            </tr>
            <tr>
                <td>2</td>
                <td>Lucia Scalamandre</td>
                <td>Princeton</td>
                <td>MB</td>
                <td>.568</td>
            </tr>
            <tr>
                <td>3</td>
                <td>Beau Vanderlann</td>
                <td>Brown</td>
                <td>MB</td>
                <td>.564</td>
            </tr>
            <tr>
                <td>4</td>
                <td>Khori Louis</td>
                <td>Florida St.</td>
                <td>MB</td>
                <td>.561</td>
            </tr>
            <tr>
                <td>5</td>
                <td>Kristen Erland</td>
                <td>Saint Mary's</td>
                <td>MB</td>
                <td>.548</td>
            </tr>
            <tr>
                <td>6</td>
                <td>Cara Cresse</td>
                <td>Louisville</td>
                <td>MB</td>
                <td>.547</td>
            </tr>
            <tr>
                <td>7</td>
                <td>Annamarie</td>
                <td>UIW</td>
                <td>MB</td>
                <td>.547</td>
            </tr>
            <tr>
                <td>8</td>
                <td>Alexia Kuehl</td>
                <td>Colorado</td>
                <td>MB</td>
                <td>.532</td>
            </tr>
            <tr>
                <td>9</td>
                <td>Claire Jeter</td>
                <td>Arizona St.</td>
                <td>MB</td>
                <td>.508</td>
            </tr>
            <tr>
                <td>10</td>
                <td>Courtney Okwara</td>
                <td>Buffalo</td>
                <td>MB</td>
                <td>.506</td>
            </tr>
            <tr>
                <td>11</td>
                <td>Madison Blane</td>
                <td>Liberty</td>
                <td>MB</td>
                <td>.506</td>                
            </tr>
            <tr>
                <td>12</td>
                <td>Magda Jehlarova</td>
                <td>Washington St.</td>
                <td>MB</td>
                <td>.500</td>                
            </tr>
            <tr>
                <td>13</td>
                <td>Eva Rohrbach</td>
                <td>Maryland</td>
                <td>MB</td>
                <td>.500</td>                
            </tr>
            <tr>
                <td>14</td>
                <td>Isabel Bennett</td>
                <td>Northern Colo.</td>
                <td>MB</td>
                <td>.491</td>                
            </tr>
            <tr>
                <td>15</td>
                <td>Becca Oldendorf</td>
                <td>UIC</td>
                <td>MB</td>
                <td>.489</td>                
            </tr>
            <tr>
                <td>16</td>
                <td>Tierney Barlow</td>
                <td>Wyoming</td>
                <td>OH</td>
                <td>.481</td>                
            </tr>
            <tr>
                <td>17</td>
                <td>Skyler Bumpers</td>
                <td>Mercer</td>
                <td>MB</td>
                <td>.473</td>                
            </tr>
            <tr>
                <td>18</td>
                <td>Kirah Johnson</td>
                <td>Delaware</td>
                <td>MB</td>
                <td>.471</td>                
            </tr>
            <tr>
                <td>19</td>
                <td>Emmy Ogogor</td>
                <td>Wake Forest</td>
                <td>MB</td>
                <td>.467</td>                
            </tr>
            <tr>
                <td>20</td>
                <td>Kiari Robey</td>
                <td>Florida St.</td>
                <td>MB</td>
                <td>.466</td>                
            </tr>
            <tr>
                <td>21</td>
                <td>Cara Lewis</td>
                <td>Virgina Tech</td>
                <td>MB</td>
                <td>.463</td>                
            </tr>
        </tbody>
    </table>
</body>
```

## HTML Table in Markdown Cell with JavaScript jquery
JavaScript is a programming language that works with HTML data, CSS helps to style that data.  In this example, we are using JavaScript and CSS that was developed by others (3rd party).  Addithing the 3rd party code makes the table interactive.
- Look at the href and src on lines inside of the lines in `<head>` tags.  This is adding code to our page from others.
- Observe the `<script>` tags at the bottom of the page.  This is generating the interactive table, from the third party code, using the data `<table id="demo">` from the `<body>`.  


<!-- Head contains information to Support the Document -->
<head>
    <!-- load jQuery and DataTables output style and scripts -->
    <link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/1.13.4/css/jquery.dataTables.min.css">
    <script type="text/javascript" language="javascript" src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script>var define = null;</script>
    <script type="text/javascript" language="javascript" src="https://cdn.datatables.net/1.13.4/js/jquery.dataTables.min.js"></script>
</head>

<!-- Body contains the contents of the Document -->
<body>
    <table id="md_demo" class="table">
        <thead>
            <tr>
                <th>Rank</th>
                <th>Name</th>
                <th>Team</th> 
                <th>Position</th>
                <th>Hitting Percentage</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>1</td>
                <td>Andi Jackson</td>
                <td>Nebraska</td>
                <td>MB</td>
                <td>.581</td>
            </tr>
            <tr>
                <td>2</td>
                <td>Lucia Scalamandre</td>
                <td>Princeton</td>
                <td>MB</td>
                <td>.568</td>
            </tr>
            <tr>
                <td>3</td>
                <td>Beau Vanderlann</td>
                <td>Brown</td>
                <td>MB</td>
                <td>.564</td>
            </tr>
            <tr>
                <td>4</td>
                <td>Khori Louis</td>
                <td>Florida St.</td>
                <td>MB</td>
                <td>.561</td>
            </tr>
            <tr>
                <td>5</td>
                <td>Kristen Erland</td>
                <td>Saint Mary's</td>
                <td>MB</td>
                <td>.548</td>
            </tr>
            <tr>
                <td>6</td>
                <td>Cara Cresse</td>
                <td>Louisville</td>
                <td>MB</td>
                <td>.547</td>
            </tr>
            <tr>
                <td>7</td>
                <td>Annamarie</td>
                <td>UIW</td>
                <td>MB</td>
                <td>.547</td>
            </tr>
            <tr>
                <td>8</td>
                <td>Alexia Kuehl</td>
                <td>Colorado</td>
                <td>MB</td>
                <td>.532</td>
            </tr>
            <tr>
                <td>9</td>
                <td>Claire Jeter</td>
                <td>Arizona St.</td>
                <td>MB</td>
                <td>.508</td>
            </tr>
            <tr>
                <td>10</td>
                <td>Courtney Okwara</td>
                <td>Buffalo</td>
                <td>MB</td>
                <td>.506</td>
            </tr>
            <tr>
                <td>11</td>
                <td>Madison Blane</td>
                <td>Liberty</td>
                <td>MB</td>
                <td>.506</td>                
            </tr>
            <tr>
                <td>12</td>
                <td>Magda Jehlarova</td>
                <td>Washington St.</td>
                <td>MB</td>
                <td>.500</td>                
            </tr>
            <tr>
                <td>13</td>
                <td>Eva Rohrbach</td>
                <td>Maryland</td>
                <td>MB</td>
                <td>.500</td>                
            </tr>
            <tr>
                <td>14</td>
                <td>Isabel Bennett</td>
                <td>Northern Colo.</td>
                <td>MB</td>
                <td>.491</td>                
            </tr>
            <tr>
                <td>15</td>
                <td>Becca Oldendorf</td>
                <td>UIC</td>
                <td>MB</td>
                <td>.489</td>                
            </tr>
            <tr>
                <td>16</td>
                <td>Tierney Barlow</td>
                <td>Wyoming</td>
                <td>OH</td>
                <td>.481</td>                
            </tr>
            <tr>
                <td>17</td>
                <td>Skyler Bumpers</td>
                <td>Mercer</td>
                <td>MB</td>
                <td>.473</td>                
            </tr>
            <tr>
                <td>18</td>
                <td>Kirah Johnson</td>
                <td>Delaware</td>
                <td>MB</td>
                <td>.471</td>                
            </tr>
            <tr>
                <td>19</td>
                <td>Emmy Ogogor</td>
                <td>Wake Forest</td>
                <td>MB</td>
                <td>.467</td>                
            </tr>
            <tr>
                <td>20</td>
                <td>Kiari Robey</td>
                <td>Florida St.</td>
                <td>MB</td>
                <td>.466</td>                
            </tr>
            <tr>
                <td>21</td>
                <td>Cara Lewis</td>
                <td>Virgina Tech</td>
                <td>MB</td>
                <td>.463</td>                
            </tr>
        </tbody>
    </table>
</body>

<!-- Script is used to embed executable code -->
<script>
    $("#md_demo").DataTable();
</script>


## Hacks
This lesson teaches you about tables.  In this hack, it is important that you analze the difference in the styles of output shown.  
- Make your own tables, with data according to your interests.
- Describe a benefit of a markdown table.
- Try to Style the HTML table using w3schools.
- Describe the difference between HTML and JavaScript.
- Describe a benefit of a table that uses JavaScript.

