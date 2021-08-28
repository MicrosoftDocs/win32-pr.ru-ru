---
title: Сообщение LVM_GETITEMSPACING (Коммктрл. h)
description: Определяет интервал между элементами в элементе управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса ЖетитемспаЦинг ListView.
ms.assetid: 4e43fb43-468c-4b8a-9e3b-1694e90ffef8
keywords:
- элементы управления Windows сообщений LVM_GETITEMSPACING
topic_type:
- apiref
api_name:
- LVM_GETITEMSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 687a1aa75d71b96cebe855bb97ea57f0a9c628ed49b1ef7a51a7557b23b5ce41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088894"
---
# <a name="lvm_getitemspacing-message"></a>\_Сообщение LVM жетитемспаЦинг

Определяет интервал между элементами в элементе управления "представление списка". Это сообщение можно отправить явно или с помощью макроса [**\_ жетитемспаЦинг ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Представление, для которого нужно получить сведения о промежутке между элементами. Этот параметр имеет **значение true** для представления небольшого значка или **значение false** для представления значков.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает величину интервала между элементами. Расстояние по горизонтали содержится в [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) , а вертикальное расстояние содержится в [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

