---
title: Сообщение WM_HSCROLLCLIPBOARD (Winuser. h)
description: Отправляется в окно просмотра владельцу буфера обмена.
ms.assetid: 73558de6-a822-40f7-9eb2-47ea5afd4e6e
keywords:
- Обмен данными с сообщениями WM_HSCROLLCLIPBOARD
topic_type:
- apiref
api_name:
- WM_HSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34ee33709601b483258ae0aec4873c47fa69a00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492195"
---
# <a name="wm_hscrollclipboard-message"></a>\_Сообщение ХСКРОЛЛКЛИПБОАРД WM

Отправляется в окно просмотра владельцу буфера обмена. Это происходит, когда буфер обмена содержит данные в формате [**CF \_ овнердисплай**](standard-clipboard-formats.md) и событие возникает в горизонтальной полосе прокрутки окна буфера просмотра. Владелец должен прокручивать изображение в буфере обмена и обновлять значения полосы прокрутки.


```C++
#define WM_HSCROLLCLIPBOARD             0x030E
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Маркер окна средства просмотра буфера обмена.

</dd> <dt>

*lParam* 
</dt> <dd>

Слово *lParam* в низком порядке указывает на событие полосы прокрутки. Этот параметр может принимать одно из указанных ниже значений. Слово *lParam* в высоком порядке задает текущую точку прокрутки, если неупорядоченное слово *lParam* является **SB \_ сумбпоситион**; в противном случае слово с высоким порядком не используется.



| Значение                                                                                                                                                                                                                         | Значение                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ ЕНДСКРОЛЛ**</dt> <dt>8</dt> </dl>             | Завершить прокрутку.<br/>                                                                            |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <dt>**SB \_ СЛЕВА**</dt> <dt>6</dt> </dl>                            | Прокрутить к верхнему левому краю.<br/>                                                                  |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <dt>**SB \_ СПРАВА**</dt> <dt>7</dt> </dl>                         | Прокрутите вниз вправо.<br/>                                                                 |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <dt>**SB \_ ЛИНЕЛЕФТ**</dt> <dt>0</dt> </dl>                | Прокрутка влево на одну единицу.<br/>                                                              |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <dt>**SB \_ ЛИНЕРИГХТ**</dt> <dt>1</dt> </dl>             | Выполняет прокрутку вправо на одну единицу.<br/>                                                             |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <dt>**SB \_ ПАЖЕЛЕФТ**</dt> <dt>2</dt> </dl>                | Прокрутка влево по ширине окна.<br/>                                               |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <dt>**SB \_ ПАЖЕРИГХТ**</dt> <dt>3</dt> </dl>             | Прокрутка вправо по ширине окна.<br/>                                              |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ СУМБПОСИТИОН**</dt> <dt>4</dt> </dl> | Прокрутить к абсолютному положению. Текущая позицией задается в виде слова в высоком порядке.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Комментарии

Владелец буфера обмена может использовать функцию [**скроллвиндов**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) для прокрутки изображения в окне средства просмотра буфера обмена и сделать недействительным соответствующий регион.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
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

 

