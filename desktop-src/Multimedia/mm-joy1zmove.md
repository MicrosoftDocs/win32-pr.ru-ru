---
title: Сообщение MM_JOY1ZMOVE (Ммсистем. h)
description: '\_Сообщение JOY1ZMOVE мм уведомляет окно с захваченным джойстиком, JOYSTICKID1, что расположение джойстика на оси z изменилось.'
ms.assetid: 25d98963-03e6-4276-a132-256e8bbfa73b
keywords:
- MM_JOY1ZMOVE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_JOY1ZMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7d4db3db8c1817f0502ce14cc5328ad666b32c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493275"
---
# <a name="mm_joy1zmove-message"></a>MM \_ JOY1ZMOVE, сообщение

Сообщение **\_ JOY1ZMOVE мм** уведомляет окно с захваченным джойстиком, JOYSTICKID1, что расположение джойстика на оси z изменилось.


```C++
MM_JOY1ZMOVE 
fwButtons = wParam; 
zPos = LOWORD(lParam); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*фвбуттонс*
</dt> <dd>

Определяет нажатые кнопки. Это может быть одно или несколько из следующих значений:



| Требование | Значение |
|--------------|------------------------------------|
| РАДОСТЬ \_ | Нажата первая кнопка джойстика.  |
| ДЖОЙСТИК ( \_ Button2) | Нажата вторая кнопка джойстика. |
| \_BUTTON3 радости | Нажата третья кнопка джойстика.  |
| \_BUTTON4 радости | Нажата четвертая кнопка джойстика. |



 

</dd> <dt>

<span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*зпос*
</dt> <dd>

Z-координата джойстика.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>Ммсистем. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Джойстики](joysticks.md)
</dt> <dt>

[Мультимедийные сообщения джойстика](multimedia-joystick-messages.md)
</dt> </dl>

 

 





