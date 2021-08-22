---
description: Сообщение WM \_ спулерстатус отправляется из диспетчера печати при добавлении или удалении задания из очереди диспетчера печати.
ms.assetid: 6140c9d8-0e5b-49f2-a4a6-cc1f2a0bed0a
title: Сообщение WM_SPOOLERSTATUS (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2869c468517abf466b348583748e391fc1f2a4226c74b5811fffabdb5eeb89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460344"
---
# <a name="wm_spoolerstatus-message"></a>\_Сообщение СПУЛЕРСТАТУС WM

Сообщение **WM \_ спулерстатус** отправляется из диспетчера печати при добавлении или удалении задания из очереди диспетчера печати.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Флаг JOBSTATUS запроса на вытягивание \_ .

</dd> <dt>

*lParam* 
</dt> <dd>

Слово нижнего порядка указывает количество заданий, остающихся в очереди диспетчера печати.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Приложение должно вернуть нуль, если оно обрабатывает это сообщение.

## <a name="remarks"></a>Remarks

Это сообщение предназначено только для информационных целей. Это сообщение является Советом и не имеет гарантированной семантики доставки. Приложения не должны рассчитывать на то, что они получат \_ сообщение WM спулерстатус для каждого изменения в состоянии диспетчера очереди печати.

\_после Windows XP сообщение WM спулерстатус не поддерживается. Чтобы получать уведомления об изменениях состояния очереди печати, можно использовать [**финдфирстпринтерчанженотификатион**](findfirstprinterchangenotification.md) и [**финднекстпринтерчанженотификатион**](findnextprinterchangenotification.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Сообщения API диспетчера очереди печати](printing-and-print-spooler-messages.md)
</dt> <dt>

[**финдфирстпринтерчанженотификатион**](findfirstprinterchangenotification.md)
</dt> <dt>

[**финднекстпринтерчанженотификатион**](findnextprinterchangenotification.md)
</dt> </dl>

 

