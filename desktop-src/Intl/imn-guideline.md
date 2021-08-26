---
description: Уведомляет приложение, когда редактор IME собирается отобразить сообщение об ошибке или другую информацию. Приложение получает эту команду через \_ \_ сообщение с уведомлением редактора IME WM с параметрами параметров, как показано ниже.
ms.assetid: b898283a-af1a-484f-bfb8-e5d5c0ac8ee1
title: Код уведомления IMN_GUIDELINE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8bbcce8c1e7a04f4474d09f221ff2e2644e84b49d98edf09c1137604b71b226
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107104"
---
# <a name="imn_guideline-notification-code"></a>\_Код уведомления об рекомендации ИМН

Уведомляет приложение, когда редактор IME собирается отобразить сообщение об ошибке или другую информацию. Приложение получает эту команду через сообщение с [**\_ \_ уведомлением редактора IME WM**](wm-ime-notify.md) с параметрами параметров, как показано ниже.


```C++
IMN_GUIDELINE
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Задайте для параметра ИМН \_ Рекомендация.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта команда не имеет возвращаемого значения.

## <a name="remarks"></a>Remarks

Приложение обрабатывает эту команду, вызывая функцию [**иммжетгуиделине**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea) для получения сообщения об ошибке или сведений из IME.

В окне редактора IME отображается сообщение об ошибке или информационная строка в информационном окне.

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

[**иммжетгуиделине**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea)
</dt> <dt>

[**\_уведомление редактора IME WM \_**](wm-ime-notify.md)
</dt> </dl>

 

 




