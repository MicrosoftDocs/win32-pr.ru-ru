---
description: Указывает окну редактора IME задать расположение окна состояния. Чтобы отправить эту команду, приложение использует \_ \_ управляющее сообщение WM IME с параметрами параметров, как показано ниже.
ms.assetid: d77de7ab-1fbc-42f4-829e-e9fb51668d21
title: Команда IMC_SETSTATUSWINDOWPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee41deac781f7885185df429c5b5231a36f9d5008b5754b718398e7ab4cd060a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107234"
---
# <a name="imc_setstatuswindowpos-command"></a>ИМК \_ сетстатусвиндовпос, команда

Указывает окну редактора IME задать расположение окна состояния. Чтобы отправить эту команду, приложение использует [**\_ \_ управляющее сообщение WM IME**](wm-ime-control.md) с параметрами параметров, как показано ниже.


```C++
LRESULT IMC_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Задайте для параметра значение ИМК \_ сетстатусвиндовпос.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Указатель на структуру [**точек**](/previous-versions//dd162808(v=vs.85)) , которая содержит координату x и координату y позиции окна состояния. Координаты расположены в экранных координатах относительно левого верхнего угла отображения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает 0 в случае успеха или ненулевое значение в противном случае.

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

[**\_ \_ элемент управления WM IME**](wm-ime-control.md)
</dt> </dl>

 

 
