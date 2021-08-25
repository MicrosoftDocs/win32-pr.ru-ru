---
title: Сообщение EM_SETCTFOPENSTATUS (RichEdit. h)
description: Открывает или закрывает клавиатуру платформы текстовых служб (TSF).
ms.assetid: 9bdabf5a-93db-4b0e-9528-807d262de866
keywords:
- элементы управления Windows сообщений EM_SETCTFOPENSTATUS
topic_type:
- apiref
api_name:
- EM_SETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ac27017abbadeb038f5b881aefe1aff394036931529c84c9c5a34a36e556c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048634"
---
# <a name="em_setctfopenstatus-message"></a>\_Сообщение СЕТКТФОПЕНСТАТУС EM

Открывает или закрывает клавиатуру платформы текстовых служб (TSF).

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Чтобы включить клавиатуру TSF, используйте **значение true**. Чтобы отключить клавиатуру TSF, используйте **значение false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха это сообщение возвращает **значение true**. В случае неудачи это сообщение возвращает **значение false**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 1 (SP1), \[ только классические приложения\]<br/>                                  |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**EM \_ жетктфопенстатус**](em-getctfopenstatus.md)
</dt> </dl>

 

 





