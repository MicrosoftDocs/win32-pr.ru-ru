---
title: THEME. Опендиалог
description: Метод Опендиалог открывает диалоговое окно файла.
ms.assetid: d7f4549c-a5c3-4902-b13b-51f3d4444ea9
keywords:
- Проигрыватель Windows Media THEME. Опендиалог
topic_type:
- apiref
api_name:
- THEME.openDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79b9478b6b970b1d8d18b6f40975479e4755fa6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699286"
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

## <a name="remarks"></a>Комментарии

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
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент THEME**](theme-element.md)
</dt> </dl>

 

 





