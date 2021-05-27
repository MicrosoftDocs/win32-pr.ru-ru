---
title: Код уведомления CDN_INCLUDEITEM (Коммдлг. h)
description: Отправляется диалоговым окном Открыть или сохранить как, чтобы определить, должно ли диалоговое окно отображать элемент в списке элементов в папке оболочки.
ms.assetid: 0972a78d-e058-4bac-85bd-fbd4c3885552
keywords:
- CDN_INCLUDEITEM диалоговых окон кода уведомления
topic_type:
- apiref
api_name:
- CDN_INCLUDEITEM
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f25ea90f8eb37c829cdc86e89f6d7e8cad2312
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549259"
---
# <a name="cdn_includeitem-notification-code"></a>\_Код уведомления ИНКЛУДЕИТЕМ CDN

\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](../shell/common-file-dialog.md). Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]

Отправляется диалоговым окном **Открыть** или **Сохранить как** , чтобы определить, должно ли диалоговое окно отображать элемент в списке элементов в папке оболочки. Когда пользователь открывает папку, диалоговое окно отправляет уведомление **\_ инклудеитем CDN** для каждого элемента в папке. Это уведомление отправляется в диалоговом окне только в том случае, если был установлен флаг **ОФН \_ енаблеинклуденотифи** при создании диалогового окна.

Процедура обработчика [*офнхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) получает это сообщение в виде сообщения [**WM \_ Notify**](../controls/wm-notify.md) .


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INCLUDEITEM         (CDN_FIRST - 0x0007)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**офнотифекс**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) .

Структура [**офнотифекс**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) содержит структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , элемент **кода** которой указывает на сообщение **уведомления \_ инклудеитем CDN** .

Элемент **ПСФ** структуры [**офнотифекс**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) является указателем на интерфейс для папки, элементы которой перечисляются. Элемент **Пидл** является указателем на список идентификаторов элементов, который определяет элемент относительно папки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если процедура-обработчик [*офнхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) возвращает значение 0, это диалоговое окно исключает элемент из списка элементов.

Чтобы включить элемент, возвратите ненулевое значение из процедуры-обработчика.

## <a name="remarks"></a>Комментарии

Диалоговое окно всегда включает элементы, содержащие атрибуты **сфгао \_ FILESYSTEM** и **\_ филесисанцестор сфгао** , независимо от значения, возвращаемого **CDN \_ инклудеитем**.

## <a name="requirements"></a>Требования



| Требование | Применение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Коммдлг. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылка**
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**жетсавефиленаме**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[*офнхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[**офнотифекс**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)
</dt> <dt>

**Зрения**
</dt> <dt>

[Библиотека общих диалоговых окон](common-dialog-box-library.md)
</dt> </dl>

