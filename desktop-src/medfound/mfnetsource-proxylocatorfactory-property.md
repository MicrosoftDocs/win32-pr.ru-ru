---
description: Содержит указатель на интерфейс Имфнетпроксилокаторфактори.
ms.assetid: 455325c0-5116-4e81-9729-fab9c6a367c7
title: Свойство MFNETSOURCE_PROXYLOCATORFACTORY (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc06f58fc11e4d0dcff95274170a76b25160b584231bd2c9e39ed1949b1363e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954744"
---
# <a name="mfnetsource_proxylocatorfactory-property"></a>МФНЕТСАУРЦЕ \_ проксилокаторфактори, свойство

Содержит указатель на интерфейс [**имфнетпроксилокаторфактори**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) .



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

Указатель **IUnknown**

VT \_ Unknown

**пунквал**



## <a name="remarks"></a>Remarks

Константа **мфнетсаурце \_ проксилокаторфактори** определяет идентификатор GUID для этого ключа свойства. Идентификатор свойства (PID) равен нулю.

Приложения могут использовать это свойство для предоставления пользовательского указателя прокси-сервера для сетевого источника. Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника. Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Сетевые подключения в Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Поддержка прокси-сервера для сетевых источников](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




