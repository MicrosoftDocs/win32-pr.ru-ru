---
title: Сообщение LVM_SETSELECTEDCOLUMN (Коммктрл. h)
description: Задает индекс выбранного столбца.
ms.assetid: 11b0838e-24a7-4c1c-b67d-0912b5a6442a
keywords:
- элементы управления Windows сообщений LVM_SETSELECTEDCOLUMN
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
ms.openlocfilehash: 6f6564e1fda50d11b3d4c520f85184439b0465f1cf5767e7926e6e1c9476f786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019175"
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

## <a name="remarks"></a>Remarks

Индексы столбцов хранятся в массиве **типа int** . См. элемент **пуколумнс** элемента [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema).

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





