---
title: Сообщение MM_JOY1BUTTONDOWN (Ммсистем. h)
description: '\_Сообщение JOY1BUTTONDOWN mm уведомляет окно с захваченным джойстиком JOYSTICKID1, что была нажата кнопка.'
ms.assetid: 764f4bb4-134d-46b8-badb-3fb06af31e13
keywords:
- сообщение MM_JOY1BUTTONDOWN Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_JOY1BUTTONDOWN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d2399eca0de21014b97c9156e6a16349fc5b0b5407b64b022eb077fd59d0609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137195"
---
# <a name="mm_joy1buttondown-message"></a>MM \_ JOY1BUTTONDOWN, сообщение

Сообщение **\_ JOY1BUTTONDOWN mm** уведомляет окно с захваченным джойстиком JOYSTICKID1, что была нажата кнопка.


```C++
MM_JOY1BUTTONDOWN 
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

Координата x джойстика относительно левого верхнего угла клиентской области.

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

 

 





