---
title: Сообщение ICM_COMPRESS (VFW. h)
description: Сообщение ICM \_ Compression уведомляет драйвер сжатия видео о необходимости сжатия фрейма данных в определенный приложением буфер.
ms.assetid: d95b943f-458d-4a5e-bab1-e3648d323395
keywords:
- сообщение ICM_COMPRESS Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_COMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1230f429eb49596dd8a450b8a384e0a69856b69c51141834458c09fa41ca54d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678474"
---
# <a name="icm_compress-message"></a>\_Сообщение о сжатии ICM

Сообщение **ICM \_** Compression уведомляет драйвер сжатия видео о необходимости сжатия фрейма данных в определенный приложением буфер.


```C++
ICM_COMPRESS 
wParam = (DWORD) (LPVOID) &icc; 
lParam = sizeof(ICCOMPRESS); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="icc"></span><span id="ICC"></span>*профилей*
</dt> <dd>

Указатель на структуру [**иккомпресс**](/windows/desktop/api/Vfw/ns-vfw-iccompress) . Следующие члены этой структуры определяют параметры сжатия: **лпбиинпут**, **лпинпут**, **лпбиаутпут**, **лпаутпут**, **лпбипрев**, **лппрев**, **лпккид**, **лпдвфлагс**, **двфрамесизе** и **двкуалити**. Драйвер также должен использовать член **бисизеимаже** структуры [**битмапинфохеадер**](/previous-versions//dd183376(v=vs.85)) , связанной с **лпбиаутпут** из **иккомпресс** , для получения размера сжатого кадра.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Размер [**иккомпресс**](/windows/desktop/api/Vfw/ns-vfw-iccompress)в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.

## <a name="requirements"></a>Requirements (Требования)



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

 

