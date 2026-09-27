# Summarizer-api

from anthropic import Anthropic

client = Anthropic()
reponse  = client.messages.create( model="claude-sonnet-4-5" , max_tokens=1000 , 
system="you summarize product review in one short sentence" ,
messages=[{"role": "user" , "content": "The product arrived late but works great once i set it up."}])

print (response.content[0].text)
