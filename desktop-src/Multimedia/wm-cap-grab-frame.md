---
title: Сообщение WM_CAP_GRAB_FRAME (VFW. h)
description: Сообщение о \_ \_ кадре захвата WM Cap \_ извлекает и отображает один кадр из драйвера записи. После записи перекрытие и предварительный просмотр отключены. Это сообщение можно отправить явно или с помощью макроса Капграбфраме.
ms.assetid: 91d58c1c-53b9-4813-88c2-7a1acf641d96
keywords:
- сообщение WM_CAP_GRAB_FRAME Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdccfc9df0f3abac7febfa78029b4ecb351ec3044c618dc4c811e91b433f0f49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892044"
---
# <a name="wm_cap_grab_frame-message"></a>\_Сообщение о \_ блоке захвата крепления WM \_

Сообщение **о \_ \_ \_ кадре захвата WM Cap** извлекает и отображает один кадр из драйвера записи. После записи перекрытие и предварительный просмотр отключены. Это сообщение можно отправить явно или с помощью макроса [**капграбфраме**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) .


```C++
WM_CAP_GRAB_FRAME 
wParam = (WPARAM)0; 
lParam = (LPARAM)0L; 
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

 

 





