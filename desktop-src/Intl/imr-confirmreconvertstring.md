---
description: Уведомляет приложение, когда редактору IME требуется изменить структуру РЕКОНВЕРТСТРИНГ. Приложение получает эту команду через \_ сообщение запроса WM IME \_ с параметрами параметров, как показано ниже.
ms.assetid: 035a7072-d292-4883-bc3e-d1e9ed64d9ec
title: Код уведомления IMR_CONFIRMRECONVERTSTRING (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a0fd1c38c7552d09489c51b9acc897f679aa3a218e86bbba222225fcff57e90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948801"
---
# <a name="imr_confirmreconvertstring-notification-code"></a>\_Код уведомления КОНФИРМРЕКОНВЕРТСТРИНГ IMR

Уведомляет приложение, когда редактору IME требуется изменить структуру [**реконвертстринг**](/windows/win32/api/imm/ns-imm-reconvertstring) . Приложение получает эту команду через сообщение [**запроса WM \_ IME \_**](wm-ime-request.md) с параметрами параметров, как показано ниже.


```C++
LRESULT IMR_CONFIRMRECONVERTSTRING
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Задайте значение IMR \_ конфирмреконвертстринг.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Указатель на структуру [**реконвертстринг**](/windows/win32/api/imm/ns-imm-reconvertstring) из редактора IME. Дополнительные сведения см. в разделе "Замечания".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение, если приложение принимает измененную структуру [**реконвертстринг**](/windows/win32/api/imm/ns-imm-reconvertstring) . В противном случае команда возвращает 0, а редактор IME использует исходную структуру **реконвертстринг** .

## <a name="remarks"></a>Remarks

Приложение заполняет структуру [**реконвертстринг**](/windows/win32/api/imm/ns-imm-reconvertstring) при получении команды [IMR \_ реконвертстринг](imr-reconvertstring.md) .

После того как приложение обработало [ \_ реконвертстринг IMR](imr-reconvertstring.md), редактор IME может изменить структуру [**реконвертстринг**](/windows/win32/api/imm/ns-imm-reconvertstring) . Редактор IME отправляет \_ запрос WM IME \_ с помощью **IMR \_ конфирмреконвертстринг** для подтверждения изменений в структуре **реконвертстринг** . Если приложение возвращает **true** для **IMR \_ конфирмреконвертстринг**, редактор IME создает новую строку композиции на основе структуры **реконвертстринг** для команды **IMR \_ конфирмреконвертстринг** . Если приложение возвращает **значение false** для **\_ КОНФИРМРЕКОНВЕРТСТРИНГА IMR**, редактор IME создает новую строку композиции на основе исходной структуры **реконвертстринг** , заданной приложением в \_ команде IMR реконвертстринг.

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

[\_РЕКОНВЕРТСТРИНГ IMR](imr-reconvertstring.md)
</dt> <dt>

[**реконвертстринг**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**\_запрос IME \_ WM**](wm-ime-request.md)
</dt> </dl>

 

 




