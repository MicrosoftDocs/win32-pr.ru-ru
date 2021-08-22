---
title: Сообщение CBEM_SETEXTENDEDSTYLE (Коммктрл. h)
description: Задает расширенные стили в элементе управления ComboBoxEx.
ms.assetid: 00848bd0-5a2f-4bfb-ae1f-ee3aa88ac57a
keywords:
- элементы управления Windows сообщений CBEM_SETEXTENDEDSTYLE
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
ms.openlocfilehash: efd1083e838d85f9cb659acb9a28b74a1d8605934be4c53fd72993e7470fad2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527974"
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

## <a name="remarks"></a>Remarks

*wParam* позволяет изменять один или несколько расширенных стилей без предварительного получения существующих стилей. Например, если передать [**кбес \_ ex \_ ноедитимаже**](comboboxex-control-extended-styles.md) для *wParam* и 0 для *lParam*, то стиль **кбес \_ ex \_ ноедитимаже** будет сброшен, но все остальные стили останутся прежними.

Если вы попытаетесь задать расширенный стиль для элемента управления ComboBoxEx, созданного с помощью [**\_ простого стиля CBS**](combo-box-styles.md) , он может не перерисовываться должным образом.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





