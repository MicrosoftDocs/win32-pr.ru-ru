---
title: Сообщение EM_GETMARGINS (Winuser. h)
description: Возвращает ширину левого и правого полей для элемента управления "поле ввода".
ms.assetid: 2482354b-aae0-4abd-8287-65c423f30abb
keywords:
- Элементы управления Windows для EM_GETMARGINS сообщений
topic_type:
- apiref
api_name:
- EM_GETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 239ad7e7888f5bceef60bf2719c3b67798b56220
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801373"
---
# <a name="em_getmargins-message"></a>\_Сообщение EM прибыли

Возвращает ширину левого и правого полей для элемента управления "поле ввода".

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

Возвращает ширину левого поля в ЛОВОРД и ширину правого поля в HIWORD.

## <a name="remarks"></a>Комментарии

**Расширенное редактирование:** Сообщение **EM \_ прибыли** не поддерживается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EM \_ сетмаргинс**](em-setmargins.md)
</dt> </dl>

 

 





