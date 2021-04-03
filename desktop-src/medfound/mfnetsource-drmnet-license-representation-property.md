---
description: Хранит массив байтов, представляющий лицензию DRM, связанную с потоком байтов.
ms.assetid: 866a9706-0b0a-4675-af61-5f55a5a69014
title: Свойство MFNETSOURCE_DRMNET_LICENSE_REPRESENTATION (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92af9a17779381aaed2d2226e17023ca40bc9c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810996"
---
# <a name="mfnetsource_drmnet_license_representation-property"></a>МФНЕТСАУРЦЕ \_ дрмнет \_ , \_ свойство представления лицензии

Хранит массив байтов, представляющий лицензию DRM, связанную с потоком байтов.



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

Массив байтов (**BLOB**)

\_большой двоичный объект VT

**объекте**



## <a name="remarks"></a>Комментарии

В **\_ \_ \_ представлении лицензии Constant мфнетсаурце дрмнет** определяется идентификатор GUID для этого ключа свойства. Идентификатор свойства (PID) равен нулю.

Это свойство доступно только для чтения. Чтобы получить значение свойства из потока сетевого байта, вызовите метод **ипропертисторе:: GetValue** и передайте структуру **PROPERTYKEY** в параметре *Key* . Члену **fmtid** объекта **PROPERTYKEY** должно быть присвоено значение GUID свойства.

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
</dt> </dl>

 

 




