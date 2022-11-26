---
title: "Mailinator.com Websocket Api"
date: "2017-09-02"
categories: 
  - "coding"
  - "hacking"
  - "programming"
---

https://mailinator.com/v2/js/m8r.js?887

var prefix='ws' h=window.location.host appen='?zone=public&query=arjunbahl1910' ws = new WebSocket(prefix + "://" + h + "/ws/fetchinbox" + appen);

f={} f\['zone'\]='public' f\['cmd'\]='sub' ws.send(JSON.stringify(f))

 

 

def on\_message(ws, message): #text.insert(END, message+"\\n") print "Received: "+message return

def on\_error(ws, error): #text.insert(END, error+"\\n") print error return

def on\_close(ws): #text.insert(END, "### closed ###\\n") print "### closed ###" return

def on\_open(ws): ws.send(raw\_input(':')) #ws.send("test") return

websocket.enableTrace(True) ws = websocket.WebSocketApp("ws://www.mailinator.com/ws/fetchinbox?zone=public&query=arjunbahl1910", on\_message = on\_message, on\_error = on\_error, on\_close = on\_close) ws.on\_open = on\_open
