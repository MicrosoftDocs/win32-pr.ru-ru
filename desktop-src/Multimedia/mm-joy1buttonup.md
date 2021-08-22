---
title: Сообщение MM_JOY1BUTTONUP (Ммсистем. h)
description: '\_Сообщение JOY1BUTTONUP mm уведомляет окно с захваченным джойстиком, JOYSTICKID1, что кнопка была снята.'
ms.assetid: 37f0f87a-4805-4cec-9c0c-9d6b36a3ff0d
keywords:
- сообщение MM_JOY1BUTTONUP Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_JOY1BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c70c7b8dda57d91e595bd65223a2fd33ef904679e35a38aaacbaf263b525258f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065574"
---
# <a name="mm_joy1buttonup-message"></a>MM \_ JOY1BUTTONUP, сообщение

Сообщение **\_ JOY1BUTTONUP mm** уведомляет окно с захваченным джойстиком, JOYSTICKID1, что кнопка была снята.


```C++
MM_JOY1BUTTONUP 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*фвбуттонс*
</dt> <dd>

Определяет кнопку, которая имеет измененное состояние и нажатые кнопки. Может принимать одно из следующих значений:



| Требование | Значение |
|-----------------|-------------------------------------------|
| \_BUTTON1CHG радости | Первая кнопка джойстика изменила состояние.  |
| \_BUTTON2CHG радости | Вторая кнопка джойстика изменила состояние. |
| \_BUTTON3CHG радости | Третья кнопка игрового состояния изменила состояние.  |
| \_BUTTON4CHG радости | Четвертая кнопка джойстика изменила состояние. |



 

и один или несколько из следующих элементов:



| Требование | Значение |
|--------------|------------------------------------|
| РАДОСТЬ \_ | Нажата первая кнопка джойстика.  |
| ДЖОЙСТИК ( \_ Button2) | Нажата вторая кнопка джойстика. |
| \_BUTTON3 радости | Нажата третья кнопка джойстика.  |
| \_BUTTON4 радости | Нажата четвертая кнопка джойстика. |



 

</dd> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*кспос*
</dt> <dd>

Координаты x джойстика относительно левого верхнего угла клиентской области.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*ипос*
</dt> <dd>

Координата по оси y джойстика относительно левого верхнего угла клиентской области.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>ммсистем. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Джойстики](joysticks.md)
</dt> <dt>

[Мультимедийные сообщения джойстика](multimedia-joystick-messages.md)
</dt> </dl>

 

 





