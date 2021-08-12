---
title: Сообщение WM_CAP_GRAB_FRAME_NOSTOP (VFW. h)
description: Сообщение о \_ \_ \_ неостановкой кадра захвата для WM \_ замещает буфер кадров одним несжатым кадром с устройства записи и отображает его.
ms.assetid: 5f6e3ce7-3595-456e-82c8-eeb162ace81a
keywords:
- сообщение WM_CAP_GRAB_FRAME_NOSTOP Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME_NOSTOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b81c581ad7e3913640271b32b18791ebf7b48ed09cd365af82ed263449f05471
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622603"
---
# <a name="wm_cap_grab_frame_nostop-message"></a>\_Сообщение о \_ \_ \_ неостановкой кадра захвата WM Cap

Сообщение **о \_ \_ \_ \_ Неостановкой кадра захвата для WM** замещает буфер кадров одним несжатым кадром с устройства записи и отображает его. В отличие от сообщения [**с \_ закреплением \_ \_ WM**](wm-cap-grab-frame.md) , состояние наложения или предварительного просмотра не изменяется этим сообщением. Это сообщение можно отправить явно или с помощью макроса [**капграбфраменостоп**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) .


```C++
WM_CAP_GRAB_FRAME_NOSTOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

## <a name="remarks"></a>Remarks

Дополнительные сведения об установке функций обратного вызова см. в разделе [**\_ \_ \_ \_ ошибка обратного вызова Set крепления WM**](wm-cap-set-callback-error.md) , а также сообщения [**\_ \_ \_ \_ кадра обратного вызова Set крепления WM**](wm-cap-set-callback-frame.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Видеозапись](video-capture.md)
</dt> <dt>

[Сообщения видеозаписи](video-capture-messages.md)
</dt> </dl>

 

 





