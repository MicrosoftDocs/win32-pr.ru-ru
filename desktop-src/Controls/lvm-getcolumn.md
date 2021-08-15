---
title: Сообщение LVM_GETCOLUMN (Коммктрл. h)
description: Возвращает атрибуты столбца элемента управления "представление списка". Это сообщение можно отправить явным образом или с помощью \_ макроса DataColumn в ListView.
ms.assetid: 59b4bbfc-6c38-4faa-8f2e-3ea5d24e55a6
keywords:
- элементы управления Windows сообщений LVM_GETCOLUMN
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
ms.openlocfilehash: b65478d1d249740c630499fd4837e31d4eba7b992cf3ef3682c4e7b72d0706cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411740"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





