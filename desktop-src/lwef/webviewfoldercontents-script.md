---
title: Свойство Вебвиевфолдерконтентс. script (Шлдисп. h)
description: Возвращает объект скрипта для представления.
ms.assetid: f65246c5-3cd6-43bd-b267-ad27bdd0b41e
keywords:
- свойства скрипта устаревшие компоненты Windows среды
- свойство скрипта устаревшие компоненты Windows среды, объект вебвиевфолдерконтентс
- функции среды Windows для устаревших объектов вебвиевфолдерконтентс, свойство Script
topic_type:
- apiref
api_name:
- WebViewFolderContents.Script
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d214719e2e40eaa680786188cf4815623d915c1e1e70e36f94eb80b6c4a6c25b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975454"
---
# <a name="webviewfoldercontentsscript-property"></a>Вебвиевфолдерконтентс. script, свойство

Возвращает объект скрипта для представления.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
objScript = WebViewFolderContents.Script
```



## <a name="property-value"></a>Значение свойства

Переменная типа [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) , которая получает объект скрипта.

## <a name="examples"></a>Примеры

в следующем примере показано правильное использование этого свойства в JScript, внедренном в HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsScriptJ()
    {
        var objScript;

        objScript = FileList.Script;
        if (objScript != null)
        {
            alert(objScript.Name);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

