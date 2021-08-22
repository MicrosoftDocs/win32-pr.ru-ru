---
description: Указывает, включены ли все протоколы потоковой передачи.
ms.assetid: cf072572-58f7-429a-954a-8808d05248f0
title: Свойство MFNETSOURCE_ENABLE_STREAMING (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fae2b127a52bbea9e8d122ec9ad219c61010068b07696b44cce49cc7546c9fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463704"
---
# <a name="mfnetsource_enable_streaming-property"></a>МФНЕТСАУРЦЕ \_ включить \_ потоковую передачу свойства

Указывает, включены ли все протоколы потоковой передачи.



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

Логическое значение (**Long**)

VT \_ I4

**лвал**



## <a name="remarks"></a>Remarks

Константа **мфнетсаурце \_ Enable \_ Streaming** определяет идентификатор GUID для этого ключа свойства. Идентификатор свойства (PID) равен нулю.

Приложения могут использовать это свойство для настройки сетевого источника. Чтобы задать свойство, передайте **ипропертисторе** указатель на [конфигурацию источника мультимедиа](configuring-a-media-source.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Сетевые подключения в Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Поддерживаемые протоколы](supported-protocols.md)
</dt> </dl>

 

 




