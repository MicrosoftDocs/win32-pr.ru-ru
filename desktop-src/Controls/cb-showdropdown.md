---
title: Сообщение CB_SHOWDROPDOWN (Winuser. h)
description: Приложение отправляет \_ сообщение ШОВДРОПДОВН CB для отображения или скрытия списка поля со списком, имеющего \_ раскрывающийся список CBS или \_ стиль DROPDOWNLIST.
ms.assetid: 32b995d7-eed6-4173-8525-0d356dea39b3
keywords:
- элементы управления Windows сообщений CB_SHOWDROPDOWN
topic_type:
- apiref
api_name:
- CB_SHOWDROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c820c65c053f7acbcffb379228ea5f7720476b6d2165ac4988ce8789e912cdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832242"
---
# <a name="cb_showdropdown-message"></a>\_Сообщение ШОВДРОПДОВН CB

Приложение отправляет сообщение **\_ шовдропдовн CB** для отображения или скрытия списка поля со списком, имеющего [**\_ раскрывающийся список CBS**](combo-box-styles.md) или стиль [**\_ DROPDOWNLIST**](combo-box-styles.md) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

**Логическое** значение, указывающее, должен ли раскрывающийся список отображаться или скрываться. Значение **true** показывает список; значение **false** скрывает его.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение всегда равно **true**.

## <a name="remarks"></a>Remarks

Это сообщение не влияет на поле со списком, созданное с [**помощью \_ простого стиля CBS**](combo-box-styles.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ЖЕТДРОППЕДСТАТЕ CB**](cb-getdroppedstate.md)
</dt> </dl>

 

 





