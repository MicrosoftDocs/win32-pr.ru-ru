---
title: Сообщение WM_CHOOSEFONT_SETFLAGS (Коммдлг. h)
description: Приложение отправляет \_ сообщение WM CHOOSEFONT \_ сетфлагс в диалоговое окно шрифта, чтобы задать параметры вывода для этого диалогового окна.
ms.assetid: 945ebc07-440d-4466-8255-ad344bdc568a
keywords:
- WM_CHOOSEFONT_SETFLAGS диалоговых окон сообщений
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETFLAGS
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d77290dfb3668e24d3586cf6d742b524e05fb07979de7c8d45f39998aca9708
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726084"
---
# <a name="wm_choosefont_setflags-message"></a>\_Сообщение WM CHOOSEFONT \_ сетфлагс

Приложение отправляет сообщение **WM \_ CHOOSEFONT \_ сетфлагс** в диалоговое окно **шрифта** , чтобы задать параметры вывода для этого диалогового окна.


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETFLAGS        (WM_USER + 102)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) , которая содержит новые параметры в элементе **flags** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Функция [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) создает диалоговое окно **шрифта** и использует структуру [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) для указания начальных значений для элемента **flags** . Используйте сообщение **WM \_ CHOOSEFONT \_ сетфлагс** , чтобы указать различные значения для элемента **flags** , пока открыто диалоговое окно **Шрифт** .

Как правило, вы должны отправить сообщение **WM \_ CHOOSEFONT \_ сетфлагс** из процедуры-обработчика [**кфхукпрок**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>коммдлг. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**кфхукпрок**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

**Зрения**
</dt> <dt>

[Библиотека общих диалоговых окон](common-dialog-box-library.md)
</dt> </dl>

 

