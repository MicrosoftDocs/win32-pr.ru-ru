---
title: Сообщение LVM_SETHOTCURSOR (Коммктрл. h)
description: Задает значение ХКУРСОР, которое используется элементом управления "представление списка" при наведении указателя мыши на элемент, пока включено отслеживание.
ms.assetid: e3ff8608-9389-4167-839b-ecc2be01bb64
keywords:
- Элементы управления Windows для LVM_SETHOTCURSOR сообщений
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
ms.openlocfilehash: 0e743f74eda3b59f04f6f4793b47d76da3bab881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801109"
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

## <a name="remarks"></a>Комментарии

Элемент управления "представление списка" использует функцию отслеживания и выбора при наведении указателя, если установлен стиль [**LVS \_ ex \_ траккселект**](extended-list-view-styles.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

