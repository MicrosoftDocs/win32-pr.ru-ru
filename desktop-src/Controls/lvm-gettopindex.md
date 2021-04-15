---
title: Сообщение LVM_GETTOPINDEX (Коммктрл. h)
description: Получает индекс самого верхнего видимого элемента в списке или представлении отчетов. Это сообщение можно отправить явно или с помощью \_ макроса Жеттопиндекс ListView.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_gettopindex.htm
keywords:
- Элементы управления Windows для LVM_GETTOPINDEX сообщений
topic_type:
- apiref
api_name:
- LVM_GETTOPINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb1cb080588d1825fcbd9e6c5e7b1b573fd7ad2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654649"
---
# <a name="lvm_gettopindex-message"></a>\_Сообщение LVM жеттопиндекс

Получает индекс самого верхнего видимого элемента в списке или представлении отчетов. Это сообщение можно отправить явно или с помощью макроса [**\_ жеттопиндекс ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс элемента, если он был успешным. Возвращает нуль, если элемент управления "представление списка" находится в виде значка или маленького значка или если элемент управления "представление списка" находится в представлении Details с включенными группами.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





