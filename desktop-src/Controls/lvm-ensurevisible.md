---
title: Сообщение LVM_ENSUREVISIBLE (Коммктрл. h)
description: Гарантирует, что элемент списка является полностью или частично видимым, при необходимости прокручивать элемент управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Енсуревисибле ListView.
ms.assetid: 3564b6e6-b8b6-401b-85bc-8bd6261fc054
keywords:
- элементы управления Windows сообщений LVM_ENSUREVISIBLE
topic_type:
- apiref
api_name:
- LVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baeefaf90f0a4562fb187024b2c6f8676c68fb9d46377a4ced900bda6cfd3dfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920304"
---
# <a name="lvm_ensurevisible-message"></a>\_Сообщение LVM енсуревисибле

Гарантирует, что элемент списка является полностью или частично видимым, при необходимости прокручивать элемент управления "представление списка". Это сообщение можно отправить явно или с помощью макроса [**\_ енсуревисибле ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс элемента представления списка.

</dd> <dt>

*lParam* 
</dt> <dd>

Значение типа, указывающее, должен ли элемент быть полностью видимым. Если этот параметр имеет **значение true**, прокрутка не выполняется, если элемент является по крайней мере частично видимым.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Remarks

Сообщение завершается ошибкой, если стиль окна включает [**LVS " \_ Scroll**](list-view-window-styles.md)".

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





