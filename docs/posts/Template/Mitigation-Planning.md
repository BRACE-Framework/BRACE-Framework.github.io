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
## Needs Mapping

There are several factors that must be taken into consideration.

- **Needs**: Identify the daily and weekly tasks that must be maintained. For example:
  - Journalists need to publish updates on elections and protests.
  - Human rights advocates focus on mitigation planning.

- **Workflow**: Break down the workflow step by step to identify alternative solutions.

- **Interference**: Assess how shutdowns can impact the ability to achieve usual work objectives.

- **Risk**: Evaluate the risks involved in each workflow step and the potential suggested mitigations.

- **Cost**: Determine the financial, time, and manpower costs involved, and assess whether the organization is willing and capable of meeting these requirements.


Determine how an internet shutdown would interfere with these tasks, including related risks such as increased police searchesIdentify the specific tasks that must be completed (e.g. publishing three articles online)
Propose possible workarounds
- Find countermeasures or circumvention strategies for each suggestion, if available; if not, suggest alternative options.
- Draft a mitigation workflow to be followed during an internet shutdown


<h2>📝 Editable Risk Assessment Table</h2>
<p>Fill in the table below with relevant details.</p>

<table id="editable-table">
    <thead>
        <tr>
            <th>#</th>
            <th>Goal</th>
            <th>What procedures/ data are involved?</th>
            <th>Who is involved?</th>
            <th>What risks or constraints will they encounter?</th>
            <th>How likely the risk is going to happen?</th>
            <th>Current circumvention method</th>
            <th>Potential circumvention</th>
            <th>Any possible risk?</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td contenteditable="true"rowspan="3">1</td>
            <td contenteditable="true"rowspan="3"><b>Publish news</b></td>
            <td contenteditable="true">Video footage from live coverage</td>
            <td contenteditable="true">Reporter</td>
            <td contenteditable="true">Device/SD card confiscation</td>
            <td contenteditable="true">High</td>
            <td contenteditable="true">None</td>
            <td contenteditable="true">Tella app</td>
            <td contenteditable="true">Device investigation</td>
        </tr>
        <tr>
            <td contenteditable="true"></td>
            <td contenteditable="true"></td>
            <td contenteditable="true">Receiving footage/photos from whistleblowers</td>
            <td contenteditable="true">Citizens/activists</td>
            <td contenteditable="true">Lack of ways to transfer files without internet</td>
            <td contenteditable="true">High</td>
            <td contenteditable="true">None</td>
            <td contenteditable="true">VPN</td>
            <td contenteditable="true">Is VPN legal?</td>
        </tr>
        <tr>
            <td contenteditable="true"></td>
            <td contenteditable="true"></td>
            <td contenteditable="true"></td>
            <td contenteditable="true"></td>
            <td contenteditable="true">Surveillance</td>
            <td contenteditable="true">Medium</td>
            <td contenteditable="true">Use Signal</td>
            <td contenteditable="true">Face-to-face handing over a USB drive</td>
            <td contenteditable="true">Manpower problem / Possibility of an undercover cop</td>
        </tr>
        <tr>
            <td contenteditable="true"rowspan="3">2</td>
            <td contenteditable="true"rowspan="3"><b>Reach audience</b></td>
            <td contenteditable="true">Audience having access to our content</td>
            <td contenteditable="true">Editor</td>
            <td contenteditable="true"></td>
            <td contenteditable="true"></td>
            <td contenteditable="true"></td>
            <td contenteditable="true"></td>
            <td contenteditable="true"></td>
        </tr>
        <tr>
            <td contenteditable="true"></td>
            <td contenteditable="true"></td>
            <td contenteditable="true"></td>
            <td contenteditable="true">Audience</td>
            <td contenteditable="true"></td>
            <td contenteditable="true"></td>
            <td contenteditable="true"></td>
            <td contenteditable="true"></td>
            <td contenteditable="true"></td>
        </tr>
    </tbody>
</table>

<button onclick="saveTable()">💾 Save Table</button>

<script>
    function saveTable() {
        let table = document.getElementById("editable-table");
        let rows = table.getElementsByTagName("tr");
        let data = [];

        for (let i = 1; i < rows.length; i++) {
            let cells = rows[i].getElementsByTagName("td");
            let rowData = Array.from(cells).map(cell => cell.innerText);
            data.push(rowData);
        }

        localStorage.setItem("editableRiskTable", JSON.stringify(data));
        alert("✅ Table saved! (It will stay even after refresh)");
    }

    window.onload = function() {
        let savedData = localStorage.getItem("editableRiskTable");
        if (savedData) {
            let data = JSON.parse(savedData);
            let table = document.getElementById("editable-table").getElementsByTagName("tbody")[0];
            table.innerHTML = "";

            data.forEach(row => {
                let newRow = table.insertRow();
                row.forEach((value, index) => {
                    let cell = newRow.insertCell(index);
                    cell.contentEditable = "true";
                    cell.innerText = value;
                });
            });
        }
    }
</script>

<style>
    :root {
        --pearl: #f5f1e0;
        --vanilla: #eceecc;
        --cambridge-blue: #b5cfc2;
        --air-superiority-blue: #a0c5da;
        --blue-munsell: #52aac6;
    }

    table {
        width: 100%;
        border-collapse: collapse;
        margin-top: 10px;
    }
    th, td {
        border: 1px solid var(--cambridge-blue);
        padding: 8px;
        text-align: center;
    }
    th {
        background-color: var(--blue-munsell);
        color: white;
    }
    td {
        background-color: var(--pearl);
    }
    td[contenteditable="true"] {
        background-color: white;
    }
    button {
        margin-top: 10px;
        padding: 10px;
        background-color: var(--air-superiority-blue);
        color: white;
        border: none;
        cursor: pointer;
        font-size: 16px;
        border-radius: 5px;
    }
    button:hover {
        background-color: var(--vanilla);
    }
</style>



