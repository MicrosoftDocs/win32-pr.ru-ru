---
title: Свойство Вебвиевфолдерконтентс. Виевоптионс (Шлдисп. h)
description: Возвращает набор флагов Шеллфолдервиевоптионс, которые указывают текущие параметры представления.
ms.assetid: 96edb144-e532-4ab5-99ae-d945e211d744
keywords:
- свойства виевоптионс устаревшей среды Windows
- свойства виевоптионс устаревшей среды Windows, объект вебвиевфолдерконтентс
- функции среды Windows вебвиевфолдерконтентс объектов прежних версий, свойство виевоптионс
topic_type:
- apiref
api_name:
- WebViewFolderContents.ViewOptions
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c897c75eab32962a18981c605c8465630aaf7b0c6b7d3e3f9a4fbe8e3d75d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607744"
---
# <a name="webviewfoldercontentsviewoptions-property"></a>Вебвиевфолдерконтентс. Виевоптионс, свойство

Возвращает набор флагов [**шеллфолдервиевоптионс**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) , которые указывают текущие параметры представления.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
objViewOptions = WebViewFolderContents.ViewOptions
```



## <a name="property-value"></a>Значение свойства

Переменная типа [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) , которая получает объект параметров представления.

## <a name="examples"></a>Примеры

в следующем примере показано правильное использование этого свойства в JScript, внедренном в HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsViewOptionsJ()
    {
        var nViewOptions;

        nViewOptions = FileList.ViewOptions;
        if (nViewOptions != "")
        {
            alert(nViewOptions);
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



 

