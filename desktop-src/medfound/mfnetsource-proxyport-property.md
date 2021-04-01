---
description: Указывает номер порта прокси-сервера.
ms.assetid: cd84911b-3658-489f-b454-23eded0cbfa0
title: Свойство MFNETSOURCE_PROXYPORT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 228f7d9390d53f7d8182a198879dcb2d81e3bae7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263613"
---
# <a name="mfnetsource_proxyport-property"></a>МФНЕТСАУРЦЕ \_ проксипорт, свойство

Указывает номер порта прокси-сервера.



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

**DWORD** (хранится в формате **Long**)

VT \_ I4

**лвал**



## <a name="remarks"></a>Комментарии

Константа **мфнетсаурце \_ проксипорт** определяет идентификатор GUID для этого ключа свойства. Идентификатор свойства (PID) равен нулю.

Приложения могут использовать это свойство для настройки локатора прокси при создании прокси-объекта-локатора. Чтобы задать свойство, передайте указатель **ипропертисторе** в параметре *ппроксиконфиг* функции [**мфкреатепроксилокатор**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) . Если это свойство не задано для HTTP, по умолчанию локатор прокси-сервера использует значение 80.

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

[Поддержка прокси-сервера для сетевых источников](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




