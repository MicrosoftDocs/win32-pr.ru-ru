---
title: Сообщение EM_SETEVENTMASK (RichEdit. h)
description: Задает маску события для элемента управления расширенного редактирования. Маска событий определяет, какие коды уведомлений отправляет элемент управления в родительское окно.
ms.assetid: 139f6e44-fc54-40f2-a3f6-2b7efc819cae
keywords:
- элементы управления Windows сообщений EM_SETEVENTMASK
topic_type:
- apiref
api_name:
- EM_SETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 244274d969473531bae7c1d124af24a88d6b98d9db8bdbe073d054a3a9e36ac1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048504"
---
# <a name="em_seteventmask-message"></a>\_Сообщение SETEVENTMASK EM

Задает маску события для элемента управления расширенного редактирования. Маска событий определяет, какие коды уведомлений отправляет элемент управления в родительское окно.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется; оно должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Новая маска событий для элемента управления Rich Edit. Список масок событий см. в разделе [**Флаги Маски событий элемента управления Rich Edit**](rich-edit-control-event-mask-flags.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение возвращает предыдущую маску события.

## <a name="remarks"></a>Remarks

Маска события по умолчанию (перед любым набором) — ЕНМ \_ None.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**EM \_ GETEVENTMASK**](em-geteventmask.md)
</dt> <dt>

[**Флаги Маски событий элемента управления Rich Edit**](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





