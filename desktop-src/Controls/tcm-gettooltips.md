---
title: Сообщение TCM_GETTOOLTIPS (Коммктрл. h)
description: Получает маркер для элемента управления ToolTip, связанного с элементом управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл.
ms.assetid: d7dcca4f-8629-4eeb-844f-b3171438f528
keywords:
- элементы управления Windows сообщений TCM_GETTOOLTIPS
topic_type:
- apiref
api_name:
- TCM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb68710c13c8b6b236782b133caa5b6f3609fef931e3b1e395b9944e9ab9a651
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166937"
---
# <a name="tcm_gettooltips-message"></a>\_Сообщение о подсказках TCM

Получает маркер для элемента управления ToolTip, связанного с элементом управления "Вкладка". Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер для элемента управления ToolTip, если он успешно, или **значение NULL** в противном случае.

## <a name="remarks"></a>Remarks

Элемент управления "Вкладка" создает элемент управления ToolTip, если он имеет стиль [**\_ подсказок TCS**](tab-control-styles.md) . Элемент управления ToolTip можно также назначить элементу управления "Вкладка" с помощью сообщения [**TCM \_ сеттултипс**](tcm-settooltips.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





