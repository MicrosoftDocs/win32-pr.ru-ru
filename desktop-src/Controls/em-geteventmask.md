---
title: Сообщение EM_GETEVENTMASK (RichEdit. h)
description: Извлекает маску события для элемента управления Rich Edit. Маска событий определяет, какие коды уведомлений отправляет элемент управления в родительское окно.
ms.assetid: cdf99f2a-e747-4b0e-9235-2719477c3ce2
keywords:
- элементы управления Windows сообщений EM_GETEVENTMASK
topic_type:
- apiref
api_name:
- EM_GETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4261869276015151e920e96e6c419675a1bce097384d6a918c2eac2b8005393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049234"
---
# <a name="em_geteventmask-message"></a>\_Сообщение GETEVENTMASK EM

Извлекает маску события для элемента управления Rich Edit. Маска событий определяет, какие коды уведомлений отправляет элемент управления в родительское окно.

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

Это сообщение возвращает маску события для элемента управления Rich Edit.

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

[**EM \_ SETEVENTMASK**](em-seteventmask.md)
</dt> <dt>

[**Флаги Маски событий элемента управления Rich Edit**](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





