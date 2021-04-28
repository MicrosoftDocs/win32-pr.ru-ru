---
title: Вебвиевфолдерконтентс. Попупитеммену, метод (Шлдисп. h)
description: Вебвиевфолдерконтентс. Попупитеммену — создает контекстное меню для указанного элемента и возвращает выбранную командную строку.
ms.assetid: 3c07500c-2fe9-4976-a1a8-b128e75f9325
keywords:
- Устаревшие функции среды Windows в методе Попупитеммену
- Метод Попупитеммену устаревшие функции среды Windows, объект Вебвиевфолдерконтентс
- Устаревшие функции среды Windows для объекта Вебвиевфолдерконтентс, метод Попупитеммену
topic_type:
- apiref
api_name:
- WebViewFolderContents.PopupItemMenu
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c879e10097b334f0c2d4f98b1b76289d20ee4a93
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102642"
---
# <a name="webviewfoldercontentspopupitemmenu-method"></a>Вебвиевфолдерконтентс. Попупитеммену, метод

Создает контекстное меню для указанного элемента и возвращает выбранную командную строку.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = WebViewFolderContents.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*витем* \[ окне\]
</dt> <dd>

Тип: **Variant**

Объект [**FolderItem**](../shell/folderitem.md) , для которого будет создано контекстное меню.

</dd> <dt>

*VX* \[ в, необязательно\]
</dt> <dd>

Тип: **Variant**

Горизонтальное расположение меню в экранных координатах.

</dd> <dt>

*Ви* \[ в необязательное\]
</dt> <dd>

Тип: **Variant**

Вертикальное расположение меню в экранных координатах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[BSTR](/previous-versions/windows/desktop/automat/bstr)\***

При возврате из этого метода содержит командную строку.

## <a name="examples"></a>Примеры

В следующем примере показано правильное использование **попупитеммену** для JScript Embedded в HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsPopupItemMenuJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            var szCommand;

            szCommand = FileList.PopupItemMenu(objFolderItem);
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



 

