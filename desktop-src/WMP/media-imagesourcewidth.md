---
title: Media. Имажесаурцевидс
description: Свойство Имажесаурцевидс извлекает ширину текущего элемента мультимедиа в пикселях.
ms.assetid: 6559bd51-cec2-4fc6-aab8-f2fdd1d59bae
keywords:
- проигрыватель Windows Media Media. имажесаурцевидс
topic_type:
- apiref
api_name:
- Media.imageSourceWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710b6f0d91d7d734b12ad75f201fcd45037f67adf2c8ed3cb60f3ee5fcf6c222
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508404"
---
# <a name="mediaimagesourcewidth"></a>Media. Имажесаурцевидс

Свойство **имажесаурцевидс** извлекает ширину текущего элемента мультимедиа в пикселях.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *куррентмедиа*. **имажесаурцевидс**

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="remarks"></a>Remarks

Если элемент мультимедиа не является текущим, это свойство возвращает ноль.

Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

в следующем примере JScript используется *носитель*. **имажесаурцевидс** для вывода размера изображения (в пикселях) **текущего элемента мультимедиа. Сведения выводятся в HTML-элемент TEXTAREA с именем Видеосизе. Объект Player** создан с идентификатором "Player".


```JScript
<!-- Create an event handler to refresh the information when the current media changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player"  EVENT = OpenStateChange(NewState)>

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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект мультимедиа**](media-object.md)
</dt> <dt>

[**Player. Куррентмедиа**](player-currentmedia.md)
</dt> <dt>

[**Параметры. медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Параметры. рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





