---
title: Сообщение EM_GETTEXTEX (RichEdit. h)
description: Возвращает текст из элемента управления Rich Edit.
ms.assetid: 46431563-fde1-4407-ab7a-b2248c0e12b8
keywords:
- Элементы управления Windows для EM_GETTEXTEX сообщений
topic_type:
- apiref
api_name:
- EM_GETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 357cfe37d3432b396183b500c945ad89397c0294
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490371"
---
# <a name="em_gettextex-message"></a>\_Сообщение ЖЕТТЕКСТЕКС EM

Возвращает текст из элемента управления Rich Edit.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указатель на структуру [**жеттекстекс**](/windows/desktop/api/Richedit/ns-richedit-gettextex) , которая указывает, как перевести текст перед помещением в выходной буфер.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на буфер для получения текста. Размер этого буфера в байтах указывается членом **CB** структуры [**жеттекстекс**](/windows/desktop/api/Richedit/ns-richedit-gettextex) . Чтобы получить требуемый размер буфера, используйте сообщение [**EM \_ жеттекстленгсекс**](em-gettextlengthex.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение — это число файлов **TCHAR**, скопированных в выходной буфер, включая знак завершения null.

## <a name="remarks"></a>Комментарии

Если размер выходного буфера меньше размера текста в элементе управления, элемент управления "поле ввода" скопирует текст с начала и поместит его в буфер до заполнения буфера. Завершающий нуль-символ все равно будет помещен в конец буфера.

Если запрашивается текст ANSI, **EM \_ жеттекстекс** использует функцию [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) для преобразования символов Юникода в ANSI. Он позволяет переходить из Юникода в ANSI с помощью определенной кодовой страницы. Структура [**жеттекстекс**](/windows/desktop/api/Richedit/ns-richedit-gettextex) содержит элементы (**лпдефаултчар** и **лпуседдефчар**), которые используются при переводе из Юникода в ANSI.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**EM \_ сеттекстекс**](em-settextex.md)
</dt> <dt>

[**жеттекстекс**](/windows/desktop/api/Richedit/ns-richedit-gettextex)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
</dt> <dt>

[**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

