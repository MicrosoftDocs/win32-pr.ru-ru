---
title: Вебвиевфолдерконтентс. Селектитем, метод (Шлдисп. h)
description: Задает состояние выбора элемента в представлении.
ms.assetid: c0e163ee-1951-476c-807a-781e26766d99
keywords:
- Устаревшие функции среды Windows в методе Селектитем
- Метод Селектитем устаревшие функции среды Windows, объект Вебвиевфолдерконтентс
- Устаревшие функции среды Windows для объекта Вебвиевфолдерконтентс, метод Селектитем
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
ms.openlocfilehash: e491fb27db2d6e1e9b449be4aa2924684021539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710444"
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

Тип: **Variant \** _

Объект [_ *FolderItem* *](../shell/folderitem.md) , для которого будет задано состояние выбора.

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

В следующем примере показано правильное использование этого метода для JScript Embedded в HTML.


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
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

