---
title: Сообщение ХЕЛПМСГСТРИНГ (Коммдлг. h)
description: Общее диалоговое окно отправляет зарегистрированное сообщение ХЕЛПМСГСТРИНГ в процедуру окна своего окна-владельца, когда пользователь нажимает кнопку "Справка".
ms.assetid: 21c0fcf5-785b-4005-8133-e48347f991a8
keywords:
- Диалоговые окна сообщения ХЕЛПМСГСТРИНГ
topic_type:
- apiref
api_name:
- HELPMSGSTRING
- HELPMSGSTRINGA
- HELPMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8a446164bb7ae51d36d1a89219f6c3b84eff74b9af3a40c2121b3bd205a581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741744"
---
# <a name="helpmsgstring-message"></a>Сообщение ХЕЛПМСГСТРИНГ

Общее диалоговое окно отправляет зарегистрированное сообщение **хелпмсгстринг** в процедуру окна своего окна-владельца, когда пользователь нажимает кнопку " **Справка** ".


```C++
#define HELPMSGSTRING TEXT("commdlg_help")
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Маркер общего диалогового окна.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру инициализации для общего диалогового окна. Эта структура может быть структурой [**чусеколор**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1), [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), [**финдреплаце**](/windows/win32/api/commdlg/ns-commdlg-findreplacea), [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea), [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) или [**пажесетупдлг**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не имеет возвращаемого значения.

## <a name="remarks"></a>Remarks

Чтобы получить идентификатор сообщения, отправленного диалоговым окном, необходимо указать константу **хелпмсгстринг** в вызове функции [**регистервиндовмессаже**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) .

При создании диалогового окна используйте элемент **хвндовнер** структуры инициализации, чтобы указать окно для получения сообщений **хелпмсгстринг** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>коммдлг. h (включает Windows. h)</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Хелпмсгстрингв** (Юникод) и **хелпмсгстринга** (ANSI)<br/>                                    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**CDN \_ СПРАВКА**](cdn-help.md)
</dt> <dt>

[**чусеколор**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**финдреплаце**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga)
</dt> <dt>

[**пажесетупдлг**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[**регистервиндовмессаже**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Зрения**
</dt> <dt>

[Библиотека общих диалоговых окон](common-dialog-box-library.md)
</dt> </dl>

 

