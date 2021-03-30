---
title: Свойство Вебвиевфолдерконтентс. Виевоптионс (Шлдисп. h)
description: Возвращает набор флагов Шеллфолдервиевоптионс, которые указывают текущие параметры представления.
ms.assetid: 96edb144-e532-4ab5-99ae-d945e211d744
keywords:
- Свойства Виевоптионс устаревшие функции среды Windows
- Свойства Виевоптионс устаревшие функции среды Windows, объект Вебвиевфолдерконтентс
- Функции среды Windows для устаревшего объекта Вебвиевфолдерконтентс, свойство Виевоптионс
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
ms.openlocfilehash: 737ec5cb22fdc5c0002006898b837b557b5f6089
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071210"
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

В следующем примере показано правильное использование этого свойства в JScript Embedded в HTML.


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

