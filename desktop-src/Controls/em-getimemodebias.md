---
title: Сообщение EM_GETIMEMODEBIAS (RichEdit. h)
description: Получает смещение режима редактора метода ввода (IME) для элемента управления Microsoft Rich Edit.
ms.assetid: e8ca899f-3423-4814-86e9-133dfd11f9a6
keywords:
- элементы управления Windows сообщений EM_GETIMEMODEBIAS
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
ms.openlocfilehash: 49ad5504ca2e5ac1a332657c4f539c9f983292617b6e74b949598488ceb38dfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019542"
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

## <a name="remarks"></a>Remarks

Чтобы получить значение смещения в режиме платформы текстовых служб, используйте [**EM \_ жетктфмодебиас**](em-getctfmodebias.md).

Перед вызовом этой функции приложение должно вызвать [**EM \_ исиме**](em-isime.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 1 (SP1), \[ только классические приложения\]<br/>                                  |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**EM \_ исиме**](em-isime.md)
</dt> <dt>

[**EM \_ жетктфмодебиас**](em-getctfmodebias.md)
</dt> </dl>

 

 





