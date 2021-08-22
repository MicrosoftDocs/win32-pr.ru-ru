---
title: Сообщение EM_GETTEXTLENGTHEX (RichEdit. h)
description: Вычисляет длину текста различными способами. Обычно он вызывается перед созданием буфера для получения текста из элемента управления.
ms.assetid: 42c89b7b-e48d-4517-9993-ce58ff9e4e40
keywords:
- элементы управления Windows сообщений EM_GETTEXTLENGTHEX
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
ms.openlocfilehash: ba6cf0a094edc2288dbeae6f735e8c10fb72f943f99f9a41b15fc1ef3136168d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540943"
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

## <a name="remarks"></a>Remarks

Это сообщение позволяет быстро и просто определить количество символов в версии элемента управления Rich Edit в Юникоде. Однако для целевой кодовой страницы, отличной от Юникода, возможно преобразование в сочетание однобайтовых и двухбайтовых символов.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**жеттекстленгсекс**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)
</dt> </dl>

 

 





