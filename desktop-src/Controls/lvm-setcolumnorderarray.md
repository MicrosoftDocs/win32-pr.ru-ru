---
title: Сообщение LVM_SETCOLUMNORDERARRAY (Коммктрл. h)
description: Устанавливает порядок столбцов слева направо в элементе управления "представление списка". Это сообщение можно отправить явным образом или использовать \_ макрос Сетколумнордераррай ListView.
ms.assetid: 9b491832-42cc-4262-8f6c-23cbc2c889bf
keywords:
- элементы управления Windows сообщений LVM_SETCOLUMNORDERARRAY
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
ms.openlocfilehash: 9931a7d2c12da02f928c21727292d7d1ce4a430790660afb99ede4bf717c38c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077304"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





