---
title: Сообщение LVM_INSERTCOLUMN (Коммктрл. h)
description: Вставляет новый столбец в элемент управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Инсертколумн ListView.
ms.assetid: 1326e38e-bb45-4d0d-b5bc-ec684b3b92ef
keywords:
- элементы управления Windows сообщений LVM_INSERTCOLUMN
topic_type:
- apiref
api_name:
- LVM_INSERTCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c2316ed2a74c82cd4530eff2d71d4771f4042b903c7ee17fc62886009ed5b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019242"
---
# <a name="lvm_insertcolumn-message"></a>\_Сообщение LVM инсертколумн

Вставляет новый столбец в элемент управления "представление списка". Это сообщение можно отправить явно или с помощью макроса [**\_ инсертколумн ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс нового столбца.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) , содержащую атрибуты нового столбца.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс нового столбца, если он выполнен успешно, или значение-1 в противном случае.

## <a name="remarks"></a>Remarks

Столбцы видимы только в представлении отчета (Details).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





