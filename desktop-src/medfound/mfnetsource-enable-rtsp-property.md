---
description: Указывает, включен ли транспорт RTSP (Real-Time Streaming Protocol) в сетевом источнике.
ms.assetid: 299393d2-7949-48ef-a36d-19bb8760fc4e
title: Свойство MFNETSOURCE_ENABLE_RTSP (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac191e6e244a8e341fef0dccd274293f09846aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711268"
---
# <a name="mfnetsource_enable_rtsp-property"></a>МФНЕТСАУРЦЕ \_ включить \_ свойство RTSP

Указывает, включен ли транспорт RTSP (Real-Time Streaming Protocol) в сетевом источнике.



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

Логическое значение (**Long**)

VT \_ I4

**лвал**



## <a name="remarks"></a>Комментарии

Константа **мфнетсаурце \_ Enable \_ RTSP** определяет идентификатор GUID для этого ключа свойства. Идентификатор свойства (PID) равен нулю.

Приложения могут использовать это свойство для настройки сетевого источника. Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника. Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Сетевые подключения в Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Поддерживаемые протоколы](supported-protocols.md)
</dt> </dl>

 

 




