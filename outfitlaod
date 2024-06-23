function doGet(e) {
  var output;
  try
  {
    var query = e.parameter["q"];
    var response = UrlFetchApp.fetch(decodeURIComponent(query));
    output = {"result":"success", "response": JSON.parse(response.getContentText())};
  }
  catch(e)
  {
    output = {"result":"error", "error": "Unable to fetch"};
  }
  return ContentService.createTextOutput(JSON.stringify(output)).setMimeType(ContentService.MimeType.JSON);
}
