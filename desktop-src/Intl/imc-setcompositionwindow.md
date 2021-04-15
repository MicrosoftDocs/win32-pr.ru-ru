---
description: Указывает окну редактора IME задать стиль окна композиции. Чтобы отправить эту команду, приложение использует \_ \_ управляющее сообщение WM IME с параметрами параметров, приведенными ниже.
ms.assetid: 19b99228-a1fc-4cd5-8f37-5462bf767f85
title: Команда IMC_SETCOMPOSITIONWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b06c53b1ff2ec343d6382dd48d0d4108cf403c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682828"
---
# <a name="imc_setcompositionwindow-command"></a>ИМК \_ сеткомпоситионвиндов, команда

Указывает окну редактора IME задать стиль окна композиции. Чтобы отправить эту команду, приложение использует [**\_ \_ управляющее сообщение WM IME**](wm-ime-control.md) с параметрами параметров, приведенными ниже.


```C++
LRESULT IMC_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Задайте для параметра значение ИМК \_ сеткомпоситионвиндов.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Указатель на структуру [**компоситионформ**](/windows/win32/api/imm/ns-imm-compositionform) , содержащую сведения о стиле.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает 0 в случае успеха или ненулевое значение в противном случае.

## <a name="remarks"></a>Комментарии

Эта команда задает стиль в текущем контексте ввода, и стиль затем применяется к каждому окну IME, которое получает этот контекст ввода.

По умолчанию окно IME имеет \_ стиль CFS Point. В этом стиле окно IME использует текущую точку курсора и клиентскую область окна при открытии любого окна композиции.

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

[**компоситионформ**](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[**\_ \_ элемент управления WM IME**](wm-ime-control.md)
</dt> </dl>

 

 




