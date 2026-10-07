# menu
[gemini-code-1791354469312.js](https://github.com/user-attachments/files/33142708/gemini-code-1791354469312.js)
function doPost(e) {
  var sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
  var data = JSON.parse(e.postData.contents);
  
  sheet.appendRow([
    data.time,
    data.table,
    data.items,
    data.total,
    data.note
  ]);
  
  return ContentService.createTextOutput("Success").setMimeType(ContentService.MimeType.TEXT);
}
