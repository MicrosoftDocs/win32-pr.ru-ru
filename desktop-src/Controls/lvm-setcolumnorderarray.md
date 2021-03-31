---
title: Сообщение LVM_SETCOLUMNORDERARRAY (Коммктрл. h)
description: Устанавливает порядок столбцов слева направо в элементе управления "представление списка". Это сообщение можно отправить явным образом или использовать \_ макрос Сетколумнордераррай ListView.
ms.assetid: 9b491832-42cc-4262-8f6c-23cbc2c889bf
keywords:
- Элементы управления Windows для LVM_SETCOLUMNORDERARRAY сообщений
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94fdeb27074a3f6762e7fb3788fd7ccc0a2dcc5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071115"
---
# <a name="lvm_setcolumnorderarray-message"></a>\_Сообщение LVM сетколумнордераррай

Устанавливает порядок столбцов слева направо в элементе управления "представление списка". Это сообщение можно отправить явным образом или использовать макрос [**\_ сетколумнордераррай ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Размер (в элементах) буфера в параметре *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на массив, указывающий порядок отображения столбцов слева направо. Например, если содержимое массива равно {2,0,1} , то элемент управления отображает столбец 2, столбец 0 и столбец 1 в этом порядке.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





