---
description: Указывает номер порта прокси-сервера.
ms.assetid: cd84911b-3658-489f-b454-23eded0cbfa0
title: Свойство MFNETSOURCE_PROXYPORT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ac286fdcce276a29f08fef9df536f9a92152729791ff04d63478246825a718f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874628"
---
# <a name="mfnetsource_proxyport-property"></a>МФНЕТСАУРЦЕ \_ проксипорт, свойство

Указывает номер порта прокси-сервера.



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

**DWORD** (хранится в формате **Long**)

VT \_ I4

**лвал**



## <a name="remarks"></a>Remarks

Константа **мфнетсаурце \_ проксипорт** определяет идентификатор GUID для этого ключа свойства. Идентификатор свойства (PID) равен нулю.

Приложения могут использовать это свойство для настройки локатора прокси при создании прокси-объекта-локатора. Чтобы задать свойство, передайте указатель **ипропертисторе** в параметре *ппроксиконфиг* функции [**мфкреатепроксилокатор**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) . Если это свойство не задано для HTTP, по умолчанию локатор прокси-сервера использует значение 80.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Сетевые подключения в Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Поддержка прокси-сервера для сетевых источников](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




