---
title: Сообщение RB_GETDROPTARGET (Коммктрл. h)
description: Извлекает указатель интерфейса интерфейс IDropTarget элемента управления "Главная панель".
ms.assetid: f429c5d1-406b-47f0-a654-47cabccc1d0e
keywords:
- Элементы управления Windows для RB_GETDROPTARGET сообщений
topic_type:
- apiref
api_name:
- RB_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55b7960cc13230a2715348bc55e5e65de6f72e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491763"
---
# <a name="rb_getdroptarget-message"></a>\_Сообщение ЖЕТДРОПТАРЖЕТ RB

Извлекает указатель интерфейса [**интерфейс IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) элемента управления "Главная панель".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на указатель [**интерфейс IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) , получающий указатель интерфейса. Вызов метода [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) с этим указателем, когда он больше не нужен, является обязанностью вызывающего объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение для этого сообщения не используется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

