---
title: Сообщение LVM_SETHOTCURSOR (Коммктрл. h)
description: Задает значение ХКУРСОР, которое используется элементом управления "представление списка" при наведении указателя мыши на элемент, пока включено отслеживание.
ms.assetid: e3ff8608-9389-4167-839b-ecc2be01bb64
keywords:
- элементы управления Windows сообщений LVM_SETHOTCURSOR
topic_type:
- apiref
api_name:
- LVM_SETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3407c5d8b53483d3a639fc40959768b3fa8eea0e7b439ab8871d36346b7079d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077254"
---
# <a name="lvm_sethotcursor-message"></a>\_Сообщение LVM сесоткурсор

Задает значение ХКУРСОР, которое используется элементом управления "представление списка" при наведении указателя мыши на элемент, пока включено отслеживание. Это сообщение можно отправить явным образом или использовать макрос [**\_ сесоткурсор ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) . Чтобы проверить, включено ли оперативное отслеживание, вызовите [**системпараметерсинфо**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на заданный курсор.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение ХКУРСОР, которое является предыдущим активным курсором.

## <a name="remarks"></a>Remarks

Элемент управления "представление списка" использует функцию отслеживания и выбора при наведении указателя, если установлен стиль [**LVS \_ ex \_ траккселект**](extended-list-view-styles.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

