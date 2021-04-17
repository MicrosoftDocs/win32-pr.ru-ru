---
title: Свойство Вебвиевфолдерконтентс. script (Шлдисп. h)
description: Возвращает объект скрипта для представления.
ms.assetid: f65246c5-3cd6-43bd-b267-ad27bdd0b41e
keywords:
- Свойства скрипта устаревшие возможности среды Windows
- Свойство скрипта устаревшие компоненты среды Windows, объект Вебвиевфолдерконтентс
- Устаревшие компоненты среды Windows для объекта Вебвиевфолдерконтентс, свойство script
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
ms.openlocfilehash: 92133278d73851fa43353c116a2385da9b0fd3da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691912"
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

В следующем примере показано правильное использование этого свойства в JScript Embedded в HTML.


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

