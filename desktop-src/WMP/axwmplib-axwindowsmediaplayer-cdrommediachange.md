---
title: Событие Кдроммедиачанже объекта Аксвиндовсмедиаплайер
description: Событие Кдроммедиачанже возникает при вставке или извлечении компакт-диска или DVD-диска из дисковода CD или DVD. | Событие Кдроммедиачанже объекта Аксвиндовсмедиаплайер
ms.assetid: 0a6378c1-59e4-4be3-8764-d5c4ab478b6c
keywords:
- Событие Кдроммедиачанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- CdromMediaChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35385541f6bc91b6935f148fd8ae28df6a415f3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694387"
---
# <a name="cdrommediachange-event-of-the-axwindowsmediaplayer-object"></a>Событие Кдроммедиачанже объекта Аксвиндовсмедиаплайер

Событие **кдроммедиачанже** возникает при вставке или ИЗВЛЕЧЕНии компакт-диска или DVD-диска из дисковода CD или DVD.

``` syntax
[C#]
private void player_CdromMediaChange(
  object sender,
  _WMPOCXEvents_CdromMediaChangeEvent e
)

[Visual Basic]
Private Sub player_CdromMediaChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromMediaChangeEvent
) Handles player.CdromMediaChange
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ кдроммедиачанжеевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ кдроммедиачанжеевент**, который содержит следующее свойство, связанное с этим событием.



| Свойство | Описание                                                        |
|----------|--------------------------------------------------------------------|
| кдромнум | System. Int32Specifies. индекс компакт-диска или DVD-дисковода.<br/> |



 

## <a name="remarks"></a>Комментарии

Индекс дисковода компакт-дисков соответствует индексу интерфейса Ивмпкдром, доступного через интерфейс Ивмпкдромколлектион.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                          |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпкдром (VB и C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпкдромколлектион (VB и C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> </dl>

 

 





