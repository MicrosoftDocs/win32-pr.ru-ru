---
title: Сообщение LVM_GETORIGIN (Коммктрл. h)
description: Возвращает начало текущего представления для элемента управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса «источник ListView».
ms.assetid: 913c8339-fbe4-43c8-a997-5a972920dc3b
keywords:
- элементы управления Windows сообщений LVM_GETORIGIN
topic_type:
- apiref
api_name:
- LVM_GETORIGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a274e81c276d70eb1ab6c7f214b62ae5c346a59dda026bb13c5ab6b3ce80f68d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411361"
---
# <a name="lvm_getorigin-message"></a>Сообщение LVM о \_ происхождении

Возвращает начало текущего представления для элемента управления "представление списка". Это сообщение можно отправить явно или с помощью макроса [**« \_ источник ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin) ».

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**точек**](/previous-versions//dd162805(v=vs.85)) , которая получает источник представления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успешного выполнения или **false** , если текущее представление является списком или представлением отчетов.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

