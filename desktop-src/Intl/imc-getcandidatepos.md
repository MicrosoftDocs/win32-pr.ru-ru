---
description: Указывает окну IME для получения расположения окна кандидатов. Чтобы отправить эту команду, приложение использует \_ \_ управляющее сообщение WM IME с параметрами параметров, приведенными ниже.
ms.assetid: e582dbc2-8081-424c-a972-1a182a477293
title: Команда IMC_GETCANDIDATEPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e155a08c9d95fa2ac9f865d80b18d51120d19b28489bcad418eb4323dda39c3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107324"
---
# <a name="imc_getcandidatepos-command"></a>ИМК \_ жеткандидатепос, команда

Указывает окну IME для получения расположения окна кандидатов. Чтобы отправить эту команду, приложение использует [**\_ \_ управляющее сообщение WM IME**](wm-ime-control.md) с параметрами параметров, приведенными ниже.


```C++
LRESULT IMC_GETCANDIDATEPOS
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Задайте для параметра значение ИМК \_ жеткандидатепос.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Указатель на структуру [**кандидатеформ**](/windows/win32/api/imm/ns-imm-candidateform) , содержащую расположение окна кандидатов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает 0 в случае успеха или ненулевое значение в противном случае.

## <a name="remarks"></a>Remarks

Так как редактор IME может скорректировать расположение окна кандидатов, приложение использует эту команду для получения фактического расположения, чтобы решить, следует ли изменить расположение окна. Полученное расположение находится в координатах окна относительно окна, имеющего текущий фокус ввода.

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

[**кандидатеформ**](/windows/win32/api/imm/ns-imm-candidateform)
</dt> </dl>

 

 




