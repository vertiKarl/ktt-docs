---
title: Über uns
type: about
---

Auf dieser Webseite geht es um das [Trouble in Terrorist Town](https://www.troubleinterroristtown.com/) Projekt welches von [@vertiKarl](https://discord.com/users/175642620767371265) gehostet wird.

## Server Admins

{{< cards >}}
{{< card link="vertikarl" title="vertiKarl" image="https://avatars.githubusercontent.com/u/39246384">}}
{{< card link="gapls" title="GAPLS" image="https://avatars.githubusercontent.com/u/125091918">}}
{{< /cards >}}

## GitHub Contributors (Docs)

<div id="contributors" class="loader"></div>

<script>
    async function getContributors() {
        const container = document.getElementById('contributors');
        if(!container) return;

        const res = await fetch("https://api.github.com/repos/vertikarl/ktt-docs/contributors");
        const body = await res.json();

        const table = document.createElement("table");
        const tableHead = document.createElement("thead");
        tableHead.innerHTML = `<tr>
                <th>User</th>
                <th>Contributions</th>
            </tr>`
        const tableBody = document.createElement("tbody");

        body.forEach(user => {
            const row = document.createElement('tr');
            row.innerHTML = `
                <td>
                    <a href="${user.html_url}" target="_blank" style="display: flex; align-items: center; gap: 10px;">
                        <img src="${user.avatar_url}" alt="${user.login}" width="30" height="30" style="border-radius: 50%;">
                        ${user.login}
                    </a>
                </td>
                <td>${user.contributions}</td>`

            tableBody.appendChild(row);
        });
        table.append(tableHead);
        table.append(tableBody);
        container.append(table);

        container.outerHTML = container.innerHTML; // replace container with its content
    }

    getContributors();
</script>

<style>
    /* https://www.w3schools.com/howto/howto_css_loader.asp */
    .loader {
        border: 16px solid #f3f3f3; /* Light grey */
        border-top: 16px solid #3498db; /* Blue */
        border-radius: 50%;
        width: 120px;
        height: 120px;
        animation: spin 2s linear infinite;
    }

    @keyframes spin {
        0% { transform: rotate(0deg); }
        100% { transform: rotate(360deg); }
    }
</style>
