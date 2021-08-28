---
description: Уведомляет приложение, когда выбранному РЕДАКТОРу требуется информация о координатах символа в строке композиции. Приложение получает эту команду через \_ сообщение запроса WM IME \_ с параметрами параметров, как показано ниже.
ms.assetid: cae7e5b3-8aaf-452d-80df-fb0ae04a342c
title: Код уведомления IMR_QUERYCHARPOSITION (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6a37679dce6a17d5687aeed1c8fbd1d5c8bf6651b3cfc597cfdfc2e419ecba3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948771"
---
# <a name="imr_querycharposition-notification-code"></a>\_Код уведомления КУЕРИЧАРПОСИТИОН IMR

Уведомляет приложение, когда выбранному РЕДАКТОРу требуется информация о координатах символа в строке композиции. Приложение получает эту команду через сообщение [**запроса WM \_ IME \_**](wm-ime-request.md) с параметрами параметров, как показано ниже.


```C++
LRESULT IMR_QUERYCHARPOSITION
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Задайте значение IMR \_ куеричарпоситион.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Указатель на структуру [**имечарпоситион**](/windows/win32/api/imm/ns-imm-imecharposition) , содержащую позиции символа в окне композиции.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает ненулевое значение, если приложение заполняет структуру [**имечарпоситион**](/windows/win32/api/imm/ns-imm-imecharposition) . В противном случае команда возвращает значение 0.

## <a name="remarks"></a>Remarks

Приложение, которое рисует строку композиции, а не полагается на IME, отвечает за заполнение всех элементов структуры [**имечарпоситион**](/windows/win32/api/imm/ns-imm-imecharposition) . В противном случае приложение должно передать команду в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) или [**иммисуимессаже**](/windows/desktop/api/Imm/nf-imm-immisuimessagea) , если она имеет собственное окно пользовательского интерфейса IME.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                 |
| Заголовок<br/>                   | <dl> <dt>Imm. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Диспетчер метода ввода](input-method-manager.md)
</dt> <dt>

[Команды диспетчера методов ввода](input-method-manager-commands.md)
</dt> <dt>

[**имечарпоситион**](/windows/win32/api/imm/ns-imm-imecharposition)
</dt> <dt>

[**иммисуимессаже**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> <dt>

[**\_запрос IME \_ WM**](wm-ime-request.md)
</dt> </dl>

 

 
