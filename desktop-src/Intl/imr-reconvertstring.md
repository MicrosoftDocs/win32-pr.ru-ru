---
description: Уведомляет приложение, когда для выбранного редактора IME требуется строка для повторного преобразования. Приложение получает эту команду через \_ сообщение запроса WM IME \_ с параметрами параметров, как показано ниже.
ms.assetid: 82ef20b5-bdfa-4bde-abb4-3d14ae35c116
title: Код уведомления IMR_RECONVERTSTRING (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cbb1caeedb729b176f116a15e64879d79d519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909500"
---
# <a name="imr_reconvertstring-notification-code"></a>\_Код уведомления РЕКОНВЕРТСТРИНГ IMR

Уведомляет приложение, когда для выбранного редактора IME требуется строка для повторного преобразования. Приложение получает эту команду через сообщение [**запроса WM \_ IME \_**](wm-ime-request.md) с параметрами параметров, как показано ниже.


```C++
LRESULT IMR_RECONVERTSTRING
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Задайте значение IMR \_ реконвертстринг.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Указатель на буфер, содержащий структуру и строки [**реконвертстринг**](/windows/win32/api/imm/ns-imm-reconvertstring) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает текущую структуру строки повторного преобразования. Если параметр *lParam* имеет значение **null**, приложение возвращает размер буфера, необходимого для хранения структуры. Команда возвращает 0, если она не выполнена.

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

[**реконвертстринг**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**\_запрос IME \_ WM**](wm-ime-request.md)
</dt> </dl>

 

 




