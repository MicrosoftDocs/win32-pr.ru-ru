---
description: Отправляется в приложение, когда операционная система собирается изменить текущий редактор IME. Окно получает это сообщение через функцию WindowProc.
ms.assetid: 5559b3ab-8d81-4f33-b0af-d05489371328
title: Сообщение WM_IME_SELECT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940858e12c616b1d6281c23633b2f0f5e9657a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682723"
---
# <a name="wm_ime_select-message"></a>\_Выбор сообщения для редактора IME WM \_

Отправляется в приложение, когда операционная система собирается изменить текущий редактор IME. Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,       
 WM_IME_SELECT,   
 WPARAM wParam,   
 LPARAM lParam    
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HWND* 
</dt> <dd>

Маркер для окна.

</dd> <dt>

*wParam* 
</dt> <dd>

Индикатор выделения. Этот параметр указывает **значение true** , если выбран указанный редактор IME. Параметр имеет значение **false** , если указанный редактор IME больше не выбран.

</dd> <dt>

*lParam* 
</dt> <dd>

Идентификатор языка ввода, связанный с редактором IME.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не имеет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Приложение, создавшее окно IME, должно передать это сообщение в это окно, чтобы он мог получить маркер раскладки клавиатуры для вновь выбранного редактора IME.

Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  обрабатывает это сообщение, передавая сведения в окно IME по умолчанию.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Диспетчер метода ввода](input-method-manager.md)
</dt> <dt>

[Сообщения диспетчера методов ввода](input-method-manager-messages.md)
</dt> </dl>

 

 
