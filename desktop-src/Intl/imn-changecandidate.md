---
description: Уведомляет приложение, когда редактор IME собирается изменить содержимое окна-кандидата. Приложение получает эту команду через \_ \_ сообщение с уведомлением редактора IME WM с параметрами параметров, как показано ниже.
ms.assetid: 0a276f9c-cece-4fa6-b71a-ba0daad5ca05
title: Код уведомления IMN_CHANGECANDIDATE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 599f064b05f4fa0bda205825d623d13eec39334683fbe2b69f1c8b7b2997026b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949255"
---
# <a name="imn_changecandidate-notification-code"></a>\_Код уведомления ИМН чанжекандидате

Уведомляет приложение, когда редактор IME собирается изменить содержимое окна-кандидата. Приложение получает эту команду через сообщение с [**\_ \_ уведомлением редактора IME WM**](wm-ime-notify.md) с параметрами параметров, как показано ниже.


```C++
IMN_CHANGECANDIDATE
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Задайте для параметра значение ИМН \_ чанжекандидате.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Флаг списка кандидатов. Каждый бит соответствует списку кандидатов: бит 0 — первому списку, бит 1 — второму списку и т. д. Если указан бит 1, соответствующее окно-кандидата будет изменено.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта команда не имеет возвращаемого значения.

## <a name="remarks"></a>Remarks

Приложение должно обработать эту команду, если на ней отображаются сами кандидаты.

Окно IME изменяет внешний вид окна кандидатов при обработке этой команды. Приложение может получать сведения о системном окне с помощью [**иммжеткандидателисткаунт**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta) и [**иммжеткандидателист**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) .

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

[**иммжеткандидателист**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[**иммжеткандидателисткаунт**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)
</dt> <dt>

[**\_уведомление редактора IME WM \_**](wm-ime-notify.md)
</dt> </dl>

 

 




