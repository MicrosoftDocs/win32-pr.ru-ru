---
title: Код уведомления CDN_SELCHANGE (Коммдлг. h)
description: Отсылается диалоговым окном открытия или сохранения в стиле обозревателя при изменении выбора в списке, отображающем содержимое текущей открытой папки или каталога.
ms.assetid: e622babf-7024-45c5-a8db-f80896f69140
keywords:
- CDN_SELCHANGE диалоговых окон кода уведомления
topic_type:
- apiref
api_name:
- CDN_SELCHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7306bf8a1cf012c70738ddf81ae9422e8d658bda33d31b7adda1d57a25629c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843265"
---
# <a name="cdn_selchange-notification-code"></a>CDN \_ Код уведомления СЕЛЧАНЖЕ

\[начиная с Windows Vista общие диалоговые окна " **открыть** " и " **сохранить как** " были заменены [диалоговым окном общих элементов](../shell/common-file-dialog.md). Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]

Отсылается диалоговым окном **открытия** или **сохранения** в стиле обозревателя при изменении выбора в списке, отображающем содержимое текущей открытой папки или каталога.

Процедура обработчика [*офнхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) получает это сообщение в виде сообщения [**WM \_ Notify**](../controls/wm-notify.md) .


```C++
#define CDN_SELCHANGE           (CDN_FIRST - 0x0001)
#define CDN_FIRST               (0U-601U)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**офнотифи**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) . структура **офнотифи** содержит структуру [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) , элемент **кода** которой указывает на сообщение уведомления о **CDN \_ селчанже** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется.

## <a name="remarks"></a>Remarks

Система отправляет это уведомление только в том случае, если диалоговое окно было создано с помощью значения **\_ обозревателя ОФН** .

Чтобы получить имя только что выбранного файла или папки, процедура-обработчик может отправить сообщение CDM- [**\_ FilePath**](cdm-getfilepath.md) или CDM- [**\_ Spec**](cdm-getspec.md) в диалоговое окно.

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

[**CDM. \_ FilePath**](cdm-getfilepath.md)
</dt> <dt>

[**CDMая \_ Спецификация**](cdm-getspec.md)
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**жетсавефиленаме**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[*офнхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[**офнотифи**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

**Зрения**
</dt> <dt>

[Библиотека общих диалоговых окон](common-dialog-box-library.md)
</dt> </dl>

