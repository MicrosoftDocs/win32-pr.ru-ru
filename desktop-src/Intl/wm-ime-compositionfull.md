---
description: Отправляется в приложение, когда окно IME не находит место для расширения области окна композиции. Окно получает это сообщение через функцию WindowProc.
ms.assetid: d81d6438-c470-4ae5-8016-8d816bcba9b8
title: Сообщение WM_IME_COMPOSITIONFULL (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 954a5f91283ca5c4944c274d422508ef0b91b55b8acc34f790cf446f93a598ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811494"
---
# <a name="wm_ime_compositionfull-message"></a>\_Сообщение компоситионфулл редактора IME WM \_

Отправляется в приложение, когда окно IME не находит место для расширения области окна композиции. Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,
  WM_IME_COMPOSITIONFULL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a>Параметры

Это сообщение не содержит параметров.

<dl></dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не имеет возвращаемого значения.

## <a name="remarks"></a>Remarks

Для указания способа отображения окна приложение должно использовать команду [ИМК \_ сеткомпоситионвиндов](imc-setcompositionwindow.md) .

Окно IME, а не редактор IME, отправляет это сообщение уведомления функцией [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Диспетчер метода ввода](input-method-manager.md)
</dt> <dt>

[Сообщения диспетчера методов ввода](input-method-manager-messages.md)
</dt> <dt>

[ИМК \_ сеткомпоситионвиндов](imc-setcompositionwindow.md)
</dt> </dl>

 

 
