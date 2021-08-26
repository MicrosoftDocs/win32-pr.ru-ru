---
title: Сообщение TCM_SETTOOLTIPS (Коммктрл. h)
description: Назначает элемент управления ToolTip элементу управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл сеттултипс.
ms.assetid: c1b173b1-9da6-441a-a2b6-3875e2c343f8
keywords:
- элементы управления Windows сообщений TCM_SETTOOLTIPS
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
ms.openlocfilehash: c8bfec3b7272ceae3dcbf1781e3bb17a988f2252b3c0a74822677bff6ea39209
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104694"
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

## <a name="remarks"></a>Remarks

Элемент управления ToolTip, связанный с элементом управления "Вкладка", можно получить с помощью сообщения [**TCM- \_ ToolTips**](tcm-gettooltips.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





