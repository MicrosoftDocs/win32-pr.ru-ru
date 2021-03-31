---
title: Сообщение ICM_DRAW_GET_PALETTE (VFW. h)
description: Сообщение ICM \_ \_ Get, получающая \_ палитру, запрашивает драйвер подготовки к просмотру для возврата палитры.
ms.assetid: 02a9df7d-e0b9-4bde-9cda-c36d2a10a23c
keywords:
- ICM_DRAW_GET_PALETTE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a03f3658d2a2653f940e18e9b82b7cc3d7690ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071239"
---
# <a name="icm_draw_get_palette-message"></a>\_Сообщение о \_ получении \_ палитры ICM Draw

Сообщение **ICM \_ \_ Get, получающая \_ палитру** , запрашивает драйвер подготовки к просмотру для возврата палитры.


```C++
ICM_DRAW_GET_PALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Возвращаемое значение

Драйвер должен возвращать один из следующих элементов: маркер используемой палитры, **значение NULL** , если он не имеет возвращаемого маркера, или ИЦЕРР не \_ поддерживается, если он не поддерживает палитры.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Диспетчер сжатия видео](video-compression-manager.md)
</dt> <dt>

[Сообщения о сжатии видео](video-compression-messages.md)
</dt> </dl>

 

 





