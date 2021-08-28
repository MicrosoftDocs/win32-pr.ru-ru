---
description: Отправляется в очередь сообщений установки потока по истечении времени ожидания. Сообщение отправляется функцией PeekMessage.
ms.assetid: 419e3f05-35ec-4e48-b24d-ab98df687b20
title: Сообщение WM_TIMER (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d770d640b801849eeebe1c4ec86df8c41642c6149b89e00d82261f4e090f56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710034"
---
# <a name="wm_timer-message"></a>\_Сообщение таймера WM

Отправляется в очередь сообщений установки потока по истечении времени ожидания. Сообщение отправляется функцией [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) . [](/windows/win32/api/winuser/nf-winuser-getmessage)


```C++
#define WM_TIMER                        0x0113
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* \[ окне\]
</dt> <dd>

Идентификатор таймера.

</dd> <dt>

*lParam* \[ окне\]
</dt> <dd>

Указатель на определяемую приложением функцию обратного вызова, которая была передана функции [**сеттимер**](/windows/win32/api/winuser/nf-winuser-settimer) при установке таймера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **lResult**

Приложение должно вернуть нуль, если оно обрабатывает это сообщение.

## <a name="remarks"></a>Remarks

Вы можете обработать сообщение, указав в процедуре Windows регистр **\_ таймера WM** . В противном случае [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) будет вызывать функцию обратного вызова [*тимерпрок*](/windows/win32/api/winuser/nc-winuser-timerproc) , указанную в вызове функции [**сеттимер**](/windows/win32/api/winuser/nf-winuser-settimer) , используемой для установки таймера.

Сообщение **\_ таймера WM** является сообщением с низким приоритетом. Функции [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) и [**Message**](/windows/win32/api/winuser/nf-winuser-getmessage) помещаются в это сообщение только в том случае, если в очереди сообщений потока отсутствуют другие сообщения с более высоким приоритетом.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[**сеттимер**](/windows/win32/api/winuser/nf-winuser-settimer)
</dt> <dt>

[**тимерпрок**](/windows/win32/api/winuser/nc-winuser-timerproc)
</dt> <dt>

**Зрения**
</dt> <dt>

[Таймеры](timers.md)
</dt> </dl>

 

 
