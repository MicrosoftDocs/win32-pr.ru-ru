---
description: Указывает транспортный протокол, используемый сетевым источником.
ms.assetid: 7c8598ff-f408-42d0-9eee-3ef1e82f0466
title: Свойство MFNETSOURCE_TRANSPORT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd41653f2b5ea0686527af4d6ee8c8b9962005aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897925"
---
# <a name="mfnetsource_transport-property"></a>МФНЕТСАУРЦЕ, \_ свойство транспорта

Указывает транспортный протокол, используемый сетевым источником. Значение этого свойства является членом перечисления [**\_ \_ типа транспорта мфнетсаурце**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) .



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

**LONG**

VT \_ I4

**лвал**



## <a name="remarks"></a>Комментарии

Постоянный **мфнетсаурце \_ транспорт** определяет идентификатор GUID для этого ключа свойства. Идентификатор свойства (PID) равен нулю.

Это свойство доступно только для чтения. Чтобы получить это свойство, выполните запрос к источнику сети для интерфейса **ипропертисторе** и вызовите метод **Ипропертисторе:: GetValue**.

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

 

 




