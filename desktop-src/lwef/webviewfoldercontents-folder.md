---
title: Свойство WebViewFolderContents.Folder (Shldisp.h)
description: Свойство Вебвиевфолдерконтентс. Folder — получает объект Folder, представляющий представление.
ms.assetid: 1d81c27a-1e48-4c0a-b74d-c63af43a909d
keywords:
- Свойства папки устаревшие возможности среды Windows
- Свойство папки устаревшие компоненты среды Windows, объект Вебвиевфолдерконтентс
- Объекты Вебвиевфолдерконтентс устаревшие компоненты среды Windows, свойство Folder
topic_type:
- apiref
api_name:
- WebViewFolderContents.Folder
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e88fd7a54971fa088bdddbc78d3d8df4af610875
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102702"
---
# <a name="webviewfoldercontentsfolder-property"></a>Вебвиевфолдерконтентс. Folder, свойство

Возвращает объект [**Folder**](../shell/folder.md) , представляющий представление.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
Folder = WebViewFolderContents.Folder
```



## <a name="property-value"></a>Значение свойства

Объект, получающий объект [**Folder**](../shell/folder.md) .

## <a name="examples"></a>Примеры

В следующем примере показано правильное использование этого свойства в JScript Embedded в HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFolderJ()
    {
        var objFolder;

        objFolder = FileList.Folder;
        if (objFolder != null)
        {
            alert(objFolder.Title);
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



 

