---
title: Сообщение EM_GETEVENTMASK (RichEdit. h)
description: Извлекает маску события для элемента управления Rich Edit. Маска событий определяет, какие коды уведомлений отправляет элемент управления в родительское окно.
ms.assetid: cdf99f2a-e747-4b0e-9235-2719477c3ce2
keywords:
- Элементы управления Windows для EM_GETEVENTMASK сообщений
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
ms.openlocfilehash: 4f4d231bbb9d5592ff2f90da6a5096783b38c292
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989016"
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

[**EM \_ SETEVENTMASK**](em-seteventmask.md)
</dt> <dt>

[**Флаги Маски событий элемента управления Rich Edit**](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





