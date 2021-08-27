---
title: Сообщение LVM_SETHOVERTIME (Коммктрл. h)
description: Задает период времени, в течение которого курсор мыши должен навести указатель на элемент, прежде чем он будет выбран. Это сообщение можно отправить явным образом или использовать \_ макрос Сесовертиме ListView.
ms.assetid: 454fbc38-f7fd-4dea-b223-56003b88528f
keywords:
- элементы управления Windows сообщений LVM_SETHOVERTIME
topic_type:
- apiref
api_name:
- LVM_SETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f93edf917dc50384f3a09f7eadf013561715735a995c63a695cb8f9ad91dbce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077234"
---
# <a name="lvm_sethovertime-message"></a>\_Сообщение LVM сесовертиме

Задает период времени, в течение которого курсор мыши должен навести указатель на элемент, прежде чем он будет выбран. Это сообщение можно отправить явным образом или использовать макрос [**\_ сесовертиме ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Новое время (в миллисекундах), в течение которого курсор мыши должен навести указатель на элемент, прежде чем он будет выбран. Если это значение равно (**DWORD**)-1, то во время наведения по умолчанию устанавливается значение времени наведения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает предыдущее время наведения.

## <a name="remarks"></a>Remarks

Время наведения на себя влияет только на элементы управления "представление списка", которые имеют расширенный стиль представления списка [**LVS \_ ex \_ траккселект**](extended-list-view-styles.md), [**LVS \_ ex \_ онекликкактивате**](extended-list-view-styles.md)или [**LVS \_ ex \_ твокликкактивате**](extended-list-view-styles.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





