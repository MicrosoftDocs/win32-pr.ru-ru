---
description: Отправляется в самое верхнее окно после изменения языка ввода приложения. Необходимо внести все зависящие от приложения параметры и передать сообщение функции Дефвиндовпрок, которая передает сообщение всем дочерним окнам первого уровня.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: Сообщение WM_INPUTLANGCHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e2ceb943290fceab13bf6f22c3d9dafbac27a8
ms.sourcegitcommit: 40dddb65cba5c5470631f1f4c78218edf7e515de
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2021
ms.locfileid: "108332409"
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
  
Тип: **wParam**

[Кодовая страница](../Intl/code-pages.md) нового языкового стандарта.

</dd> <dt>

*lParam*

</dt> <dd>
 
Тип: **lParam** .

Идентификатор языка ввода **HKL** . Дополнительные сведения см. в разделе [языки, языковые стандарты и раскладки клавиатуры](../inputdev/about-keyboard-input.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **lResult**

Приложение должно вернуть ненулевое значение, если обрабатывает это сообщение.

## <a name="remarks"></a>Комментарии

Вы можете получить [имя локали](../Intl/locale-names.md) клавиатуры с помощью функции [лЦидтолокаленаме](/windows/win32/api/winnls/nf-winnls-lcidtolocalename) . С помощью имени языкового стандарта можно использовать [современные функции языкового стандарта](/windows/win32/intl/calling-the--locale-name--functions):

```cpp
case WM_INPUTLANGCHANGE:
{
    HKL hkl = (HKL)lParam;
    WCHAR localeName[LOCALE_NAME_MAX_LENGTH];
    LCIDToLocaleName(MAKELCID(LOWORD(hkl), SORT_DEFAULT), localeName, LOCALE_NAME_MAX_LENGTH, 0);

    WCHAR lang[9];
    GetLocaleInfoEx(localeName, LOCALE_SISO639LANGNAME2, lang, 9);
}
```

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |

## <a name="see-also"></a>См. также раздел

**Ссылка**

- [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
- [**WM \_ инпутлангчанжерекуест**](wm-inputlangchangerequest.md)

**Основные понятия**

- [Windows](windows.md) 
