# Automation-Tasks
All of the Automation Tasks are provided here.

to use this automation, u just have to give the RSS link to the website or any category you want where the news is uploaded. you will upload the RSS link in RSS trigger node and all your work for news reading will be in the appended in the sheet and in summarized version, as well with some ipnortant insights of the news.

it also checks for the article to be not included in the sheet two times, against the title field.
my news format includes this structure:
{
  "Title": "",
  "Context/Problem": "",
  "The Innovation": "",
  "Key Features": [],
  "Applications": "",
  "Challenges": "",
  "Future Outlook": "",
  "Conclusion": ""
}
 you can add your own formate if you want if u need to add or remove any specific field to your own specific needs. you just have to open the "LLM basic chain" node to give the prompt you want from the news. and the "structure output parser" node you will enter that strucure you defined in the LLM node. 
