---
title: Media. Аттрибутекаунт
description: Свойство Аттрибутекаунт извлекает количество атрибутов, которые могут быть запрошены или заданы для элемента мультимедиа.
ms.assetid: d2a5286f-dde1-48b5-b486-6cee1be463f9
keywords:
- Media. Аттрибутекаунт проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Media.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df4979f670cdd6a79b1b309bc3eceff5a2798223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708451"
---
# <a name="mediaattributecount"></a>Media. Аттрибутекаунт

Свойство **аттрибутекаунт** извлекает количество атрибутов, которые могут быть запрошены или заданы для элемента мультимедиа.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *куррентмедиа*. **аттрибутекаунт**

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="remarks"></a>Комментарии

Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.

**Проигрыватель Windows Media 10 Mobile:** Атрибуты для элемента мультимедиа доступны только во время воспроизведения, если они не извлекаются из элемента через коллекцию мультимедиа.

## <a name="examples"></a>Примеры

В следующем примере JScript используется *носитель*. **аттрибутекаунт** для определения количества атрибутов, доступных в текущем элементе мультимедиа. Код использует это значение для печати списка имен и значений атрибутов в текстовой области HTML с именем myText. Объект **Player** создан с идентификатором "Player".


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Create arrays to hold each attribute name and value.
var atNames = new Array();
var atValues = new Array();

// Loop through the attribute list.   
for(var i = 0; i < cm.attributeCount; i++){

   // Fill the arrays with the attribute info.
   atNames[i] = cm.getAttributeName(i);
   atValues[i] = cm.getItemInfo(atNames[i]);

   // Print the attribute information to the text area.
   myText.value += atNames[i] + ": " + atValues[i];
   myText.value += "\n";
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект мультимедиа**](media-object.md)
</dt> <dt>

[**Media. Жетаттрибутенаме**](media-getattributename.md)
</dt> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





