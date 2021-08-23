---
description: Указывает имя узла прокси-сервера.
ms.assetid: e53c86e9-c326-41c9-aa86-c80a750b9ce3
title: Свойство MFNETSOURCE_PROXYHOSTNAME (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82746763c937bdca388782cb0882b536c0b9e93b660e0f8e0a04426e5b48a61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663674"
---
# <a name="mfnetsource_proxyhostname-property"></a>МФНЕТСАУРЦЕ \_ проксихостнаме, свойство

Указывает имя узла прокси-сервера.



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

Строка расширенных символов (**WCHAR** \* )

VT \_ LPWSTR

**пвсзвал**



## <a name="remarks"></a>Remarks

Константа **мфнетсаурце \_ проксихостнаме** определяет идентификатор GUID для этого ключа свойства. Идентификатор свойства (PID) равен нулю.

Приложения могут использовать это свойство для настройки локатора прокси-сервера по умолчанию при создании объекта локатора прокси-сервера. Чтобы задать свойство, передайте указатель **ипропертисторе** в параметре *ппроксиконфиг* функции [**мфкреатепроксилокатор**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) . Это свойство должно быть задано приложением, если локатор прокси-сервера настроен для выполнения в ручном режиме.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Сетевые подключения в Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Поддержка прокси-сервера для сетевых источников](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




