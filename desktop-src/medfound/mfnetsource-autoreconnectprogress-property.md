---
description: Число попыток повторного подключения сетевого источника к сети.
ms.assetid: e3410e68-6358-4f00-8039-833a4ccdf7fa
title: Свойство MFNETSOURCE_AUTORECONNECTPROGRESS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cfbf0bac147b3608145d3ef38eb328a44de1c064899a5e7800acbadfadcf709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243878"
---
# <a name="mfnetsource_autoreconnectprogress-property"></a>МФНЕТСАУРЦЕ \_ аутореконнектпрогресс, свойство

Число попыток повторного подключения сетевого источника к сети.



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

**DWORD** (хранится в формате **Long**)

VT \_ I4

**лвал**



## <a name="remarks"></a>Remarks

Константа **мфнетсаурце \_ аутореконнектпрогресс** определяет идентификатор GUID для этого ключа свойства. Идентификатор свойства (PID) равен нулю.

Это свойство доступно только для чтения. Чтобы получить это свойство, выполните запрос к источнику сети для интерфейса **ипропертисторе** и вызовите метод **Ипропертисторе:: GetValue**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также статью

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Компоненты сетевого источника](network-source-features.md)
</dt> <dt>

[Сетевые подключения в Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




