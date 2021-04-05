---
title: Сообщение WM_CAP_DRIVER_DISCONNECT (VFW. h)
description: '\_ \_ \_ Сообщение об отключении драйвера WM Cap отключает драйвер записи из окна записи. Это сообщение можно отправить явно или с помощью макроса Капдривердисконнект.'
ms.assetid: a420f24a-aa7d-4788-9120-2c11e5e2c14c
keywords:
- WM_CAP_DRIVER_DISCONNECT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_DISCONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acad628cc61bbb50c56f68fda91ac87be4feb728
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988529"
---
# <a name="wm_cap_driver_disconnect-message"></a>\_ \_ \_ Сообщение об отключении драйвера WM Cap

Сообщение **об \_ \_ \_ отключении драйвера WM Cap** отключает драйвер записи из окна записи. Это сообщение можно отправить явно или с помощью макроса [**капдривердисконнект**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) .


```C++
WM_CAP_DRIVER_DISCONNECT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** , если окно записи не подключено к драйверу записи.

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

 

 





