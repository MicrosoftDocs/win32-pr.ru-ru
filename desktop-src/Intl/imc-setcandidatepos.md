---
description: Указывает окну IME задать расположение окна кандидатов. Чтобы отправить эту команду, приложение использует \_ \_ управляющее сообщение WM IME с параметрами параметров, приведенными ниже.
ms.assetid: 7a2f9958-4a4e-462a-9737-e7796fd90216
title: Команда IMC_SETCANDIDATEPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8ac05890e4c720c5b671faa7f20a68a96b24a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810409"
---
# <a name="imc_setcandidatepos-command"></a>ИМК \_ сеткандидатепос, команда

Указывает окну IME задать расположение окна кандидатов. Чтобы отправить эту команду, приложение использует [**\_ \_ управляющее сообщение WM IME**](wm-ime-control.md) с параметрами параметров, приведенными ниже.


```C++
LRESULT IMC_SETCANDIDATEPOS
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Задайте для параметра значение ИМК \_ сеткандидатепос.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Указатель на структуру [**кандидатеформ**](/windows/win32/api/imm/ns-imm-candidateform) , которая содержит координату x и координату y для окна кандидатов. Приложение должно установить элемент **двиндекс** этой структуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает 0 в случае успеха или ненулевое значение в противном случае.

## <a name="remarks"></a>Комментарии

Эта команда предназначена для приложений, которые отображают собственные символы композиции, но используют окно IME для вывода кандидатов.

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

[**кандидатеформ**](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[**\_ \_ элемент управления WM IME**](wm-ime-control.md)
</dt> </dl>

 

 




