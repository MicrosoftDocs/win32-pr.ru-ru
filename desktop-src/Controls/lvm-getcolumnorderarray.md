---
title: Сообщение LVM_GETCOLUMNORDERARRAY (Коммктрл. h)
description: Возвращает текущий порядок столбцов слева направо в элементе управления "представление списка". Это сообщение можно отправить явным образом или использовать \_ макрос Жетколумнордераррай ListView.
ms.assetid: d4636aa8-c61e-4467-abc7-eea897bf370e
keywords:
- Элементы управления Windows для LVM_GETCOLUMNORDERARRAY сообщений
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aee387f65abd3f30826e361778d5acac02dfab7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071123"
---
# <a name="lvm_getcolumnorderarray-message"></a>\_Сообщение LVM жетколумнордераррай

Возвращает текущий порядок столбцов слева направо в элементе управления "представление списка". Это сообщение можно отправить явным образом или использовать макрос [**\_ жетколумнордераррай ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Число столбцов в элементе управления "список".

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на массив целых чисел, который получает значения индекса столбцов в элементе управления List-View. Массив должен быть достаточно большим, чтобы вместить элементы *wParam* .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха возвращает ненулевое значение, и буфер в *lParam* получает индекс столбца для каждого столбца в элементе управления в том порядке, в котором они отображаются слева направо. В противном случае возвращаемое значение равно нулю.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





