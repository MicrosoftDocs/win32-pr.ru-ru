---
title: Сообщение LVM_GETHOVERTIME (Коммктрл. h)
description: Возвращает количество времени, в течение которого курсор мыши должен навести указатель на элемент, прежде чем он будет выбран. Это сообщение можно отправить явным образом или использовать \_ макрос Жесовертиме ListView.
ms.assetid: e7646024-f868-459f-88be-b232b6b4bb2a
keywords:
- элементы управления Windows сообщений LVM_GETHOVERTIME
topic_type:
- apiref
api_name:
- LVM_GETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 150a8eff54f8b3c27f0e7783ceda67af60c326e370d1a518d83e6bdd214fb529
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920104"
---
# <a name="lvm_gethovertime-message"></a>\_Сообщение LVM жесовертиме

Возвращает количество времени, в течение которого курсор мыши должен навести указатель на элемент, прежде чем он будет выбран. Это сообщение можно отправить явным образом или использовать макрос [**\_ жесовертиме ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает количество времени в миллисекундах, в течение которого курсор мыши должен навестися над элементом, прежде чем он будет выбран. Если возвращаемое значение равно (**DWORD**)-1, то по умолчанию используется время наведения.

## <a name="remarks"></a>Remarks

Время наведения на себя влияет только на элементы управления "представление списка", которые имеют расширенный стиль представления списка [**LVS \_ ex \_ траккселект**](extended-list-view-styles.md), [**LVS \_ ex \_ онекликкактивате**](extended-list-view-styles.md)или [**LVS \_ ex \_ твокликкактивате**](extended-list-view-styles.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





