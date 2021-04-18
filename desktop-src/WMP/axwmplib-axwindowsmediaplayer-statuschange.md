---
title: Событие StatusChange объекта Аксвиндовсмедиаплайер
description: Событие StatusChange возникает при изменении значения свойства Status. | Событие StatusChange объекта Аксвиндовсмедиаплайер
ms.assetid: 5295fccb-7be0-46d3-85ba-b481e575d393
keywords:
- Событие StatusChange в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- StatusChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3ef3224afadb1f98a3067913a8beb095d4e46e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695038"
---
# <a name="statuschange-event-of-the-axwindowsmediaplayer-object"></a>Событие StatusChange объекта Аксвиндовсмедиаплайер

Событие **StatusChange** возникает при изменении значения свойства **Status** .

``` syntax
[C#]
private void player_StatusChange(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_StatusChange(
  sender As Object,
  e As System.EventArgs
) Handles player.StatusChange
```

## <a name="event-data"></a>Данные о событиях

Это событие не содержит данных.

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

[**Аксвиндовсмедиаплайер. Status (VB и C#)**](axwmplib-axwindowsmediaplayer-status--vb-and-c.md)
</dt> </dl>

 

 





