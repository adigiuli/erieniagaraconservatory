<!DOCTYPE html>
<html>
<head>
    <title>Niagara Conservatory Timeline</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/vis/4.21.0/vis.min.js"></script>
    <style>
        #timeline {
            width: 100%;
            height: 500px;
            border: 1px solid lightgray;
        }
    </style>
</head>
<body>

<h2 style="text-align:center;">Niagara Conservatory Development Timeline</h2>

<div id="timeline"></div>

<script>
    var container = document.getElementById("timeline");

    var items = new vis.DataSet([
        { id: 1, content: "Foundation & Launch", start: "2025-01-01", end: "2027-12-31", group: 1 },
        { id: 2, content: "Pre-College Expansion", start: "2028-01-01", end: "2030-12-31", group: 2 },
        { id: 3, content: "Degree Program Development", start: "2031-01-01", end: "2033-12-31", group: 3 },
        { id: 4, content: "Accreditation & Bachelor's Degrees", start: "2034-01-01", end: "2036-12-31", group: 4 },
        { id: 5, content: "Graduate Programs", start: "2037-01-01", end: "2039-12-31", group: 5 },
        { id: 6, content: "Full Higher Ed Institution", start: "2040-01-01", end: "2042-12-31", group: 6 },
        { id: 7, content: "World-Class Conservatory", start: "2043-01-01", end: "2045-12-31", group: 7 }
    ]);

    var groups = new vis.DataSet([
        { id: 1, content: "Phase 1" },
        { id: 2, content: "Phase 2" },
        { id: 3, content: "Phase 3" },
        { id: 4, content: "Phase 4" },
        { id: 5, content: "Phase 5" },
        { id: 6, content: "Phase 6" },
        { id: 7, content: "Phase 7" }
    ]);

    var options = {
        stack: false,
        start: "2025-01-01",
        end: "2045-12-31",
        editable: false,
        margin: { item: 10 },
        zoomable: true,
    };

    var timeline = new vis.Timeline(container, items, groups, options);
</script>

</body>
</html>
