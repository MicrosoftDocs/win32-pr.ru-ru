---
description: Уведомляет приложение при обновлении режима преобразования входного контекста. Приложение получает эту команду через \_ \_ сообщение с уведомлением редактора IME WM с параметрами параметров, как показано ниже.
ms.assetid: 62bb9717-cc41-4e34-af1a-ff41324bd3a9
title: Код уведомления IMN_SETCONVERSIONMODE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff970f5800dee660948bce84a8862f8da93b7390b3742c0de9c9cbdb21d9d7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146106"
---
# <a name="imn_setconversionmode-notification-code"></a>\_Код уведомления ИМН сетконверсионмоде

Уведомляет приложение при обновлении режима преобразования входного контекста. Приложение получает эту команду через сообщение с [**\_ \_ уведомлением редактора IME WM**](wm-ime-notify.md) с параметрами параметров, как показано ниже.


```C++
IMN_SETCONVERSIONMODE
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Задайте для параметра значение ИМН \_ сетконверсионмоде.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта команда не имеет возвращаемого значения.

## <a name="remarks"></a>Remarks

Приложение может получать сведения о режиме преобразования с помощью функции [**иммжетконверсионстатус**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) .

## <a name="requirements"></a>Requirements (Требования)



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

[**иммжетконверсионстатус**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[**\_уведомление редактора IME WM \_**](wm-ime-notify.md)
</dt> </dl>

 

 




