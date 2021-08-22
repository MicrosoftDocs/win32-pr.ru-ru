---
title: Сообщение LVM_GETHOTCURSOR (Коммктрл. h)
description: Получает значение ХКУРСОР, используемое, когда указатель находится над элементом, а активирована Оперативное отслеживание. Это сообщение можно отправить явным образом или использовать \_ макрос Жесоткурсор ListView.
ms.assetid: 064d04b2-d74e-4a80-aec6-97a3c53fc4fb
keywords:
- элементы управления Windows сообщений LVM_GETHOTCURSOR
topic_type:
- apiref
api_name:
- LVM_GETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e5703d252d239124b78656c4a5991efdecb2107552fb6e2ab0f87701af4e18d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540804"
---
# <a name="lvm_gethotcursor-message"></a>\_Сообщение LVM жесоткурсор

Получает значение ХКУРСОР, используемое, когда указатель находится над элементом, а активирована Оперативное отслеживание. Это сообщение можно отправить явным образом или использовать макрос [**\_ жесоткурсор ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение ХКУРСОР, которое является маркером для курсора, который используется элементом управления "список" при включенном режиме отслеживания.

## <a name="remarks"></a>Remarks

Элемент управления "представление списка" использует функцию отслеживания и выбора при наведении указателя, если установлен стиль [**LVS \_ ex \_ траккселект**](extended-list-view-styles.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





