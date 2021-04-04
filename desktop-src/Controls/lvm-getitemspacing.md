---
title: Сообщение LVM_GETITEMSPACING (Коммктрл. h)
description: Определяет интервал между элементами в элементе управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса ЖетитемспаЦинг ListView.
ms.assetid: 4e43fb43-468c-4b8a-9e3b-1694e90ffef8
keywords:
- Элементы управления Windows для LVM_GETITEMSPACING сообщений
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
ms.openlocfilehash: 5ea08a7fc1004ffb46d710da6d1c2a8b0fb18e57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989177"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

