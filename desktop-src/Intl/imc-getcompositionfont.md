---
description: Указывает окну редактора IME получить логический шрифт, используемый для отображения промежуточных символов в окне композиции. Чтобы отправить эту команду, приложение использует \_ \_ управляющее сообщение WM IME с параметрами параметров, приведенными ниже.
ms.assetid: 43db70b6-f8bc-4241-9096-5d91fd1e332b
title: Команда IMC_GETCOMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696d9809cadbe4f2c0e632719401e882777888dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263241"
---
# <a name="imc_getcompositionfont-command"></a>ИМК \_ жеткомпоситионфонт, команда

Указывает окну редактора IME получить логический шрифт, используемый для отображения промежуточных символов в окне композиции. Чтобы отправить эту команду, приложение использует [**\_ \_ управляющее сообщение WM IME**](wm-ime-control.md) с параметрами параметров, приведенными ниже.


```C++
LRESULT IMC_GETCOMPOSITIONFONT
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Задайте для параметра значение ИМК \_ жеткомпоситионфонт.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Указатель на структуру [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , которая получает сведения о логическом шрифте.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает 0 в случае успеха или ненулевое значение в противном случае.

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
</dt> </dl>

 

 
