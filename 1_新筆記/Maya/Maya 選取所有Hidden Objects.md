#### Python
```general
sel = cmds.ls(type = 'transform')
cmds.select(cl=1)

hiddenObjs = []

for i in sel:
    if (cmds.getAttr('%s.visibility'%i) == 0):
        hiddenObjs.append(i)
        
cmds.select(hiddenObjs)
```

