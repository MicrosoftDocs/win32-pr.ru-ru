---
title: Сообщение WM_CHOOSEFONT_SETLOGFONT (Коммдлг. h)
description: Приложение отправляет \_ сообщение WM CHOOSEFONT \_ сетлогфонт в диалоговое окно шрифта, чтобы задать текущие сведения о логическом шрифте.
ms.assetid: ad169eca-a3ae-45bd-90df-821a93a7a764
keywords:
- WM_CHOOSEFONT_SETLOGFONT диалоговых окон сообщений
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d35c6f54679389b411417e5539382fd322c0873e6dba87fc90efb93b8be7ba1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503427"
---
# <a name="wm_choosefont_setlogfont-message"></a>\_Сообщение WM CHOOSEFONT \_ сетлогфонт

Приложение отправляет сообщение **WM \_ CHOOSEFONT \_ сетлогфонт** в диалоговое окно **шрифта** , чтобы задать текущие сведения о логическом шрифте.


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETLOGFONT      (WM_USER + 101)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , содержащую сведения о текущем логическом шрифте.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не имеет возвращаемого значения.

## <a name="remarks"></a>Remarks

При вызове функции [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) для создания диалогового окна **шрифта** можно использовать элемент **лплогфонт** структуры [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) , чтобы указать структуру [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , содержащую начальные значения для диалогового окна. Используйте сообщение **WM \_ CHOOSEFONT \_ сетлогфонт** , чтобы указать структуру **LOGFONT** с разными значениями, пока открыто диалоговое окно **Шрифт** .

Как правило, сообщение **WM \_ CHOOSEFONT \_ сетлогфонт** отправляется из процедуры-обработчика [**кфхукпрок**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) . Процедура-обработчик также может отправить сообщения [**WM \_ CHOOSEFONT \_ жетлогфонт**](wm-choosefont-getlogfont.md) и [**WM \_ CHOOSEFONT \_ сетфлагс**](wm-choosefont-setflags.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>коммдлг. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**кфхукпрок**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**WM \_ CHOOSEFONT \_ жетлогфонт**](wm-choosefont-getlogfont.md)
</dt> <dt>

[**WM \_ CHOOSEFONT \_ сетфлагс**](wm-choosefont-setflags.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Библиотека общих диалоговых окон](common-dialog-box-library.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

