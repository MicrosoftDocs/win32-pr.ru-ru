---
title: Сообщение WM_CAP_GET_USER_DATA (VFW. h)
description: Сообщение о \_ \_ получении \_ \_ данных об ошибке WM Cap Получает длинное \_ значение типа PTR, связанное с окном сбора данных. Это сообщение можно отправить явно или с помощью макроса Капжетусердата.
ms.assetid: f7c121ba-44a1-4916-b602-c53d8332c2af
keywords:
- сообщение WM_CAP_GET_USER_DATA Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_GET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a79a513d415d166ab2715a181a6d8fc366b60480caf2982f6bbc53eadf90d96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892034"
---
# <a name="wm_cap_get_user_data-message"></a>\_Сообщение о \_ получении \_ \_ данных пользователя с креплениями WM

Сообщение **о \_ \_ получении \_ \_ данных** об ошибке WM Cap получает **длинное значение \_ типа PTR** , связанное с окном сбора данных. Это сообщение можно отправить явно или с помощью макроса [**капжетусердата**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata) .


```C++
WM_CAP_GET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Возвращаемое значение

Возвращает значение, сохраненное ранее с помощью сообщения о [**\_ \_ \_ пользовательских \_ данных для установки крепления WM**](wm-cap-set-user-data.md) .

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

 

 





