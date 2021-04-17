---
title: Событие Фолдерсканстатечанже объекта Аксвиндовсмедиаплайер
description: Событие Фолдерсканстатечанже возникает при изменении состояния операции наблюдения за папками.
ms.assetid: f68829a3-00df-417a-ae78-49dff1e6f09b
keywords:
- Событие Фолдерсканстатечанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- FolderScanStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3672f16bee5251aa46e6a64a0da983e0f34ec54a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694450"
---
# <a name="folderscanstatechange-event-of-the-axwindowsmediaplayer-object"></a>Событие Фолдерсканстатечанже объекта Аксвиндовсмедиаплайер

Событие Фолдерсканстатечанже возникает при изменении состояния операции наблюдения за папками.

``` syntax
[C#]
private void player_FolderScanStateChange(
  object sender,
  _WMPOCXEvents_FolderScanStateChangeEvent e
)

[Visual Basic]
Private Sub player_FolderScanStateChange( 
  sender As Object,  
  e As _WMPOCXEvents_FolderScanStateChangeEvent
) Handles player.FolderScanStateChange
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ фолдерсканстатечанжеевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ фолдерсканстатечанжеевент**, который содержит следующее свойство, связанное с этим событием.



| Свойство | Описание                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| вмпфсс   | Значение перечисления Вмплиб. Вмпфолдерсканстатесе, указывающее новое состояние.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 11<br/>                                                                                         |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**вмпфолдерсканстате**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpfolderscanstate)
</dt> </dl>

 

 





