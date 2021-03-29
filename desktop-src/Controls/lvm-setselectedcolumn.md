---
title: Сообщение LVM_SETSELECTEDCOLUMN (Коммктрл. h)
description: Задает индекс выбранного столбца.
ms.assetid: 11b0838e-24a7-4c1c-b67d-0912b5a6442a
keywords:
- Элементы управления Windows для LVM_SETSELECTEDCOLUMN сообщений
topic_type:
- apiref
api_name:
- LVM_SETSELECTEDCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827c41fabaea722bb2372c6bd3f7c3a54bee92f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892838"
---
# <a name="lvm_setselectedcolumn-message"></a>\_Сообщение LVM сетселектедколумн

Задает индекс выбранного столбца.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Значение типа **int** , указывающее индекс столбца.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение не используется.

## <a name="remarks"></a>Комментарии

Индексы столбцов хранятся в массиве **типа int** . См. элемент **пуколумнс** элемента [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema).

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





