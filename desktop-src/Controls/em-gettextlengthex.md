---
title: Сообщение EM_GETTEXTLENGTHEX (RichEdit. h)
description: Вычисляет длину текста различными способами. Обычно он вызывается перед созданием буфера для получения текста из элемента управления.
ms.assetid: 42c89b7b-e48d-4517-9993-ce58ff9e4e40
keywords:
- Элементы управления Windows для EM_GETTEXTLENGTHEX сообщений
topic_type:
- apiref
api_name:
- EM_GETTEXTLENGTHEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2d91674e07ef60c2ce95535983a31cf380f9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891833"
---
# <a name="em_gettextlengthex-message"></a>\_Сообщение ЖЕТТЕКСТЛЕНГСЕКС EM

Вычисляет длину текста различными способами. Обычно он вызывается перед созданием буфера для получения текста из элемента управления.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указатель на структуру [**жеттекстленгсекс**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) , которая получает сведения о длине текста.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется; оно должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Сообщение возвращает количество элементов **TCHAR** в элементе управления "поле ввода" в зависимости от настроек флагов в структуре [**жеттекстленгсекс**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) . Если в элементе **flags** заданы несовместимые флаги, сообщение возвращает E \_ INVALIDARG.

## <a name="remarks"></a>Комментарии

Это сообщение позволяет быстро и просто определить количество символов в версии элемента управления Rich Edit в Юникоде. Однако для целевой кодовой страницы, отличной от Юникода, возможно преобразование в сочетание однобайтовых и двухбайтовых символов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жеттекстленгсекс**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)
</dt> </dl>

 

 





