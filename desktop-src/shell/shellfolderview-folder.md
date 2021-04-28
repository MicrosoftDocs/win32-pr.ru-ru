---
description: Свойство Шеллфолдервиев. Folder — получает объект Folder, представляющий представление.
ms.assetid: 8f3e7827-f2a0-4ce9-b3e9-e6316ec58863
title: Свойство Шеллфолдервиев. Folder (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Folder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 370fddc1428c8f77edb77cdac2dc04123fc5211f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083422"
---
# <a name="shellfolderviewfolder-property"></a>Шеллфолдервиев. Folder, свойство

Возвращает объект [**Folder**](folder.md) , представляющий представление.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
Folder = ShellFolderView.Folder
```



## <a name="property-value"></a>Значение свойства

Объект, получающий объект [**Folder**](folder.md) .

## <a name="remarks"></a>Remarks

**Папка** может быть вызвана только в локальной системе. Он не будет работать при запуске на веб-странице по протоколу HTTP или UNC.

## <a name="examples"></a>Примеры

В следующем примере показано правильное использование этого свойства для JScript Embedded в HTML.


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewFolderJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            alert("Got Folder object");
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC" 
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400 VIEWASTEXT>
</object>
<br><br>
<INPUT id=Folder 
       type=button 
       value=Folder 
       name=Folder 
       onclick="fnShellFolderViewFolderJ()">
</body>
</html>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

 




