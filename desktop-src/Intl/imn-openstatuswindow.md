---
description: Уведомляет приложение, когда редактор IME собирается создать окно состояния. Приложение получает эту команду через \_ \_ сообщение с уведомлением редактора IME WM с параметрами параметров, как показано ниже.
ms.assetid: bbd85c72-aa78-4e1d-8a7a-490650b2d782
title: Код уведомления IMN_OPENSTATUSWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca33771d1474c2f2ac78551a31545cecc2e513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683521"
---
# <a name="imn_openstatuswindow-notification-code"></a>\_Код уведомления ИМН опенстатусвиндов

Уведомляет приложение, когда редактор IME собирается создать окно состояния. Приложение получает эту команду через сообщение с [**\_ \_ уведомлением редактора IME WM**](wm-ime-notify.md) с параметрами параметров, как показано ниже.


```C++
IMN_OPENSTATUSWINDOW
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Задайте для параметра значение ИМН \_ опенстатусвиндов.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта команда не имеет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Приложение обрабатывает эту команду, чтобы отобразить окно состояния IME отдельно.

Окно редактора IME создает окно состояния при обработке этой команды и задает строки, отображаемые в окне во входном контексте. Приложения могут получать сведения о окне состояния с помощью функции [**иммжетконверсионстатус**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) .

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

[**иммжетконверсионстатус**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[**\_уведомление редактора IME WM \_**](wm-ime-notify.md)
</dt> </dl>

 

 




