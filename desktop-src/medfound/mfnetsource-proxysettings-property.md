---
description: Задает параметр конфигурации для локатора прокси-сервера по умолчанию.
ms.assetid: 85f2bd02-8a2f-46b5-b765-1a0bc5b6ccc3
title: Свойство MFNETSOURCE_PROXYSETTINGS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1330773ab33674e58ef07b95a53c4493e6e6f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155555"
---
# <a name="mfnetsource_proxysettings-property"></a>МФНЕТСАУРЦЕ \_ проксисеттингс, свойство

Задает параметр конфигурации для локатора прокси-сервера по умолчанию. Значение этого свойства является членом перечисления [**мфнет \_ проксисеттингс**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) .



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

**LONG**

VT \_ I4

**лвал**



## <a name="remarks"></a>Комментарии

Константа **мфнетсаурце \_ проксисеттингс** определяет идентификатор GUID для этого ключа свойства. Идентификатор свойства (PID) равен нулю.

Приложения могут использовать это свойство для настройки локатора прокси при создании объекта-посредника по умолчанию. Чтобы задать свойство, передайте указатель **ипропертисторе** в параметре *ппроксиконфиг* функции [**мфкреатепроксилокатор**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .

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

 

 




