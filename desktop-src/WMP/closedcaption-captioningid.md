---
title: Клоседкаптион. Каптионингид
description: Свойство Каптионингид указывает или получает имя элемента, отображающего субтитры.
ms.assetid: 99d4aae3-485f-4c86-9130-101b1ca968e9
keywords:
- Проигрыватель Windows Media Клоседкаптион. Каптионингид
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
ms.openlocfilehash: faadae626dd5ac0314c4140e3f9d82ab645ef9b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694377"
---
# <a name="closedcaptioncaptioningid"></a>Клоседкаптион. Каптионингид

Свойство **каптионингид** указывает или получает имя элемента, отображающего субтитры.

``` syntax
player.closedCaption.captioningID
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **строкой** для чтения и записи.

## <a name="remarks"></a>Комментарии

Указанное имя элемента может быть любым HTML-элементом на веб-странице, если он поддерживает атрибут innerHTML. Если веб-страница содержит несколько кадров, имя элемента может ссылаться только на элемент в том же кадре, что и элемент управления проигрывателя.

**Проигрыватель Windows Media 10 Mobile:** Это свойство доступно только для чтения и всегда возвращает пустую строку.

## <a name="examples"></a>Примеры

В следующем примере Microsoft JScript используется *клоседкаптион*. **каптионингид** , чтобы выбрать область веб-страницы, используемую для вывода субтитров. Были созданы два элемента HTML DIV с ИДЕНТИФИКАТОРом = CC1 и ID = CC2 соответственно. Объект **Player** создан с идентификатором "Player".


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
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Добавление субтитров к цифровым носителям**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Объект Клоседкаптион**](closedcaption-object.md)
</dt> </dl>

 

 





