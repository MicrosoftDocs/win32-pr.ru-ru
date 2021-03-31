---
title: Сообщение LVM_SETTILEVIEWINFO (Коммктрл. h)
description: Задает сведения, используемые элементом управления "представление списка" в мозаичном представлении.
ms.assetid: 1c4f2aff-1ce1-484a-9360-3efbe870b39b
keywords:
- Элементы управления Windows для LVM_SETTILEVIEWINFO сообщений
topic_type:
- apiref
api_name:
- LVM_SETTILEVIEWINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25d6c728d92bb931837eca440af679b5bcb98d1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135586"
---
# <a name="lvm_settileviewinfo-message"></a>\_Сообщение LVM сеттилевиевинфо

Задает сведения, используемые элементом управления "представление списка" в мозаичном представлении.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Указатель на структуру <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**лвтилевиевинфо**</a> , содержащую сведения, которые необходимо задать.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Комментарии

Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





