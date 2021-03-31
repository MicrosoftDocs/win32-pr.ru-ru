---
title: Сообщение TCM_SETTOOLTIPS (Коммктрл. h)
description: Назначает элемент управления ToolTip элементу управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл сеттултипс.
ms.assetid: c1b173b1-9da6-441a-a2b6-3875e2c343f8
keywords:
- Элементы управления Windows для TCM_SETTOOLTIPS сообщений
topic_type:
- apiref
api_name:
- TCM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e00166fb97c49c33b22811d28b79165bed4e9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801054"
---
# <a name="tcm_settooltips-message"></a>\_Сообщение СЕТТУЛТИПС TCM

Назначает элемент управления ToolTip элементу управления "Вкладка". Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ сеттултипс**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Обработчик для элемента управления ToolTip.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Элемент управления ToolTip, связанный с элементом управления "Вкладка", можно получить с помощью сообщения [**TCM- \_ ToolTips**](tcm-gettooltips.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





