---
title: Сообщение LVM_GETCOLUMNWIDTH (Коммктрл. h)
description: Возвращает ширину столбца в представлении отчета или списка. Это сообщение можно отправить явно или с помощью \_ макроса Жетколумнвидс ListView.
ms.assetid: 06e8ec36-3bc5-4516-ac29-17c36fb6d962
keywords:
- элементы управления Windows сообщений LVM_GETCOLUMNWIDTH
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 800ab7172ec489b84506cc55a342325527f38e447fc2bae635c2e5688a142b25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411510"
---
# <a name="lvm_getcolumnwidth-message"></a>\_Сообщение LVM жетколумнвидс

Возвращает ширину столбца в представлении отчета или списка. Это сообщение можно отправить явно или с помощью макроса [**\_ жетколумнвидс ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс столбца. Этот параметр не учитывается в представлении списка.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ширину столбца в случае успеха или ноль в противном случае. Если это сообщение отправлено в элемент управления "представление списка" с использованием стиля [**\_ отчета LVS**](list-view-window-styles.md) , а указанный столбец не существует, возвращаемое значение не определено.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





