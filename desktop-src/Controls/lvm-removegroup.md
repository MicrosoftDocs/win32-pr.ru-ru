---
title: Сообщение LVM_REMOVEGROUP (Коммктрл. h)
description: Удаляет группу из элемента управления "представление списка".
ms.assetid: c6f4f54c-4cf8-47d0-8e96-fa8a1df0501b
keywords:
- элементы управления Windows сообщений LVM_REMOVEGROUP
topic_type:
- apiref
api_name:
- LVM_REMOVEGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c644a0367747ad63eb15a2b83a8df3078c1c89ca1c51875b178aa22d054de2b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062324"
---
# <a name="lvm_removegroup-message"></a>\_Сообщение LVM ремовеграуп

Удаляет группу из элемента управления "представление списка".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Идентификатор, указывающий удаляемую группу.</dd> <dt>

*lParam* 
</dt> <dd>

Должен иметь **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс группы в случае успеха или значение-1 в противном случае.

## <a name="remarks"></a>Remarks

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





