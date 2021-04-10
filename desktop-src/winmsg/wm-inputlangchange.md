---
description: Отправляется в самое верхнее окно после изменения языка ввода приложения. Необходимо внести все зависящие от приложения параметры и передать сообщение функции Дефвиндовпрок, которая передает сообщение всем дочерним окнам первого уровня.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: Сообщение WM_INPUTLANGCHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0cdf04a775873e4cefe2c79269c14bd3d4da8d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144719"
---
# <a name="wm_inputlangchange-message"></a>\_Сообщение ИНПУТЛАНГЧАНЖЕ WM

Отправляется в самое верхнее окно после изменения языка ввода приложения. Необходимо внести все зависящие от приложения параметры и передать сообщение функции [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , которая передает сообщение всем дочерним окнам первого уровня. Эти дочерние окна могут передать сообщение в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , чтобы оно передавало сообщение дочерним окнам и так далее.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_INPUTLANGCHANGE              0x0051
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Кодировка нового языкового стандарта.

</dd> <dt>

*lParam* 
</dt> <dd>

Идентификатор локали ввода. Дополнительные сведения см. в разделе [языки, языковые стандарты и раскладки клавиатуры](../inputdev/about-keyboard-input.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **lResult**

Приложение должно вернуть ненулевое значение, если обрабатывает это сообщение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ инпутлангчанжерекуест**](wm-inputlangchangerequest.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
