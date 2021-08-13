---
title: Сообщение WM_VSCROLLCLIPBOARD (Winuser. h)
description: Посылается владельцу буфера обмена в окне средства просмотра буфера обмена, когда в буфере обмена содержатся данные в \_ формате CF овнердисплай, а в вертикальной полосе прокрутки появляется событие.
ms.assetid: 17bd32c4-1b07-42b7-b269-f517e3ec13f3
keywords:
- WM_VSCROLLCLIPBOARD Exchange данных сообщений
topic_type:
- apiref
api_name:
- WM_VSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbcf634870ce232543cd20ccd42c9e8ca255705810e81af39cc6e81f8e41658d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544879"
---
# <a name="wm_vscrollclipboard-message"></a>\_Сообщение ВСКРОЛЛКЛИПБОАРД WM

Посылается владельцу буфера обмена в окне средства просмотра буфера обмена, когда в буфере обмена содержатся данные в формате [**CF \_ овнердисплай**](standard-clipboard-formats.md) , а в вертикальной полосе прокрутки появляется событие. Владелец должен прокручивать изображение в буфере обмена и обновлять значения полосы прокрутки.


```C++
#define WM_VSCROLLCLIPBOARD             0x030A
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Маркер окна средства просмотра буфера обмена.

</dd> <dt>

*lParam* 
</dt> <dd>

Слово *lParam* в низком порядке указывает на событие полосы прокрутки. Этот параметр может принимать одно из указанных ниже значений.



| Значение                                                                                                                                                                                                                         | Значение                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <dt>**SB \_ 7 НИЖНИх**</dt> <dt></dt> </dl>                      | Прокрутите вниз вправо.<br/>                                                                 |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ ЕНДСКРОЛЛ**</dt> <dt>8</dt> </dl>             | Завершить прокрутку.<br/>                                                                            |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ ЛИНЕДОВН**</dt> <dt>1</dt> </dl>                | Прокрутить на одну строку вниз.<br/>                                                                  |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**SB \_**</dt>Отметка <dt>0</dt> </dl>                      | Прокрутить на одну строку вверх.<br/>                                                                    |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB \_ PAGEDOWN**</dt> <dt>3</dt> </dl>                | Прокрутить на одну страницу вниз.<br/>                                                                  |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**SB \_ PAGEUP**</dt> <dt>2</dt> </dl>                      | Прокрутка на одну страницу вверх.<br/>                                                                    |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ СУМБПОСИТИОН**</dt> <dt>4</dt> </dl> | Прокрутить к абсолютному положению. Текущая позицией задается в виде слова в высоком порядке.<br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <dt>**SB \_ Первые**</dt> <dt>6</dt> </dl>                               | Прокрутить к верхнему левому краю.<br/>                                                                  |



 

Слово *lParam* с высоким приоритетом задает текущую точку прокрутки, если неупорядоченное слово *lParam* является **SB \_ сумбпоситион**; в противном случае не используется слово с высоким порядком *lParam* .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Remarks

Владелец буфера обмена может использовать функцию [**скроллвиндов**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) для прокрутки изображения в окне средства просмотра буфера обмена и сделать недействительным соответствующий регион.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылка**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Зрения**
</dt> <dt>

[Буфер обмена](clipboard.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**скроллвиндов**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)
</dt> </dl>

 

