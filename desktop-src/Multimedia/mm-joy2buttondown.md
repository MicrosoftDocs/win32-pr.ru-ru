---
title: Сообщение MM_JOY2BUTTONDOWN (Ммсистем. h)
description: '\_Сообщение JOY2BUTTONDOWN mm уведомляет окно с захваченным джойстиком JOYSTICKID2, что была нажата кнопка.'
ms.assetid: b4cd48ea-91ad-48e9-b0ae-58d8ee124171
keywords:
- MM_JOY2BUTTONDOWN сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONDOWN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f155fcdc21247e01fd5d730f3f7d4daaba705e65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672493"
---
# <a name="mm_joy2buttondown-message"></a>MM \_ JOY2BUTTONDOWN, сообщение

Сообщение **\_ JOY2BUTTONDOWN mm** уведомляет окно с захваченным джойстиком JOYSTICKID2, что была нажата кнопка.


```C++
MM_JOY2BUTTONDOWN 
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

 

 





