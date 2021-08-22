---
description: Указывает окну IME указать логический шрифт, используемый для отображения промежуточных символов в окне композиции. Чтобы отправить эту команду, приложение использует \_ \_ управляющее сообщение WM IME с параметрами параметров, приведенными ниже.
ms.assetid: 17b222e7-bf57-4cdd-8475-d9a8be03ab7f
title: Команда IMC_SETCOMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ebc9f435371d4ae08b12191419c95fd53c69256064f0e90bb654e75fab922f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949275"
---
# <a name="imc_setcompositionfont-command"></a>ИМК \_ сеткомпоситионфонт, команда

Указывает окну IME указать логический шрифт, используемый для отображения промежуточных символов в окне композиции. Чтобы отправить эту команду, приложение использует [**\_ \_ управляющее сообщение WM IME**](wm-ime-control.md) с параметрами параметров, приведенными ниже.


```C++
LRESULT IMC_SETCOMPOSITIONFONT
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Задайте для параметра значение ИМК \_ сеткомпоситионфонт.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Указатель на структуру [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , содержащую сведения о логическом шрифте.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает 0 в случае успеха или ненулевое значение в противном случае.

## <a name="remarks"></a>Remarks

При обработке этой команды окно IME изменяет текущий выбранный шрифт во входном контексте.

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

[**\_ \_ элемент управления WM IME**](wm-ime-control.md)
</dt> </dl>

 

 
