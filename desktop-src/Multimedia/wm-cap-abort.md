---
title: Сообщение WM_CAP_ABORT (VFW. h)
description: '\_ \_ Сообщение об отмене крепления WM останавливает операцию записи.'
ms.assetid: a0479d73-8422-4833-9e8a-c262ec386f58
keywords:
- сообщение WM_CAP_ABORT Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_ABORT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904edb47c371ee13ed3492fd9257e3933bf2f001010d7dd2b0177a7729500813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800663"
---
# <a name="wm_cap_abort-message"></a>\_ \_ Сообщение об отмене крепления WM

Сообщение **об \_ \_ отмене крепления WM** останавливает операцию записи. В случае записи шага данные изображения, собранные до точки **\_ \_ прерывания крепления WM** , будут сохранены в файле записи, но звук не будет записан. Это сообщение можно отправить явно или с помощью макроса [**капкаптуреаборт**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) .


```C++
WM_CAP_ABORT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

## <a name="remarks"></a>Remarks

Операция отслеживания должна использовать это сообщение.

Используйте сообщение [**об \_ \_ остановке WM Cap**](wm-cap-stop.md) , чтобы остановить запись шагов в текущей позиции, а затем записать звук.

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

 

 





