---
title: Сообщение LVM_GETSELECTIONMARK (Коммктрл. h)
description: Извлекает метку выделения из элемента управления "представление списка". Это сообщение можно отправить явным образом или использовать \_ макрос Жетселектионмарк ListView.
ms.assetid: 21daf7d7-1217-4608-93f9-c390546f1591
keywords:
- Элементы управления Windows для LVM_GETSELECTIONMARK сообщений
topic_type:
- apiref
api_name:
- LVM_GETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 076aff15ff69c4b442c74022ed5a7c02b92a8c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654653"
---
# <a name="lvm_getselectionmark-message"></a>\_Сообщение LVM жетселектионмарк

Извлекает метку выделения из элемента управления "представление списка". Это сообщение можно отправить явным образом или использовать макрос [**\_ жетселектионмарк ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает знак выбора, начинающийся с нуля, или значение-1, если нет отметки выделения.

## <a name="remarks"></a>Комментарии

*Отметка выделения* — это индекс элемента, с которого начинается выбор нескольких элементов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**LVM \_ сетселектионмарк**](lvm-setselectionmark.md)
</dt> </dl>

 

 





