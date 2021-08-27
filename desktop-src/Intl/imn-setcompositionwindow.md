---
description: Уведомляет приложение при обновлении стиля или расположения окна композиции. Приложение получает эту команду через \_ \_ сообщение с уведомлением редактора IME WM с параметрами параметров, как показано ниже.
ms.assetid: 07a9f0f6-587e-47c6-8f18-b48bdab0a541
title: Код уведомления IMN_SETCOMPOSITIONWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fed8e69c03250166e155b07d34a2ce19b5d5fd9336af6cf82133c258c2b88d46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107054"
---
# <a name="imn_setcompositionwindow-notification-code"></a>\_Код уведомления ИМН сеткомпоситионвиндов

Уведомляет приложение при обновлении стиля или расположения окна композиции. Приложение получает эту команду через сообщение с [**\_ \_ уведомлением редактора IME WM**](wm-ime-notify.md) с параметрами параметров, как показано ниже.


```C++
IMN_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Задайте для параметра значение ИМН \_ сеткомпоситионвиндов.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта команда не имеет возвращаемого значения.

## <a name="remarks"></a>Remarks

Приложение может получать сведения о форме компоновки с помощью команды [**ИМК \_ жеткомпоситионвиндов**](imc-getcompositionwindow.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                 |
| Заголовок<br/>                   | <dl> <dt>Imm. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Диспетчер метода ввода](input-method-manager.md)
</dt> <dt>

[Команды диспетчера методов ввода](input-method-manager-commands.md)
</dt> <dt>

[**ИМК \_ жеткомпоситионвиндов**](imc-getcompositionwindow.md)
</dt> <dt>

[**\_уведомление редактора IME WM \_**](wm-ime-notify.md)
</dt> </dl>

 

 




