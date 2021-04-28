---
title: Свойство Вебвиевфолдерконтентс. Фокуседитем (Шлдисп. h)
description: Вебвиевфолдерконтентс. Фокуседитем Property — возвращает объект FolderItem, представляющий элемент, имеющий фокус ввода.
ms.assetid: 84cf92ac-dadb-4741-8383-a8ae1d35d4e0
keywords:
- Свойства Фокуседитем устаревшие функции среды Windows
- Свойства Фокуседитем устаревшие функции среды Windows, объект Вебвиевфолдерконтентс
- Функции среды Windows для устаревшего объекта Вебвиевфолдерконтентс, свойство Фокуседитем
topic_type:
- apiref
api_name:
- WebViewFolderContents.FocusedItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 724743b81f605dc9ba5794a4a796b8a0c4a2a03f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102732"
---
# <a name="webviewfoldercontentsfocuseditem-property"></a>Вебвиевфолдерконтентс. Фокуседитем, свойство

Возвращает объект [**FolderItem**](../shell/folderitem.md) , представляющий элемент, имеющий фокус ввода.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
objFocusedItem = WebViewFolderContents.FocusedItem
```



## <a name="property-value"></a>Значение свойства

Переменная типа [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) , получающая объект элемента с сортировкой.

## <a name="examples"></a>Примеры

В следующем примере показано правильное использование этого свойства в JScript Embedded в HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFocusedItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            alert(objFolderItem.Name);
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



 

