---
description: Уведомляет приложение, когда редактор IME готов открыть окно кандидатов. Приложение получает эту команду через \_ \_ сообщение с уведомлением редактора IME WM с параметрами параметров, как показано ниже.
ms.assetid: 439ff125-2731-4eb1-8287-4ca8ace7d8ec
title: Событие IMN_OPENCANDIDATE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dbf6db7415a62b6d77925a4fb7106b70f0b42d77f922e0c1b6df76e71d10c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147637"
---
# <a name="imn_opencandidate-event"></a>\_Событие ИМН опенкандидате

Уведомляет приложение, когда редактор IME готов открыть окно кандидатов. Приложение получает эту команду через сообщение с [**\_ \_ уведомлением редактора IME WM**](wm-ime-notify.md) с параметрами параметров, как показано ниже.


```C++
IMN_OPENCANDIDATE
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Задайте для параметра значение ИМН \_ опенкандидате.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Флаг списка кандидатов. Каждый бит соответствует списку кандидатов: бит 0 в первый список, бит 1 – второй и т. д. Если указан бит 1, откроется соответствующее окно с кандидатом.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта команда не имеет возвращаемого значения.

## <a name="remarks"></a>Remarks

Приложение должно обработать эту команду, если на ней отображаются сами кандидаты. Приложение может получить список кандидатов для вывода с помощью функции [**иммжеткандидателист**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) .

По умолчанию при обработке этой команды в окне редактора IME создается окно кандидатов.

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

[**\_уведомление редактора IME WM \_**](wm-ime-notify.md)
</dt> </dl>

 

 




