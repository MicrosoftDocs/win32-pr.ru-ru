---
title: Сообщение MM_JOY2BUTTONUP (Ммсистем. h)
description: '\_Сообщение JOY2BUTTONUP mm уведомляет окно с захваченным джойстиком, JOYSTICKID2, что кнопка была снята.'
ms.assetid: da024466-7cd3-42ec-90a7-1468eb42841e
keywords:
- сообщение MM_JOY2BUTTONUP Windows мультимедиа
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
ms.openlocfilehash: 8f94a1761686bd2e3ac7c470268427a213d54cdb4b8a58d54fdd6961427c2377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119557314"
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

 

 





