---
title: Сообщение LVM_GETORIGIN (Коммктрл. h)
description: Возвращает начало текущего представления для элемента управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса «источник ListView».
ms.assetid: 913c8339-fbe4-43c8-a997-5a972920dc3b
keywords:
- Элементы управления Windows для LVM_GETORIGIN сообщений
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
ms.openlocfilehash: 8af42f3d616aa609d6b9e41d3991adb9d68eb24e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137110"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

