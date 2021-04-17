---
description: Нотфиес приложение, когда для выбранного редактора IME требуются сведения о окне кандидатов. Приложение получает эту команду через \_ сообщение запроса WM IME \_ с параметрами параметров, как показано ниже.
ms.assetid: 35849290-a5be-406f-82f5-4a7e2af48586
title: Код уведомления IMR_CANDIDATEWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb905acace27cc9bb04ce2b14dc6a685b7c4f8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663063"
---
# <a name="imr_candidatewindow-notification-code"></a>\_Код уведомления КАНДИДАТЕВИНДОВ IMR

Нотфиес приложение, когда для выбранного редактора IME требуются сведения о окне кандидатов. Приложение получает эту команду через сообщение [**запроса WM \_ IME \_**](wm-ime-request.md) с параметрами параметров, как показано ниже.


```C++
LRESULT IMR_CANDIDATEWINDOW
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Задайте значение IMR \_ кандидатевиндов.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Указатель на буфер, содержащий структуру [**кандидатеформ**](/windows/win32/api/imm/ns-imm-candidateform) . Его член **двиндекс** содержит индекс к окну кандидатов, на которое есть ссылка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает ненулевое значение, если приложение заполняет структуру [**кандидатеформ**](/windows/win32/api/imm/ns-imm-candidateform) . В противном случае команда возвращает значение 0.

## <a name="remarks"></a>Комментарии

Эта команда может быть отправлена редактором IME в окно, которое очистило \_ флаг ISC шовуикандидатевиндов в обработчике сообщений [**\_ \_ SETCONTEXT редактора IME**](wm-ime-setcontext.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                 |
| Заголовок<br/>                   | <dl> <dt>IMM. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Диспетчер метода ввода](input-method-manager.md)
</dt> <dt>

[Команды диспетчера методов ввода](input-method-manager-commands.md)
</dt> <dt>

[**кандидатеформ**](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[**\_запрос IME \_ WM**](wm-ime-request.md)
</dt> <dt>

[**\_SETCONTEXT IME \_ WM**](wm-ime-setcontext.md)
</dt> </dl>

 

 




