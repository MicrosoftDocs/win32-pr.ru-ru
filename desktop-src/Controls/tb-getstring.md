---
title: Сообщение TB_GETSTRING (Коммктрл. h)
description: Извлекает строку из пула строк панели инструментов.
ms.assetid: a5f80c16-bc6d-466d-8ec6-77451432148e
keywords:
- Элементы управления Windows для TB_GETSTRING сообщений
topic_type:
- apiref
api_name:
- TB_GETSTRING
- TB_GETSTRINGA
- TB_GETSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 465ad2546397fa31c33d6a52b4989902c979d91d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071381"
---
# <a name="tb_getstring-message"></a>Сообщение о GETSTRING (ТБ) \_

Извлекает строку из пула строк панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) указывает длину буфера *lParam* в байтах. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает индекс строки.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на буфер, используемый для возврата строки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает длину строки в случае успеха или значение-1 в противном случае.

## <a name="remarks"></a>Комментарии

Это сообщение возвращает указанную строку из пула строк панели инструментов. Он не обязательно соответствует текстовой строке, отображаемой в данный момент кнопкой. Чтобы получить текущую текстовую строку кнопки, отправьте на панель инструментов сообщение [**\_ Жетбуттонтекст (ТБ**](tb-getbuttontext.md) ).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТБ \_ ЖЕТСТРИНГВ** (Юникод) и **ТБ- \_ строка** (ANSI)<br/>                 |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**\_ADDSTRING ТБ**](tb-addstring.md)
</dt> <dt>

[**\_АДДБУТТОНС ТБ**](tb-addbuttons.md)
</dt> <dt>

[**\_ИНСЕРТБУТТОН ТБ**](tb-insertbutton.md)
</dt> </dl>

 

