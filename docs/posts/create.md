---
meta_title: "Content Research for Contingency Planning for Internet Shutdown - Shutdown Contingency Framework"
title: "Content Research"
description: TBC 
cover: 
schema:
  -
    "@context": http://schema.org
    "@type": WebPage
    name: Needs Mapping for Contingency Planning for Internet Shutdown
    url: "./"
---
This framework provides activities that might be an organisation to curate a contingency plan. However, you don't have to conduct every activity listed here. It is flexible and scalable to accommodate organizations with low capacity. 

You can select which activities that you think are suitable for the orgnisation you work with and create a feasible timeframe for your training.


<!-- Activity List -->
<div class="activity-list">
    <div class="activity draggable" data-link="/posts/Template/questionnaire">Questionnaire</div>
    <div class="activity draggable" data-link="/posts/Template/context-Research">Context Research</div>
    <div class="activity draggable" data-link="/posts/Template/Impact-Cost-Matrix">Impact-Cost Matrix</div>
    <div class="activity draggable" data-link="/posts/Template/familiarisation">Tool Familiarisation Training</div>
    <div class="activity draggable" data-link="/posts/Template/Needs-Mapping">Needs Mapping</div>
</div>
<!-- Schedule Table -->
<h3>Training Timeline</h3>
<table class="schedule-table">
    <thead>
        <tr>
            <th>Item</th>
            <th>Activity</th>
            <th>Duration</th>
            <th>Start Date</th>
            <th>End Date</th>
        </tr>
    </thead>
    <tbody id="schedule-body">
        <!-- Users will drop items here -->
        <tr class="schedule-row">
            <td>1</td>
            <td class="dropzone">Drop activity here</td>
            <td><input type="text" class="duration-input" placeholder="Enter duration"></td>
            <td><input type="date" class="start-date-input"></td>
            <td><input type="date" class="end-date-input"></td>
        </tr>
        <tr class="schedule-row">
            <td>2</td>
            <td class="dropzone">Drop activity here</td>
            <td><input type="text" class="duration-input" placeholder="Enter duration"></td>
            <td><input type="date" class="start-date-input"></td>
            <td><input type="date" class="end-date-input"></td>
        </tr>
        <tr class="schedule-row">
            <td>3</td>
            <td class="dropzone">Drop activity here</td>
            <td><input type="text" class="duration-input" placeholder="Enter duration"></td>
            <td><input type="date" class="start-date-input"></td>
            <td><input type="date" class="end-date-input"></td>
        </tr>
        <tr class="schedule-row">
            <td>4</td>
            <td class="dropzone">Drop activity here</td>
            <td><input type="text" class="duration-input" placeholder="Enter duration"></td>
            <td><input type="date" class="start-date-input"></td>
            <td><input type="date" class="end-date-input"></td>
        </tr>
        <tr class="schedule-row">
            <td>5</td>
            <td class="dropzone">Drop activity here</td>
            <td><input type="text" class="duration-input" placeholder="Enter duration"></td>
            <td><input type="date" class="start-date-input"></td>
            <td><input type="date" class="end-date-input"></td>
        </tr>
        <tr class="schedule-row">
            <td>6</td>
            <td class="dropzone">Drop activity here</td>
            <td><input type="text" class="duration-input" placeholder="Enter duration"></td>
            <td><input type="date" class="start-date-input"></td>
            <td><input type="date" class="end-date-input"></td>
        </tr>
        <tr class="schedule-row">
            <td>7</td>
            <td class="dropzone">Drop activity here</td>
            <td><input type="text" class="duration-input" placeholder="Enter duration"></td>
            <td><input type="date" class="start-date-input"></td>
            <td><input type="date" class="end-date-input"></td>
        </tr>
    </tbody>
</table>

<script>
document.addEventListener("DOMContentLoaded", function() {
    const draggables = document.querySelectorAll(".draggable");
    const dropzones = document.querySelectorAll(".dropzone");

    draggables.forEach(item => {
        item.setAttribute("draggable", "true");
        item.addEventListener("dragstart", function(e) {
            e.dataTransfer.setData("text/plain", item.outerHTML);
        });
        item.addEventListener("click", function(e) {
    if (!e.defaultPrevented) {  // Ensure click works even after dragging
        window.location.href = item.getAttribute("data-link");
    }
});

    });

    dropzones.forEach(zone => {
        zone.addEventListener("dragover", function(e) {
            e.preventDefault();
        });
        zone.addEventListener("drop", function(e) {
            e.preventDefault();
            const activityHTML = e.dataTransfer.getData("text/plain");
            zone.innerHTML = activityHTML;
        });
    });
});
</script>

<style>
.activity-list {
    display: flex;
    gap: 10px;
    margin-bottom: 20px;
}
.draggable {
    padding: 10px;
    background-color: #f0f0f0;
    border: 1px solid #ccc;
    cursor: grab;
    display: inline-block;
}
.schedule-table {
    width: 100%;
    border-collapse: collapse;
}
.schedule-table th, .schedule-table td {
    border: 1px solid #ddd;
    padding: 10px;
    text-align: center;
}
.dropzone {
    min-height: 40px;
    background-color: #fafafa;
    border: 2px dashed #ccc;
    cursor: pointer;
}
.duration-input, .date-input {
    width: 120px;
    padding: 5px;
    text-align: center;
}
</style>