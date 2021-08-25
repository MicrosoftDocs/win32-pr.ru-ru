---
title: Сообщение WM_CAP_DRIVER_DISCONNECT (VFW. h)
description: '\_ \_ \_ Сообщение об отключении драйвера WM Cap отключает драйвер записи из окна записи. Это сообщение можно отправить явно или с помощью макроса Капдривердисконнект.'
ms.assetid: a420f24a-aa7d-4788-9120-2c11e5e2c14c
keywords:
- сообщение WM_CAP_DRIVER_DISCONNECT Windows мультимедиа
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
ms.openlocfilehash: f6365366c6ea37b36734262d1d7a8412a7729406ff3fcc12e10ae9ba55d9ba84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803864"
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

 

 





