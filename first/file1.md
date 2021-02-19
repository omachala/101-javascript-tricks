# File 1

## Example Title

This is some example description

```js
  for (const [groupName, images] of Object.entries(groups)) {
    const groupDone = output.findIndex((g) => g.groupName === groupName) >= 0;
    if (groupDone) {
      console.log(`Group ${groupName} already done`)
      continue;
    }
    console.log(`\nprocessing: ${groupName}`);
    const results = await processGroup(
      images.map(([name, url]) => ({ name, url }))
    );
    output.push({ groupName, results });
    fs.writeFileSync(outputFile, JSON.stringify(output, null, 2));
  }
```
