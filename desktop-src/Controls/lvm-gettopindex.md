---
title: Сообщение LVM_GETTOPINDEX (Коммктрл. h)
description: Получает индекс самого верхнего видимого элемента в списке или представлении отчетов. Это сообщение можно отправить явно или с помощью \_ макроса Жеттопиндекс ListView.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_gettopindex.htm
keywords:
- элементы управления Windows сообщений LVM_GETTOPINDEX
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
ms.openlocfilehash: 6434aa2c7382a4a4d54fc3a76edd5eb4b70ccae858b8d9fcf41547590a8bc69c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920044"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





