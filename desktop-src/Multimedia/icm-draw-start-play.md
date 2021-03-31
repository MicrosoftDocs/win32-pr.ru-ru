---
title: Сообщение ICM_DRAW_START_PLAY (VFW. h)
description: Сообщение ICM \_ Draw \_ Start \_ Play предоставляет время начала и окончания операции воспроизведения для драйвера подготовки к просмотру. Это сообщение можно отправить явно или с помощью макроса Икдравстартплай.
ms.assetid: 27c4c06e-6510-43dc-a754-fe44144796f5
keywords:
- ICM_DRAW_START_PLAY сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_START_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefea0f6344fb598fac1f0413bba5c377c5914e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135683"
---
# <a name="icm_draw_start_play-message"></a>\_Сообщение о запуске ICM Draw \_ начать \_ Воспроизведение

Сообщение **ICM \_ Draw \_ Start \_ Play** предоставляет время начала и окончания операции воспроизведения для драйвера подготовки к просмотру. Это сообщение можно отправить явно или с помощью макроса [**икдравстартплай**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) .


```C++
ICM_DRAW_START_PLAY 
wParam = (DWORD_PTR) lFrom; 
lParam = (DWORD_PTR) lTo; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lFrom"></span><span id="lfrom"></span><span id="LFROM"></span>*лфром*
</dt> <dd>

Время начала.

</dd> <dt>

<span id="lTo"></span><span id="lto"></span><span id="LTO"></span>*lTo*
</dt> <dd>

Время окончания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="remarks"></a>Комментарии

Это сообщение предшествует всем данным кадра, отправляемым драйверу подготовки отчетов.

Единицы для *лфром* и *lTo* задаются с помощью сообщения [**ICM \_ Draw \_ Begin**](icm-draw-begin.md) . Для данных видео это обычно номер кадра. Дополнительные сведения о скорости воспроизведения см. в разделе **дврате** and **двскале** Members структуры [**икдравбегин**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) .

Если время окончания меньше времени начала, направление воспроизведения изменяется на противоположное.

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

 

 





