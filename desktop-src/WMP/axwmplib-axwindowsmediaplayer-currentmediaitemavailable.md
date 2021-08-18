---
title: Событие Куррентмедиаитемаваилабле объекта Аксвиндовсмедиаплайер
description: Событие Куррентмедиаитемаваилабле возникает при доступности элемента метаданных изображения в текущем элементе мультимедиа. | Событие Куррентмедиаитемаваилабле объекта Аксвиндовсмедиаплайер
ms.assetid: 7db62e6a-5f20-441a-801f-147ac386c5f8
keywords:
- событие куррентмедиаитемаваилабле объекта аксвиндовсмедиаплайер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- CurrentMediaItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b5bbac6f27dfa7c9de1115eb3c2f5eea85096e0868ac17e0f8b11d81385f344
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582353"
---
# <a name="currentmediaitemavailable-event-of-the-axwindowsmediaplayer-object"></a>Событие Куррентмедиаитемаваилабле объекта Аксвиндовсмедиаплайер

Событие Куррентмедиаитемаваилабле возникает при доступности элемента метаданных изображения в текущем элементе мультимедиа.

``` syntax
[C#]
private void player_CurrentMediaItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentMediaItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentMediaItemAvailable(
  sender As Object,  
  e As _WMPOCXEvents_CurrentMediaItemAvailableEvent
) Handles player.CurrentMediaItemAvailable
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ куррентмедиаитемаваилабливенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ куррентмедиаитемаваилабливент**, который содержит следующее свойство, связанное с этим событием.



| Свойство     | Описание                                                 |
|--------------|-------------------------------------------------------------|
| бстритемнаме | Имя System. Стрингсе текущего элемента мультимедиа.<br/> |



 

## <a name="remarks"></a>Remarks

Так как воспроизведение может начаться до полной загрузки элемента мультимедиа, все метаданные, содержащиеся в элементе мультимедиа (например, обложку альбома), могут быть недоступны при начале воспроизведения. Это событие предупреждает о завершении загрузки графического элемента метаданных. Затем можно получить интерфейс **ивмпмедиа** , передав значение **бстритемнаме** в *ивмпмедиаколлектион*. метод **жетбинаме** , после которого можно получить доступ к графическому элементу метаданных с помощью *IWMPMedia3*. **жетитеминфобитипе** и укажите **WM/Picture** в качестве имени атрибута.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                          |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. Жетитеминфобитипе (VB и C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[**Ивмпмедиаколлектион. Жетбинаме (VB и C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





