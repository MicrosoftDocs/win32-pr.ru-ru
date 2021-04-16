---
title: Сообщение LVM_GETCOLUMN (Коммктрл. h)
description: Возвращает атрибуты столбца элемента управления "представление списка". Это сообщение можно отправить явным образом или с помощью \_ макроса DataColumn в ListView.
ms.assetid: 59b4bbfc-6c38-4faa-8f2e-3ea5d24e55a6
keywords:
- Элементы управления Windows для LVM_GETCOLUMN сообщений
topic_type:
- apiref
api_name:
- LVM_GETCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eebf57138d27c31c5594f271e5d36a052b81673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489066"
---
# <a name="lvm_getcolumn-message"></a>\_Сообщение LVM DataColumn

Возвращает атрибуты столбца элемента управления "представление списка". Это сообщение можно отправить явным образом или с помощью макроса [**\_ DataColumn в ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс столбца.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) , указывающую сведения для извлечения и получения сведений о столбце. Элемент **Mask** указывает, какие атрибуты столбца следует извлечь. Если элемент **Mask** задает \_ текстовое значение лвкф, то элемент **псзтекст** должен содержать адрес буфера, который получает текст элемента, а элемент **кчтекстмакс** должен задавать размер буфера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





