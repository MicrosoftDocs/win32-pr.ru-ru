---
title: Сообщение WM_CAP_SINGLE_FRAME_OPEN (VFW. h)
description: '\_ \_ \_ При открытии сообщения с одним кадром WM Cap \_ открывается файл записи для однокадровой записи. Все предыдущие сведения в файле записи перезаписываются. Это сообщение можно отправить явно или с помощью макроса Капкаптуресинглефрамеопен.'
ms.assetid: 4814737c-4395-4c01-a68e-fac43dd291fd
keywords:
- WM_CAP_SINGLE_FRAME_OPEN сообщения Windows мультимедиа
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
ms.openlocfilehash: ac38186e4b5a34bbc11563b7e37a1aefc3de18c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892634"
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

## <a name="remarks"></a>Комментарии

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

 

 





