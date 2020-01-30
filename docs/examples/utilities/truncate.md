---
wrapper_template: '_layouts/examples.html'
context:
  title: Truncate text
---

<table>
    <thead>
      <tr>
        <th>FQDN</th>
        <th>Status</th>
        <th class="u-align--right">RAM</th>
        <th class="u-align--right">Disks</th>
        <th class="u-align--right">Storage</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td class="u-truncate">NameLongEnoughToCauseOverflowAndRevealAnEllipsis</td>
        <td class="u-truncate">Failed to enter rescue mode</td>
        <td class="u-align--right">2 GiB</td>
        <td class="u-align--right">1</td>
        <td class="u-align--right">2TB</td>
      </tr>
      <tr>
          <td>
            <span>This sentence will wrap on multiple lines without truncating, while the following one will truncate once it reaches the end of the line.</span>
            <span class="u-truncate">
              This one will truncate when it reaches the end of the line
            </span>
          </td>
          <td>This text will not get truncated.</td>
          <td class="u-align--right">2 GiB</td>
          <td class="u-align--right">1</td>
          <td class="u-align--right">2TB</td>
        </tr>
    </tbody>
  </table>
  <p class="u-truncate">This sentence will truncate and reveal an ellipsis once it exceeds the paragraph's max-width.</p>