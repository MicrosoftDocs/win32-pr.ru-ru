---
title: Событие Домаинчанже объекта Аксвиндовсмедиаплайер
description: Событие Домаинчанже возникает при смене домена DVD. | Событие Домаинчанже объекта Аксвиндовсмедиаплайер
ms.assetid: a080082e-1ba4-4080-b39c-b84292ecacb0
keywords:
- событие домаинчанже объекта аксвиндовсмедиаплайер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- DomainChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a37f10679225fb893fad8bcf6fc6687021256e305e8c5a08e6ebe96d16b74e81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136127"
---
# <a name="domainchange-event-of-the-axwindowsmediaplayer-object"></a>Событие Домаинчанже объекта Аксвиндовсмедиаплайер

Событие Домаинчанже возникает при смене домена DVD.

``` syntax
[C#]
private void player_DomainChange(
  object sender,
  _WMPOCXEvents_DomainChangeEvent e
)

[Visual Basic]
Private Sub player_DomainChange(  
  sender As Object,
  e As _WMPOCXEvents_DomainChangeEvent
) Handles player.DomainChange
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ домаинчанжеевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ домаинчанжеевент**, который содержит следующее свойство, связанное с этим событием.



| Свойство.  | Описание                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| стрдомаин | System. Стрингиндикатес новый домен. Возможные значения см. в разделе "Примечания".<br/> |



 

## <a name="remarks"></a>Remarks

В следующей таблице приведены возможные значения для свойства Стрдомаин.



| Строка            | Описание                                                          |
|-------------------|----------------------------------------------------------------------|
| фирстплай         | Выполнение инициализации DVD-диска по умолчанию.                     |
| видеоманажермену  | Отображение меню для всего диска. Также называется корневым меню или Топмену. |
| видеотитлесетмену | Отображение меню для текущего набора заголовков. Также называется Титлемену.     |
| title             | Отображение текущего заголовка.                                        |
| stop              | Навигатор DVD находится в области DVD-диска.                         |



 

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

[**Интерфейс ИВМПДВД (VB и C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





