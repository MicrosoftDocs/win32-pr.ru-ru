---
title: Сообщение СЕТРГБСТРИНГ (Коммдлг. h)
description: Процедура-обработчик диалогового окна цвета, Кчукпрок, может отправить в диалоговое окно зарегистрированное сообщение СЕТРГБСТРИНГ, чтобы задать текущее выделение цветом.
ms.assetid: 02d36248-be75-4552-853f-6ac3ec034ebe
keywords:
- Диалоговые окна сообщения СЕТРГБСТРИНГ
topic_type:
- apiref
api_name:
- SETRGBSTRING
- SETRGBSTRINGA
- SETRGBSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea5489aaa6fafcaa19a97a44d81fd85abb178d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803089"
---
# <a name="setrgbstring-message"></a>Сообщение СЕТРГБСТРИНГ

Процедура-обработчик диалогового окна **цвета** , [*кчукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), может отправить в диалоговое окно зарегистрированное сообщение **сетргбстринг** , чтобы задать текущее выделение цветом.


```C++
#define SETRGBSTRING TEXT("commdlg_SetRGBColor")
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Значение RGB цвета, которое необходимо выбрать в диалоговом окне " **Цвет** ". С помощью макроса [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) можно задать красный, зеленый и синий интенситиес в значении цвета RGB.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не имеет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Если параметр *lParam* соответствует одному из основных цветов или одному из 16 пользовательских цветов, то процедура выбора этого цвета выбирается в диалоговом окне. Процедура также обновляет все элементы управления в пользовательском расширении цвета диалогового окна **Цвет** , если оно открыто.

Если параметр *lParam* не соответствует базовому или пользовательскому цвету, то процедура диалогового окна не изменяет текущий выбор цвета, но обновляет элементы управления пользовательского цвета, если они видимы.

## <a name="examples"></a>Примеры

В следующем примере кода возвращается идентификатор сообщения **сетргбстринг** , а затем выбирается синий цвет.


```
UINT uiSetRGB;

uiSetRGB = RegisterWindowMessage(SETRGBSTRING);

SendMessage(hdlg, uiSetRGB, 0, (LPARAM) RGB(0, 0, 255)); 
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Коммдлг. h (включение Windows. h)</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Сетргбстрингв** (Юникод) и **сетргбстринга** (ANSI)<br/>                                      |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**регистервиндовмессаже**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

**Зрения**
</dt> <dt>

[Библиотека общих диалоговых окон](common-dialog-box-library.md)
</dt> </dl>

 

