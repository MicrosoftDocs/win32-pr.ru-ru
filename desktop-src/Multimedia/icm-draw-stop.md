---
title: Сообщение ICM_DRAW_STOP (VFW. h)
description: Сообщение об ошибке ICM \_ Draw \_ уведомляет драйвер подготовки к прекращению его внутренних часов на время рисования кадров. Это сообщение можно отправить явно или с помощью макроса Икдравстоп.
ms.assetid: 9ffda595-e3d6-48f0-9487-69f7e95979c2
keywords:
- ICM_DRAW_STOP сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3bde99dfcf483e67aa6a601de2718814cc22439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490137"
---
# <a name="icm_draw_stop-message"></a>\_ \_ Сообщение об ошибке ПРОРИСОВКи ICM

Сообщение об ошибке **ICM \_ Draw \_** уведомляет драйвер подготовки к прекращению его внутренних часов на время рисования кадров. Это сообщение можно отправить явно или с помощью макроса [**икдравстоп**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) .


```C++
ICM_DRAW_STOP 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="remarks"></a>Комментарии

Это сообщение используется оборудованием, которое выполняет собственное асинхронное распаковка, время и рисование.

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

 

 





