let newWin = window.open("about:blank", "Mathhelp", "width=200,height=200");

fetch('[https://raw.githubusercontent.com/USERNAME/REPO_NAME/BANCH_NAME/FILE_NAME.html](https://raw.githubusercontent.com/Nedearb/Mathhelp/main/index.html)')
  .then(response => response.text())
  .then(data => {
    newWin.document.write(data + "<script>window.opener.document.body.innerHTML = 'Test'<\/script>")
  })
