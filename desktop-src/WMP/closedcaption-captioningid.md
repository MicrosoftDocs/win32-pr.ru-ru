---
title: Клоседкаптион. Каптионингид
description: Свойство Каптионингид указывает или получает имя элемента, отображающего субтитры.
ms.assetid: 99d4aae3-485f-4c86-9130-101b1ca968e9
keywords:
- клоседкаптион. каптионингид проигрыватель Windows Media
topic_type:
- apiref
api_name:
- ClosedCaption.captioningID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1da667e5479cc33312375920c1d573f0e2c19607b2399ff6f4fe34b130ca61e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580992"
---
# <a name="closedcaptioncaptioningid"></a>Клоседкаптион. Каптионингид

Свойство **каптионингид** указывает или получает имя элемента, отображающего субтитры.

``` syntax
player.closedCaption.captioningID
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **строкой** для чтения и записи.

## <a name="remarks"></a>Remarks

Указанное имя элемента может быть любым HTML-элементом на веб-странице, если он поддерживает атрибут innerHTML. Если веб-страница содержит несколько кадров, имя элемента может ссылаться только на элемент в том же кадре, что и элемент управления проигрывателя.

**проигрыватель Windows Media 10 Mobile:** Это свойство доступно только для чтения и всегда возвращает пустую строку.

## <a name="examples"></a>Примеры

в следующем примере Microsoft JScript используется *клоседкаптион*. **каптионингид** , чтобы выбрать область веб-страницы, используемую для вывода субтитров. Были созданы два элемента HTML DIV с ИДЕНТИФИКАТОРом = CC1 и ID = CC2 соответственно. Объект **Player** создан с идентификатором "Player".


```JScript
<!-- Create two HTML BUTTON elements to allow the user to choose a display region. -->
<INPUT TYPE = "BUTTON"  NAME = "SET1"  VALUE = "Move Caption to CC1"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC2.innerHTML = 'This is the CC2 DIV';

           /* Show the captions in the DIV named CC1. */ 
           Player.ClosedCaption.captioningID = 'CC1';
          ">

<INPUT TYPE = "BUTTON" NAME = "SET2" VALUE = "Move Caption to CC2"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC1.innerHTML = 'This is the CC1 DIV';

           /* Show the captions in the DIV named CC2. */
           Player.ClosedCaption.captioningID = 'CC2';
          ">

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Добавление субтитров к цифровым носителям**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Объект Клоседкаптион**](closedcaption-object.md)
</dt> </dl>

 

 





