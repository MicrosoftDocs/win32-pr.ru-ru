---
title: Метод WebViewFolderContents.SelectedItems (Shldisp.h)
description: Вебвиевфолдерконтентс. SelectedItems, метод возвращает объект Фолдеритемс, представляющий все выбранные элементы в представлении.
ms.assetid: 683acac4-f157-4a75-a3f8-c693887c1ea5
keywords:
- Устаревшие функции среды Windows в методе SelectedItems
- Метод SelectedItems устаревшие функции среды Windows, объект Вебвиевфолдерконтентс
- Устаревшие функции среды Windows для объекта Вебвиевфолдерконтентс, метод SelectedItems
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectedItems
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a242991f6f9472610dffa20593f9cab5d8c310
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102652"
---
# <a name="webviewfoldercontentsselecteditems-method"></a>Вебвиевфолдерконтентс. SelectedItems, метод

Возвращает объект [**фолдеритемс**](../shell/folderitems.md) , представляющий все выбранные элементы в представлении.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = WebViewFolderContents.SelectedItems()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **фолдеритемс**](../shell/folderitems.md)\*\***

Ссылка на объект [**фолдеритемс**](../shell/folderitems.md) .

## <a name="examples"></a>Примеры

В следующем примере показано правильное использование этого метода для JScript Embedded в HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectedItemsJ()
    {
        var objFolderItems;

        objFolderItems = FileList.SelectedItems();
        if (objFolderItems != null)
        {
            alert(objFolderItems.Count);
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



 

