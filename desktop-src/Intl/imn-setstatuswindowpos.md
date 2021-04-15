---
description: Уведомляет приложение при обновлении расположения окна состояния во входном контексте. Приложение получает эту команду через \_ \_ сообщение с уведомлением редактора IME WM с параметрами параметров следующим образом.
ms.assetid: 15e65aff-67d9-4d1a-a6a7-b921cecb3aec
title: Код уведомления IMN_SETSTATUSWINDOWPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d76a962e9cc509a6f9ffaac900b761b868f960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683365"
---
# <a name="imn_setstatuswindowpos-notification-code"></a>\_Код уведомления ИМН сетстатусвиндовпос

Уведомляет приложение при обновлении расположения окна состояния во входном контексте. Приложение получает эту команду через сообщение с [**\_ \_ уведомлением редактора IME WM**](wm-ime-notify.md) с параметрами параметров следующим образом.


```C++
IMN_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Задайте для параметра значение ИМН \_ сетстатусвиндовпос.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта команда не имеет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Приложение может получить сведения о положении окна состояния с помощью команды [**ИМК \_ жетстатусвиндовпос**](imc-getstatuswindowpos.md) .

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

[**ИМК \_ жетстатусвиндовпос**](imc-getstatuswindowpos.md)
</dt> <dt>

[**\_уведомление редактора IME WM \_**](wm-ime-notify.md)
</dt> </dl>

 

 




