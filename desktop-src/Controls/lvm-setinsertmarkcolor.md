---
title: Сообщение LVM_SETINSERTMARKCOLOR (Коммктрл. h)
description: Задает цвет точки вставки.
ms.assetid: dce2c266-672b-4682-ba23-51d9a8e1102b
keywords:
- Элементы управления Windows для LVM_SETINSERTMARKCOLOR сообщений
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260d21d083e2c70d8e82a27628e42596bd1b37eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988196"
---
# <a name="lvm_setinsertmarkcolor-message"></a>\_Сообщение LVM сетинсертмаркколор

Задает цвет точки вставки.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Структура **COLORREF** , указывающая цвет для установки точки вставки.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает структуру **COLORREF** , установленную на предыдущий цвет.

## <a name="remarks"></a>Комментарии

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





