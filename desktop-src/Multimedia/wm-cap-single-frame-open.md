---
title: Сообщение WM_CAP_SINGLE_FRAME_OPEN (VFW. h)
description: '\_ \_ \_ При открытии сообщения с одним кадром WM Cap \_ открывается файл записи для однокадровой записи. Все предыдущие сведения в файле записи перезаписываются. Это сообщение можно отправить явно или с помощью макроса Капкаптуресинглефрамеопен.'
ms.assetid: 4814737c-4395-4c01-a68e-fac43dd291fd
keywords:
- сообщение WM_CAP_SINGLE_FRAME_OPEN Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a58df70bea8971e10a769efbbc98220c46897ff6979e66ab45ae8f2ba81b971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134839"
---
# <a name="wm_cap_single_frame_open-message"></a>\_ \_ \_ Сообщение об открытом одном кадре WM Cap \_

При **открытии сообщения с \_ \_ одним \_ кадром \_ WM Cap** открывается файл записи для однокадровой записи. Все предыдущие сведения в файле записи перезаписываются. Это сообщение можно отправить явно или с помощью макроса [**капкаптуресинглефрамеопен**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen) .


```C++
WM_CAP_SINGLE_FRAME_OPEN 
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

 

 





