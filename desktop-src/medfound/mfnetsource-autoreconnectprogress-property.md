---
description: Число попыток повторного подключения сетевого источника к сети.
ms.assetid: e3410e68-6358-4f00-8039-833a4ccdf7fa
title: Свойство MFNETSOURCE_AUTORECONNECTPROGRESS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ade09bd425988cb0a64b258ff0887f8e79d4c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711273"
---
# <a name="mfnetsource_autoreconnectprogress-property"></a>МФНЕТСАУРЦЕ \_ аутореконнектпрогресс, свойство

Число попыток повторного подключения сетевого источника к сети.



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

**DWORD** (хранится в формате **Long**)

VT \_ I4

**лвал**



## <a name="remarks"></a>Комментарии

Константа **мфнетсаурце \_ аутореконнектпрогресс** определяет идентификатор GUID для этого ключа свойства. Идентификатор свойства (PID) равен нулю.

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

[Компоненты сетевого источника](network-source-features.md)
</dt> <dt>

[Сетевые подключения в Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




