---
title: Сообщение CB_SHOWDROPDOWN (Winuser. h)
description: Приложение отправляет \_ сообщение ШОВДРОПДОВН CB для отображения или скрытия списка поля со списком, имеющего \_ раскрывающийся список CBS или \_ стиль DROPDOWNLIST.
ms.assetid: 32b995d7-eed6-4173-8525-0d356dea39b3
keywords:
- Элементы управления Windows для CB_SHOWDROPDOWN сообщений
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
ms.openlocfilehash: fb66e9a0ecf3b6680fce9aca7f680fd6e6fd13e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137182"
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

## <a name="remarks"></a>Комментарии

Это сообщение не влияет на поле со списком, созданное с [**помощью \_ простого стиля CBS**](combo-box-styles.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ЖЕТДРОППЕДСТАТЕ CB**](cb-getdroppedstate.md)
</dt> </dl>

 

 





