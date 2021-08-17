---
title: Вебвиевфолдерконтентс. Селектитем, метод (Шлдисп. h)
description: Вебвиевфолдерконтентс. Селектитем, метод — задает состояние выбора элемента в представлении.
ms.assetid: c0e163ee-1951-476c-807a-781e26766d99
keywords:
- устаревшие функции Windows метода селектитем
- метод селектитем устаревшие функции среды Windows, объект вебвиевфолдерконтентс
- устаревшие компоненты Windows среды для объекта вебвиевфолдерконтентс, метод селектитем
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d144801e62962f4071b6c8e60147326908a9b4f7787e0d4ac549be9c51fa3c97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960624"
---
# <a name="webviewfoldercontentsselectitem-method"></a>Вебвиевфолдерконтентс. Селектитем, метод

Задает состояние выбора элемента в представлении.

## <a name="syntax"></a>Синтаксис


```JScript
WebViewFolderContents.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*витем* \[ окне\]
</dt> <dd>

Тип: **Variant \***

Объект [**FolderItem**](../shell/folderitem.md) , для которого будет задано состояние выбора.

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Тип: **Integer**

Набор флагов, указывающих новое состояние выбора. Это может быть одно или несколько из следующих значений.

<dt>



  (0)


</dt> <dd>

Отмените выбор элемента.

</dd> <dt>



 (1)


</dt> <dd>

Выберите элемент.

</dd> <dt>



 (3)


</dt> <dd>

Перевести элемент в режим редактирования.

</dd> <dt>



 (4)


</dt> <dd>

Отменить выбор всех элементов, кроме указанного.

</dd> <dt>



 (8)


</dt> <dd>

Убедитесь, что элемент отображается в представлении.

</dd> <dt>



 (16)


</dt> <dd>

Присвойте элементу фокус.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="examples"></a>Примеры

в следующем примере показано правильное использование этого метода для JScript, внедренного в HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            FileList.SelectItem(objFolderItem, 1);
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
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

