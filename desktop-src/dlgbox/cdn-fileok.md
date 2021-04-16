---
title: Код уведомления CDN_FILEOK (Коммдлг. h)
description: Отсылается диалоговым окном открытия или сохранения в стиле обозревателя, когда пользователь указывает имя файла и нажимает кнопку ОК.
ms.assetid: 7f3de96f-68d8-4f40-b74f-304835f9def2
keywords:
- CDN_FILEOK диалоговых окон кода уведомления
topic_type:
- apiref
api_name:
- CDN_FILEOK
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5aef63d531b603c94369936374bc10531639254
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672815"
---
# <a name="cdn_fileok-notification-code"></a>\_Код уведомления ФИЛЕОК CDN

Отсылается диалоговым окном **открытия** или **сохранения** в стиле обозревателя, когда пользователь указывает имя файла и нажимает кнопку **ОК** .

Процедура обработчика [*офнхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) получает это сообщение в виде сообщения [**WM \_ Notify**](../controls/wm-notify.md) .


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FILEOK              (CDN_FIRST - 0x0005)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**офнотифи**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .

Структура [**офнотифи**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) содержит структуру [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) , элемент **кода** которой указывает на сообщение **уведомления \_ филеок CDN** .

Структура [**офнотифи**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) также содержит указатель на структуру [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) , член **указанный** которой указывает адрес выбранного имени файла.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если процедура-обработчик возвращает значение 0, диалоговое окно принимает указанное имя файла и закрывается.

Чтобы отклонить указанное имя файла и принудительно оставить диалоговое окно открытым, возвращайте ненулевое значение из процедуры-ловушки и вызовите функцию [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , чтобы установить ненулевое значение **\_ мсгресулт DWL** .

## <a name="remarks"></a>Комментарии

Система отправляет это уведомление только в том случае, если диалоговое окно было создано с помощью значения **\_ обозревателя ОФН** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Коммдлг. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**жетсавефиленаме**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[*офнхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[**офнотифи**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

**Зрения**
</dt> <dt>

[Библиотека общих диалоговых окон](common-dialog-box-library.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**\_уведомление WM**](../controls/wm-notify.md)
</dt> </dl>

 

