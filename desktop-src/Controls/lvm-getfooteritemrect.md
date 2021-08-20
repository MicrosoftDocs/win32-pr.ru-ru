---
title: Сообщение LVM_GETFOOTERITEMRECT (Коммктрл. h)
description: Возвращает координаты нижнего колонтитула для указанного элемента в элементе управления "представление списка". Отправьте это сообщение явным образом или с помощью \_ макроса Жетфутеритемрект ListView.
ms.assetid: 4a6055d3-1cc1-4c3d-a5f6-006617ff3bce
keywords:
- элементы управления Windows сообщений LVM_GETFOOTERITEMRECT
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f5df635c18de3dec7cad128fe23ceeea2829b273984c561f5f289e2f0533b0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830675"
---
# <a name="lvm_getfooteritemrect-message"></a>\_Сообщение LVM жетфутеритемрект

Возвращает координаты нижнего колонтитула для указанного элемента в элементе управления "представление списка". Отправьте это сообщение явным образом или с помощью макроса [**\_ жетфутеритемрект ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* \[ окне\]
</dt> <dd>

Индекс элемента в элементе управления List-View.

</dd> <dt>

*lParam* \[ в, out\]
</dt> <dd>

Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) для получения координат. Вызывающее приложение отвечает за выделение этой структуры. Полученные координаты выражаются как клиентские координаты.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

