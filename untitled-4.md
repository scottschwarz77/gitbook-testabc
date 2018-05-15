# Untitled10





1. First, render the header template. This is template is shown on all pages. The header template usually contains the main menu. The header template may contain widgets, which are helper components that the body template calls.

When a user makes a URL request to a web site running Frameplicity, the framework constructs the result page by applying the header, body and footer templates to one or more pages. These templates are explained below.

Frameplicity renders a page while processing it. Below is a high-level explanation of how page rendering works.  
  
 ![](https://scottschwarz77.gitbooks.io/how-to-write-large-programs/content/assets/fp-renderpage.png)

**  
**

In the `NextPreviousPageWidget.php` file that you create, add this function, which displays a button and creates spacing between buttons:

```text
private function createButton($page,$text) {
    emit("<a class='button' href=".$page->getURL().">".$text."</a>");
}

private function createSpacing() {
    emit("&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;");
}
```

In NextPreviousPageWidget.php, you will need to use some functions from the Folder class, located in `NextPreviousPage/_Source/Folder.php`. Refer to `NextPreviousPage/Widgets/PageListWidget.php` as an example for using the Folder class.

