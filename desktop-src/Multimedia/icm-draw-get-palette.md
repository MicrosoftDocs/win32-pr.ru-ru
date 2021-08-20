---
title: Сообщение ICM_DRAW_GET_PALETTE (VFW. h)
description: Сообщение ICM \_ \_ Get, получающая \_ палитру, запрашивает драйвер подготовки к просмотру для возврата палитры.
ms.assetid: 02a9df7d-e0b9-4bde-9cda-c36d2a10a23c
keywords:
- сообщение ICM_DRAW_GET_PALETTE Windows мультимедиа
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
ms.openlocfilehash: 6ef07085bef92d6191cea69429a5b544d5d2f706e1771baa404741aa98a5812b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987394"
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



## <a name="see-also"></a>См. также

<dl> <dt>

[Диспетчер сжатия видео](video-compression-manager.md)
</dt> <dt>

[Сообщения о сжатии видео](video-compression-messages.md)
</dt> </dl>

 

 





