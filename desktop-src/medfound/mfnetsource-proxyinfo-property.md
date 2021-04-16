---
description: Хранит имя узла и порт прокси-сервера, используемого сетевым источником.
ms.assetid: 164f8ac3-08ce-40a8-ac8d-4c2a267d9db5
title: Свойство MFNETSOURCE_PROXYINFO (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f73ceedf71e567e026c5e9af67a67c5d84bebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712251"
---
# <a name="mfnetsource_proxyinfo-property"></a>МФНЕТСАУРЦЕ \_ проксинфо, свойство

Хранит имя узла и порт прокси-сервера, используемого сетевым источником.



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

Строка расширенных символов (**WCHAR** \* )

VT \_ LPWSTR

**пвсзвал**



## <a name="remarks"></a>Комментарии

Константа **мфнетсаурце \_ проксинфо** определяет идентификатор GUID для этого ключа свойства. Идентификатор свойства (PID) равен нулю.

Это свойство доступно только для чтения. Чтобы получить значение свойства из сетевого источника, вызовите метод **ипропертисторе:: GetValue** и передайте структуру **PROPERTYKEY** в параметре *Key* . Члену **fmtid** объекта **PROPERTYKEY** должно быть присвоено значение GUID свойства.

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

 

 




