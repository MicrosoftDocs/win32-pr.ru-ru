---
title: THEME. Опендиалог
description: Метод Опендиалог открывает диалоговое окно файла.
ms.assetid: d7f4549c-a5c3-4902-b13b-51f3d4444ea9
keywords:
- проигрыватель Windows Media THEME. опендиалог
topic_type:
- apiref
api_name:
- THEME.openDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d57218105aa081ddebcb98fadbdb40b4bbd42511de9df94e204320ce78cf03c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134557"
---
# <a name="themeopendialog"></a>THEME. Опендиалог

Метод **опендиалог** открывает диалоговое окно файла.

``` syntax
        theme.openDialog(dialogType, parameters)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*диалогтипе*
</dt> <dd>

**Строка** , указывающая тип диалогового окна. Необходимо задать значение "открыть файл \_ ".

</dd> <dt>

<span id="parameters"></span><span id="PARAMETERS"></span>*Вход*
</dt> <dd>

**Строка** , которую можно использовать для получения дополнительных сведений. Необходимо задать значение FILEs \_ аллмедиа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **строку** , содержащую URL-адрес выбранного файла, или "" (пустая строка), если пользователь нажимает кнопку "Отмена".

## <a name="remarks"></a>Remarks

Этот метод можно использовать для файлов на локальных жестких дисках или на сетевых дисках.

## <a name="examples"></a>Примеры


```JScript
<THEME>
  <VIEW id="View1" 
    backgroundImage="greenstone.bmp" 
    width=500 height=300 author="Microsoft Corp.">
    <BUTTON 
      id="Open" 
      image="Open.png" 
      onclick="jscript:
        player.URL = theme.openDialog('FILE_OPEN','FILES_ALLMEDIA')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент THEME**](theme-element.md)
</dt> </dl>

 

 





