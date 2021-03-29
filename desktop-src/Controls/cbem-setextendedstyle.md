---
title: Сообщение CBEM_SETEXTENDEDSTYLE (Коммктрл. h)
description: Задает расширенные стили в элементе управления ComboBoxEx.
ms.assetid: 00848bd0-5a2f-4bfb-ae1f-ee3aa88ac57a
keywords:
- Элементы управления Windows для CBEM_SETEXTENDEDSTYLE сообщений
topic_type:
- apiref
api_name:
- CBEM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a60518d2f6130c2c89e379125308fc2e647c6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654693"
---
# <a name="cbem_setextendedstyle-message"></a>\_Сообщение кбем сетекстендедстиле

Задает расширенные стили в элементе управления ComboBoxEx.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Значение **типа DWORD** , указывающее, какие стили в *lParam* должны быть затронуты. Будут изменены только расширенные стили в параметре *wParam* . Если этот параметр равен нулю, будут затронуты все стили в *lParam* .

</dd> <dt>

*lParam* 
</dt> <dd>

Значение **типа DWORD** , содержащее [Расширенные стили элемента управления ComboBoxEx](comboboxex-control-extended-styles.md) , заданные для элемента управления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **типа DWORD** , содержащее расширенные стили, которые использовались ранее для элемента управления.

## <a name="remarks"></a>Комментарии

*wParam* позволяет изменять один или несколько расширенных стилей без предварительного получения существующих стилей. Например, если передать [**кбес \_ ex \_ ноедитимаже**](comboboxex-control-extended-styles.md) для *wParam* и 0 для *lParam*, то стиль **кбес \_ ex \_ ноедитимаже** будет сброшен, но все остальные стили останутся прежними.

Если вы попытаетесь задать расширенный стиль для элемента управления ComboBoxEx, созданного с помощью [**\_ простого стиля CBS**](combo-box-styles.md) , он может не перерисовываться должным образом.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





