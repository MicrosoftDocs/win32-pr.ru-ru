---
title: Сообщение WM_CAP_GET_USER_DATA (VFW. h)
description: Сообщение о \_ \_ получении \_ \_ данных об ошибке WM Cap Получает длинное \_ значение типа PTR, связанное с окном сбора данных. Это сообщение можно отправить явно или с помощью макроса Капжетусердата.
ms.assetid: f7c121ba-44a1-4916-b602-c53d8332c2af
keywords:
- WM_CAP_GET_USER_DATA сообщения Windows мультимедиа
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
ms.openlocfilehash: 02951667600acba115f506a610b167b72b69ea99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535021"
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

 

 





