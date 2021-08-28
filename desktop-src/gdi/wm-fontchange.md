---
description: Приложение отправляет \_ сообщение WM фонтчанже всем окнам верхнего уровня в системе после изменения пула ресурсов шрифтов.
ms.assetid: 4774308e-2f18-4a35-a769-56871f3c29a2
title: Сообщение WM_FONTCHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c88edaf2db356fea2b92ce05769360ac9c8664e913ff6e5a05daaf245d1204
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119399934"
---
# <a name="wm_fontchange-message"></a>\_Сообщение ФОНТЧАНЖЕ WM

Приложение отправляет сообщение **WM \_ фонтчанже** всем окнам верхнего уровня в системе после изменения пула ресурсов шрифтов.

Чтобы отправить это сообщение, вызовите функцию [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) со следующими параметрами.


```C++
SendMessage( 
  (HWND)  hWnd,              
  WM_FONTCHANGE,            
  (WPARAM)  wParam,          
  (LPARAM)  lParam            
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="remarks"></a>Remarks

Приложение, добавляющее или удаляющее шрифты из системы (например, с помощью функции [**аддфонтресаурце**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) или [**ремовефонтресаурце**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) ), должно отправить это сообщение всем окнам верхнего уровня.

Чтобы отправить сообщение **WM \_ фонтчанже** всем окнам верхнего уровня, приложение может вызвать функцию **SendMessage** с параметром *HWND* , для которого установлено значение HWND \_ Broadcast.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о шрифтах и тексте](fonts-and-text.md)
</dt> <dt>

[Шрифт и текстовые сообщения](font-and-text-messages.md)
</dt> <dt>

[**аддфонтресаурце**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)
</dt> <dt>

[**ремовефонтресаурце**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)
</dt> </dl>

 

 
