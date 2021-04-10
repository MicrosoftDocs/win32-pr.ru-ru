---
title: Сообщение LVM_SETINSERTMARK (Коммктрл. h)
description: Задает точку вставки в заданную позицию.
ms.assetid: 32cf5a11-918a-4dc4-bf10-88b3c26f26cc
keywords:
- Элементы управления Windows для LVM_SETINSERTMARK сообщений
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dab80b1b73b620ce94b75aecab90f6bdd69bf228
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135118"
---
# <a name="lvm_setinsertmark-message"></a>\_Сообщение LVM сетинсертмарк

Задает точку вставки в заданную позицию.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Указатель на структуру <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">лвинсертмарк</a> , указывающую место установки точки вставки.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае. **Значение false** возвращается, если размер элемента **кбсизе** структуры [**лвинсертмарк**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) не равен фактическому размеру структуры или если точка вставки не применяется в текущем представлении.

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



 

 





