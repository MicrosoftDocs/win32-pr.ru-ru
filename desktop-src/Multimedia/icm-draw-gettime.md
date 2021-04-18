---
title: Сообщение ICM_DRAW_GETTIME (VFW. h)
description: Сообщение ICM \_ Draw \_ запрашивает драйвер подготовки отчетов, который управляет временем рисования кадров, чтобы вернуть текущее значение его внутреннего времени. Это сообщение можно отправить явно или с помощью макроса Икдравжеттиме.
ms.assetid: 77f0a322-c0bc-4cfe-a3d0-7633cf8d682a
keywords:
- ICM_DRAW_GETTIME сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_GETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f756a76408d01cb72ee1762f14bb8a5eab19e475
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672706"
---
# <a name="icm_draw_gettime-message"></a>\_Сообщение о \_ выполнении ICM Draw

Сообщение **ICM \_ Draw \_** запрашивает драйвер подготовки отчетов, который управляет временем рисования кадров, чтобы вернуть текущее значение его внутреннего времени. Это сообщение можно отправить явно или с помощью макроса [**икдравжеттиме**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) .


```C++
ICM_DRAW_GETTIME 
wParam = (DWORD_PTR) (LPVOID) lplTime; 
lParam = 0; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lplTime"></span><span id="lpltime"></span><span id="LPLTIME"></span>*лплтиме*
</dt> <dd>

Адрес, который будет содержать текущее время. Возвращаемое значение должно быть указано в примерах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Комментарии

Это сообщение обычно поддерживается оборудованием, которое выполняет собственное асинхронное распаковка, время и рисование. Сообщение также может быть отправлено, если оборудование используется в качестве хозяина синхронизации.

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

 

 





