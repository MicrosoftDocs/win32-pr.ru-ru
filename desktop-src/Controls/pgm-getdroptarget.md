---
title: Сообщение PGM_GETDROPTARGET (Коммктрл. h)
description: Извлекает указатель интерфейса интерфейс IDropTarget элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать \_ макрос Жетдроптаржет пейджера.
ms.assetid: 6b548c30-2d32-4372-90e4-346a27dda218
keywords:
- Элементы управления Windows для PGM_GETDROPTARGET сообщений
topic_type:
- apiref
api_name:
- PGM_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b90f7f9667dd30a79b9345eec211a6ebfcd7a12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491790"
---
# <a name="pgm_getdroptarget-message"></a>\_Сообщение ЖЕТДРОПТАРЖЕТ PGM

Извлекает указатель интерфейса [**интерфейс IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать макрос [**\_ жетдроптаржет пейджера**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

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



 

