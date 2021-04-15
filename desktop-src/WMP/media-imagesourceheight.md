---
title: Media. Имажесаурцехеигхт
description: Свойство Имажесаурцехеигхт извлекает высоту текущего элемента мультимедиа в пикселях.
ms.assetid: fa98ec62-4c58-46ab-98f3-8017096d46d8
keywords:
- Media. Имажесаурцехеигхт проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Media.imageSourceHeight
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de364243e71c6653085b4c9c9ff81f148dc299d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695205"
---
# <a name="mediaimagesourceheight"></a>Media. Имажесаурцехеигхт

Свойство **имажесаурцехеигхт** извлекает высоту текущего элемента мультимедиа в пикселях.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *куррентмедиа*. **имажесаурцехеигхт**

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="remarks"></a>Комментарии

Если элемент мультимедиа не является текущим, это свойство возвращает ноль.

Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

В следующем примере на языке JScript используется *Media*. имажесаурцехеигхт для вывода размера изображения (в пикселях) текущего элемента мультимедиа. Сведения выводятся в HTML-элемент TEXTAREA с именем Видеосизе. Объект **Player** создан с идентификатором "Player".


```JScript
<!-- Create an event handler to refresh the information when the current media changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Store the height and width of the new media item.
   var Height = Player.currentMedia.imageSourceHeight;
   var Width =  Player.currentMedia.imageSourceWidth;

   // Erase the information in the text area.
   VideoSize.value = "";

   // Test whether an image is visible.
   if (Height != 0 && Width != 0)

      // Display the image size information.
      VideoSize.value = Width + " x " + Height;
}
</SCRIPT>

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

[**Player. Куррентмедиа**](player-currentmedia.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





