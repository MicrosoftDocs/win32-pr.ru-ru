---
title: Сообщение EM_GETIMEMODEBIAS (RichEdit. h)
description: Получает смещение режима редактора метода ввода (IME) для элемента управления Microsoft Rich Edit.
ms.assetid: e8ca899f-3423-4814-86e9-133dfd11f9a6
keywords:
- Элементы управления Windows для EM_GETIMEMODEBIAS сообщений
topic_type:
- apiref
api_name:
- EM_GETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea13e151ae9d487340ee440e3b123ae70b437a02
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071820"
---
# <a name="em_getimemodebias-message"></a>\_Сообщение ЖЕТИМЕМОДЕБИАС EM

Получает смещение режима редактора метода ввода (IME) для элемента управления Microsoft Rich Edit.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение возвращает текущий параметр смещения режима IME.

## <a name="remarks"></a>Комментарии

Чтобы получить значение смещения в режиме платформы текстовых служб, используйте [**EM \_ жетктфмодебиас**](em-getctfmodebias.md).

Перед вызовом этой функции приложение должно вызвать [**EM \_ исиме**](em-isime.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 1 \[\]<br/>                                  |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**EM \_ исиме**](em-isime.md)
</dt> <dt>

[**EM \_ жетктфмодебиас**](em-getctfmodebias.md)
</dt> </dl>

 

 





