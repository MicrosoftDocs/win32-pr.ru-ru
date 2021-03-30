---
title: Сообщение LVM_SETSELECTIONMARK (Коммктрл. h)
description: Задает метку выделения в элементе управления "представление списка". Это сообщение можно отправить явным образом или использовать \_ макрос Сетселектионмарк ListView.
ms.assetid: 3218f1b3-b934-4083-aaaa-e10ef1dbb6bd
keywords:
- Элементы управления Windows для LVM_SETSELECTIONMARK сообщений
topic_type:
- apiref
api_name:
- LVM_SETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3efc01068f22585061cae5a6f2c5c0c841810f52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801102"
---
# <a name="lvm_setselectionmark-message"></a>\_Сообщение LVM сетселектионмарк

Задает метку выделения в элементе управления "представление списка". Это сообщение можно отправить явным образом или использовать макрос [**\_ сетселектионмарк ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Отсчитываемый от нуля индекс новой метки выделения. Если задано значение-1, отметка выделения удаляется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает предыдущую отметку выделения или-1, если Предыдущая метка выбора отсутствует.

## <a name="remarks"></a>Комментарии

*Отметка выделения* — это индекс элемента, с которого начинается выбор нескольких элементов. Это сообщение не влияет на состояние выбора элемента.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**LVM \_ жетселектионмарк**](lvm-getselectionmark.md)
</dt> </dl>

 

 





