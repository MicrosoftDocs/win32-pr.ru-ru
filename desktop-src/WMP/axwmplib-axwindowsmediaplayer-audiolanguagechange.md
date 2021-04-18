---
title: Событие Аудиолангуажечанже объекта Аксвиндовсмедиаплайер
description: Событие Аудиолангуажечанже возникает при изменении текущего звукового языка. | Событие Аудиолангуажечанже объекта Аксвиндовсмедиаплайер
ms.assetid: 35e4ff82-fc59-4d28-b7fc-1527fb46b960
keywords:
- Событие Аудиолангуажечанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- AudioLanguageChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354a34f30df237827e3d369721963ec2c1797e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694393"
---
# <a name="audiolanguagechange-event-of-the-axwindowsmediaplayer-object"></a>Событие Аудиолангуажечанже объекта Аксвиндовсмедиаплайер

Событие Аудиолангуажечанже возникает при изменении текущего звукового языка.

``` syntax
[C#]
private void player_AudioLanguageChange(
  object sender,
  _WMPOCXEvents_AudioLanguageChangeEvent e
)

[Visual Basic]
Private Sub player_AudioLanguageChange(
  sender As Object,
  e As _WMPOCXEvents_AudioLanguageChangeEvent
) Handles player.AudioLanguageChange
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ аудиолангуажечанжеевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ аудиолангуажечанжеевент**, который содержит следующее свойство, связанное с этим событием.



| Свойство   | Описание                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| **Надежно** | **System. Int32** Уникально идентифицирует определенный диалект языка, называемый языковым стандартом.<br/> |



 

## <a name="remarks"></a>Комментарии

Код локали (LCID) однозначно определяет определенный диалект языка, который называется локальным языком.

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

[**IWMPControls3. Куррентаудиолангуаже (VB и C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> </dl>

 

 





