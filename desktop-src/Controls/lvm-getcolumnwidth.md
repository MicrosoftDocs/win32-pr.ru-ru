---
title: Сообщение LVM_GETCOLUMNWIDTH (Коммктрл. h)
description: Возвращает ширину столбца в представлении отчета или списка. Это сообщение можно отправить явно или с помощью \_ макроса Жетколумнвидс ListView.
ms.assetid: 06e8ec36-3bc5-4516-ac29-17c36fb6d962
keywords:
- Элементы управления Windows для LVM_GETCOLUMNWIDTH сообщений
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
ms.openlocfilehash: 0577e7cb2a589c432d4b5ca62f640de61d67dc75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135134"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





