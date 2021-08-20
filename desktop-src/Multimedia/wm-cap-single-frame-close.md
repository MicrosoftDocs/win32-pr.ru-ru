---
title: Сообщение WM_CAP_SINGLE_FRAME_CLOSE (VFW. h)
description: Сообщение о \_ \_ закрытии одинарного кадра WM Cap \_ \_ закрывает файл записи, Открытый \_ \_ \_ \_ сообщением об открытом фрейме WM Cap. Это сообщение можно отправить явно или с помощью макроса Капкаптуресинглефрамеклосе.
ms.assetid: fde5f34b-0781-49a2-a509-64192a1d9ec0
keywords:
- сообщение WM_CAP_SINGLE_FRAME_CLOSE Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_CLOSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f304fd0c62818562e53c6129a15b266db6f1ac000de64fb779e5cdb3e437d43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134968"
---
# <a name="wm_cap_single_frame_close-message"></a>\_Сообщение о \_ \_ \_ закрытии одиночного кадра WM Cap

Сообщение **о \_ \_ \_ \_ закрытии одинарного кадра WM Cap** закрывает файл записи, Открытый сообщением об [**\_ \_ \_ \_ открытом фрейме WM Cap**](wm-cap-single-frame-open.md) . Это сообщение можно отправить явно или с помощью макроса [**капкаптуресинглефрамеклосе**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) .


```C++
WM_CAP_SINGLE_FRAME_CLOSE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

## <a name="remarks"></a>Remarks

Дополнительные сведения об установке функций обратного вызова см. в разделе [**\_ \_ \_ \_ ошибка обратного вызова Set крепления WM**](wm-cap-set-callback-error.md) , а также сообщения [**\_ \_ \_ \_ кадра обратного вызова Set крепления WM**](wm-cap-set-callback-frame.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Видеозапись](video-capture.md)
</dt> <dt>

[Сообщения видеозаписи](video-capture-messages.md)
</dt> </dl>

 

 





