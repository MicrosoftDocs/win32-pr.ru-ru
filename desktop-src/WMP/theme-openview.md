---
title: THEME. openView
description: Метод openView открывает представление в новом окне.
ms.assetid: 2aa63c29-dafe-4942-a010-076f1503862b
keywords:
- проигрыватель Windows Media THEME. openView
topic_type:
- apiref
api_name:
- THEME.openView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e5dd33760cb86ef1f85f7efd8a3ff38cb36f0408076555e2fe8732ffb53779a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119466614"
---
# <a name="themeopenview"></a>THEME. openView

Метод **openView** открывает **представление** в новом окне.

``` syntax
        theme.openView(view)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="view"></span><span id="VIEW"></span>*режиме*
</dt> <dd>

**Строка** , указывающая **идентификатор** открываемого **представления** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="examples"></a>Примеры


```JScript
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openView('newView')"/>
    <TEXT top="30" value="close" 
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент THEME**](theme-element.md)
</dt> <dt>

[**THEME. closeView**](theme-closeview.md)
</dt> <dt>

[**THEME. Опенвиеврелативе**](theme-openviewrelative.md)
</dt> </dl>

 

 





