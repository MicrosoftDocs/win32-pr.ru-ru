---
title: Сообщение LVM_GETINSERTMARK (Коммктрл. h)
description: Возвращает позицию точки вставки.
ms.assetid: ad00df4c-4b4b-48f1-8821-7849a216df2e
keywords:
- Элементы управления Windows для LVM_GETINSERTMARK сообщений
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8cba96ae7d357e3e1f5a007fa41f6b7e9e3b64f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891705"
---
# <a name="lvm_getinsertmark-message"></a>\_Сообщение LVM жетинсертмарк

Возвращает позицию точки вставки.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Указатель на структуру <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">лвинсертмарк</a> , которая получает позицию точки вставки.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае. **Значение false** возвращается, если размер в элементе **кбсизе** структуры [**лвинсертмарк**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) не равен фактическому размеру структуры.

## <a name="remarks"></a>Комментарии

Точка вставки может отображаться только в том случае, если элемент управления "представление списка" находится в представлении значков, представлении с небольшим значком или мозаичном представлении, а не в режиме просмотра группы.

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





