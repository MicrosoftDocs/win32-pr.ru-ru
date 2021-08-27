---
title: Сообщение CB_SETDROPPEDWIDTH (Winuser. h)
description: Приложение отправляет \_ сообщение СЕТДРОППЕДВИДС CB, чтобы задать минимальную допустимую ширину (в пикселях) поля со списком, используя \_ раскрывающийся список CBS или \_ стиль DROPDOWNLIST.
ms.assetid: 89f44733-aebe-44ea-b62d-8bd988f1bd6f
keywords:
- элементы управления Windows сообщений CB_SETDROPPEDWIDTH
topic_type:
- apiref
api_name:
- CB_SETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05d59aee89c4be18ba8e5013fa1a1e685a56b727d293c833c7f99140b683efeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089054"
---
# <a name="cb_setdroppedwidth-message"></a>\_Сообщение СЕТДРОППЕДВИДС CB

Приложение отправляет сообщение **\_ сетдроппедвидс CB** , чтобы задать минимальную допустимую ширину (в пикселях) поля со списком, используя [**\_ раскрывающийся список CBS**](combo-box-styles.md) или стиль [**\_ DROPDOWNLIST**](combo-box-styles.md) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Минимальная допустимая ширина окна списка в пикселях.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если сообщение прошло успешно, возвращаемое значение является новой шириной списка.

Если сообщение не выполняется, возвращается значение CB \_ Err.

## <a name="remarks"></a>Remarks

По умолчанию минимальная допустимая ширина раскрывающегося списка равна нулю. Ширина списка является либо минимальной допустимой шириной, либо шириной поля со списком, в зависимости от того, какое значение больше.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_ЖЕТДРОППЕДВИДС CB**](cb-getdroppedwidth.md)
</dt> </dl>

 

 





