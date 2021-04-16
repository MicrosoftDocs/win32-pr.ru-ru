---
description: Уведомляет приложение, когда выбранному РЕДАКТОРу требуется информация о шрифте, используемом окном композиции. Приложение получает эту команду через \_ сообщение запроса WM IME \_ с параметрами, как показано ниже.
ms.assetid: 46bb71ee-8dc9-4ef0-bc4e-59866c122bf7
title: Код уведомления IMR_COMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be2751944e451475fd0bde9a34d8902dcaf30e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683363"
---
# <a name="imr_compositionfont-notification-code"></a>\_Код уведомления КОМПОСИТИОНФОНТ IMR

Уведомляет приложение, когда выбранному РЕДАКТОРу требуется информация о шрифте, используемом окном композиции. Приложение получает эту команду через сообщение [**запроса WM \_ IME \_**](wm-ime-request.md) с параметрами, как показано ниже.


```C++
LRESULT IMR_COMPOSITIONFONT
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Задайте значение IMR \_ компоситионфонт.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Указатель на буфер, содержащий структуру [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) . Приложение заполняет значения для текущего окна композиции.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает ненулевое значение, если приложение заполняет структуру [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) . В противном случае команда возвращает значение 0.

## <a name="remarks"></a>Комментарии

Эта команда может быть отправлена редактором IME в окно, которое очистило \_ флаг ШОВУИКОМПОСИТИОНВИНДОВ ISC в обработчике сообщений [**\_ \_ SETCONTEXT редактора IME**](wm-ime-setcontext.md) .

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

[**\_запрос IME \_ WM**](wm-ime-request.md)
</dt> <dt>

[**\_SETCONTEXT IME \_ WM**](wm-ime-setcontext.md)
</dt> </dl>

 

 
