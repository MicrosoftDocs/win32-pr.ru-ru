---
title: Сообщение EM_GETCTFMODEBIAS (RichEdit. h)
description: Возвращает значения смещения режима платформы текстовых служб для элемента управления Microsoft Rich Edit.
ms.assetid: 2421d37d-169d-480f-a5f7-4c6033ca6c1a
keywords:
- Элементы управления Windows для EM_GETCTFMODEBIAS сообщений
topic_type:
- apiref
api_name:
- EM_GETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d5eabbddca1c13fefae99c29d8c550fbd274e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136139"
---
# <a name="em_getctfmodebias-message"></a>\_Сообщение ЖЕТКТФМОДЕБИАС EM

Возвращает значения смещения режима платформы текстовых служб для элемента управления Microsoft Rich Edit.

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

Текущее значение смещения в режиме платформы текстовых служб.

## <a name="remarks"></a>Комментарии

Чтобы получить смещение режима IME, вызовите [**EM \_ жетимемодебиас**](em-getimemodebias.md).

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

[**EM \_ сетктфмодебиас**](em-setctfmodebias.md)
</dt> <dt>

[**EM \_ жетимемодебиас**](em-getimemodebias.md)
</dt> </dl>

 

 





