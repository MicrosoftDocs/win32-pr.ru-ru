---
title: Сообщение MM_JOY2BUTTONUP (Ммсистем. h)
description: '\_Сообщение JOY2BUTTONUP mm уведомляет окно с захваченным джойстиком, JOYSTICKID2, что кнопка была снята.'
ms.assetid: da024466-7cd3-42ec-90a7-1468eb42841e
keywords:
- MM_JOY2BUTTONUP сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7a4f2d23739fc72a6898e2b53fc3e1c330687f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682162"
---
# <a name="mm_joy2buttonup-message"></a>MM \_ JOY2BUTTONUP, сообщение

Сообщение **\_ JOY2BUTTONUP mm** уведомляет окно с захваченным джойстиком, JOYSTICKID2, что кнопка была снята.


```C++
MM_JOY2BUTTONUP 
fwButton = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

**фвбуттонс** 
</dt> <dd>

Определяет кнопку, которая имеет измененное состояние и нажатые кнопки. Может принимать одно из следующих значений:



| Значение                                                                                                                                                            | Значение                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="JOY_BUTTON1CHG"></span><span id="joy_button1chg"></span><dl> <dt>**\_BUTTON1CHG радости**</dt> </dl> | Первая кнопка джойстика изменила состояние.<br/>  |
| <span id="JOY_BUTTON2CHG"></span><span id="joy_button2chg"></span><dl> <dt>**\_BUTTON2CHG радости**</dt> </dl> | Вторая кнопка джойстика изменила состояние.<br/> |
| <span id="JOY_BUTTON3CHG"></span><span id="joy_button3chg"></span><dl> <dt>**\_BUTTON3CHG радости**</dt> </dl> | Третья кнопка игрового состояния изменила состояние.<br/>  |
| <span id="JOY_BUTTON4CHG"></span><span id="joy_button4chg"></span><dl> <dt>**\_BUTTON4CHG радости**</dt> </dl> | Четвертая кнопка джойстика изменила состояние.<br/> |



 

и один или несколько из следующих элементов:



| Значение                                                                                                                                                   | Значение                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="JOY_BUTTON1"></span><span id="joy_button1"></span><dl> <dt>**РАДОСТЬ \_**</dt> </dl> | Нажата первая кнопка джойстика.<br/>  |
| <span id="JOY_BUTTON2"></span><span id="joy_button2"></span><dl> <dt>**ДЖОЙСТИК ( \_ Button2)**</dt> </dl> | Нажата вторая кнопка джойстика.<br/> |
| <span id="JOY_BUTTON3"></span><span id="joy_button3"></span><dl> <dt>**\_BUTTON3 радости**</dt> </dl> | Нажата третья кнопка джойстика.<br/>  |
| <span id="JOY_BUTTON4"></span><span id="joy_button4"></span><dl> <dt>**\_BUTTON4 радости**</dt> </dl> | Нажата четвертая кнопка джойстика.<br/> |



 

</dd> <dt>

**кспос** 
</dt> <dd>

Координаты x джойстика относительно левого верхнего угла клиентской области.

</dd> <dt>

**ипос** 
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

 

 





