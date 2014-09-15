jquery-mobile-dynamic-custom-alert-confirm-prompt-dialog
================================================

A custom dialog box for alert, confirm, prompt actions based on jquery mobile, compatible with custom jquery themes.

Example in plunker http://plnkr.co/edit/PKz1SK?p=preview

============================
Dependencies : 
=============================

1 : jquery
2 : jquery mobile

=========================
Features : 
=========================

Create dynamic dialogs boxes without worrying about writing code in HTML.
Create html markup and add events dynamically.
The html markup and events are removed once dialog is closed.
Supports the jquery mobile theme roller
Easy to use

==================================================
HTML

  &lt;input type="button" value="Alert Box" id="jqmAlert" /&gt;
  &lt;input type="button" value="Confirm Box" id="jqmConfirm" /&gt;
  &lt;input type="button" value="Prompt Box" id="jqmPrompt" /&gt;
  
==================================================
Jquery

      //All parameters are mandatory

      $('#jqmAlert').on('click', function() {
        
        //parameters are message, heading
        
        $.jAlert("I am an ALert Box", "Alert");
      });

      $('#jqmConfirm').on('click', function() {
        
        //parameters are message, heading, callback
        
        $.jConfirm("I am an Confirm Box", "Confirm",function(result){
          $.jAlert("Result is : " + result, "Alert");
        });
      });

      $('#jqmPrompt').on('click', function() {
        
        //parameters are message, initial value, heading, callback
        
        $.jPrompt("I am an Prompt Box","", "Prompt",function(result){
          $.jAlert("Result is : " + result, "Alert");
        });
      });
