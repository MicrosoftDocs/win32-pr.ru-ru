---
title: Сообщение WM_CHOOSEFONT_GETLOGFONT (Коммдлг. h)
description: Приложение отправляет \_ сообщение WM CHOOSEFONT \_ жетлогфонт в диалоговое окно шрифта для получения сведений о текущем выборе шрифта пользователем.
ms.assetid: afbf953a-13dd-409b-a988-f1426c8bbd31
keywords:
- WM_CHOOSEFONT_GETLOGFONT диалоговых окон сообщений
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_GETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fb429c3cd66af28485edf2979d2efbe50b3205a2142e963c8c3bb51ef5713f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280436"
---
# <a name="wm_choosefont_getlogfont-message"></a>\_Сообщение WM CHOOSEFONT \_ жетлогфонт

Приложение отправляет сообщение **WM \_ CHOOSEFONT \_ жетлогфонт** в диалоговое окно **шрифта** для получения сведений о текущем выборе шрифта пользователем.


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_GETLOGFONT      (WM_USER + 1)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , которая получает сведения о текущем выборе шрифта пользователем.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="remarks"></a>Remarks

Функция [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) создает диалоговое окно **шрифта** . Когда пользователь закрывает диалоговое окно « **Шрифт** », функция **ChooseFont** возвращает сведения о выборе шрифта пользователем в структуре [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) . Элемент **лплогфонт** структуры **CHOOSEFONT** является указателем на структуру [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

Используйте сообщение **WM \_ CHOOSEFONT \_ жетлогфонт** для получения сведений о текущем выборе шрифта пользователя, когда открыто диалоговое окно **Шрифт** . Например, если включить кнопку **Применить** в диалоговом окне **Шрифт** , отправьте сообщение, чтобы получить сведения о шрифте, которые будут применены к текущему выделению текста.

Как правило, вы включаете процедуру обработчика [*кфхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) для обработки [**\_ командных сообщений WM**](/windows/desktop/menurc/wm-command) для кнопки **Применить** . Когда пользователь нажимает кнопку " **Применить** ", процедура-обработчик отправляет сообщение **WM \_ CHOOSEFONT \_ жетлогфонт** в диалоговое окно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>коммдлг. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылка**
</dt> <dt>

[**кфхукпрок**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**\_команда WM**](/windows/desktop/menurc/wm-command)
</dt> <dt>

**Зрения**
</dt> <dt>

[Библиотека общих диалоговых окон](common-dialog-box-library.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

