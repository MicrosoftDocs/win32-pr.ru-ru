---
title: Сообщение ICM_DRAW_SETTIME (VFW. h)
description: ICM \_ Draw \_ SETTIME предоставляет сведения о синхронизации драйверу подготовки отчетов, который обрабатывает время рисования кадров.
ms.assetid: 211e8ecc-ef36-4598-aa1d-cb0a06e64f14
keywords:
- ICM_DRAW_SETTIME сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_SETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ce1e37709477ba6080219e5225b3fde02dfed75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891757"
---
# <a name="icm_draw_settime-message"></a>\_Сообщение ICM Draw \_ SETTIME

**ICM \_ Draw \_ SETTIME** предоставляет сведения о синхронизации драйверу подготовки отчетов, который обрабатывает время рисования кадров. Сведения о синхронизации — это образец номера кадра для рисования. Это сообщение можно отправить явно или с помощью макроса [**икдравсеттиме**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) .


```C++
ICM_DRAW_SETTIME 
wParam = (DWORD_PTR) lpTime; 
lParam = 0; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*лптиме*
</dt> <dd>

Образец номера кадра для отображения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Комментарии

Как правило, драйвер сравнивает указанное значение с номером кадра, связанным со временем его внутреннего времени, и пытается синхронизировать два, если разница существенна.

Это сообщение используется, когда оборудование выполняет собственное асинхронное распаковку, время и рисование, а оборудование использует внешний сигнал синхронизации (оборудование не используется в качестве хозяина синхронизации).

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

 

 





