---
description: Шеллфолдервиев. Селектитем, метод — задает состояние выбора элемента в представлении.
title: Шеллфолдервиев. Селектитем, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.SelectItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91c39d4c-56c3-4c2b-93e8-9f782ca0aa93
ms.openlocfilehash: c8cbff0da4da55d9621bfeb01f26c5ed62fe230a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116752"
---
# <a name="shellfolderviewselectitem-method"></a>Шеллфолдервиев. Селектитем, метод

Задает состояние выбора элемента в представлении.

## <a name="syntax"></a>Синтаксис


```JScript
ShellFolderView.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*витем* \[ окне\]
</dt> <dd>

Тип: **Variant \***

Объект [**FolderItem**](folderitem.md) , для которого будет задано состояние выбора.

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

## <a name="remarks"></a>Remarks

[**Фокуседитем**](shellfolderview-focuseditem.md) может быть вызван только в локальной системе. Он не будет работать при запуске на веб-странице по протоколу HTTP или UNC.

## <a name="examples"></a>Примеры

В следующем примере показано правильное использование этого метода в JScript Embedded в HTML.


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewSelectItemJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.Self;
            if (objFolderItem != null)
            {
                WebOC.Document.SelectItem(objFolderItem, 16);
                alert("item selected");
            }
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC"
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400>
</object>
<br><br>
<INPUT id=SelectItem 
       type=button 
       value=SelectItem 
       name=SelectItem 
       onclick="fnShellFolderViewSelectItemJ()">
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



 

 




