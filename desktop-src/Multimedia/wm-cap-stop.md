---
title: Сообщение WM_CAP_STOP (VFW. h)
description: Сообщение о \_ \_ прекращении крепления WM останавливает операцию записи. Это сообщение можно отправить явно или с помощью макроса Капкаптурестоп.
ms.assetid: 0fea82f5-f381-485a-82ae-b081b3a5e402
keywords:
- сообщение WM_CAP_STOP Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bceac7a821a42227a388de6ebc2b9ea548156ec80d1e5baba7f1e1ad708002d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369333"
---
# <a name="wm_cap_stop-message"></a>\_ \_ Сообщение об ошибке крепления WM

Сообщение **о \_ \_ прекращении крепления WM** останавливает операцию записи. Это сообщение можно отправить явно или с помощью макроса [**капкаптурестоп**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) .

На этапе записи кадров данных изображение, собранное до отправки этого сообщения, сохраняется в файле записи. Аналогичная длительность звуковых данных также сохраняется в файле записи, если запись звука включена.


```C++
WM_CAP_STOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

## <a name="remarks"></a>Remarks

Операция отслеживания должна использовать это сообщение. Используйте сообщение [**об \_ \_ отмене крепления WM**](wm-cap-abort.md) , чтобы отказаться от текущей операции записи.

## <a name="requirements"></a>Requirements (Требования)



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

 

 





