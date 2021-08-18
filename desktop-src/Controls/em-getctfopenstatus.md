---
title: Сообщение EM_GETCTFOPENSTATUS (RichEdit. h)
description: Определяет, открыта или закрыта клавиатура платформы текстовых служб (TSF).
ms.assetid: a50fedf4-b4e5-4b99-be46-1bbbf08e85a8
keywords:
- элементы управления Windows сообщений EM_GETCTFOPENSTATUS
topic_type:
- apiref
api_name:
- EM_GETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef55fe0944ad3632f8bfec11894c5613efde02dc1ec16f8c0d31105f6b19ea8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019742"
---
# <a name="em_getctfopenstatus-message"></a>\_Сообщение ЖЕТКТФОПЕНСТАТУС EM

Определяет, открыта или закрыта клавиатура платформы текстовых служб (TSF).

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

Если клавиатура TSF открыта, возвращается значение **true**. В противном случае — **false**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 1 (SP1), \[ только классические приложения\]<br/>                                  |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**EM \_ сетктфопенстатус**](em-setctfopenstatus.md)
</dt> </dl>

 

 





