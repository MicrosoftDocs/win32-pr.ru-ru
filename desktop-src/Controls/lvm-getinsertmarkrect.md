---
title: Сообщение LVM_GETINSERTMARKRECT (Коммктрл. h)
description: Извлекает прямоугольник, ограничивающий точку вставки.
ms.assetid: 7b10229c-73ab-426c-8a8a-71258a33e248
keywords:
- элементы управления Windows сообщений LVM_GETINSERTMARKRECT
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARKRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5832ce185a579432b341482847400e96d60869a64d3ff0a2cd599e2eecf6b20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062604"
---
# <a name="lvm_getinsertmarkrect-message"></a>\_Сообщение LVM жетинсертмаркрект

Извлекает прямоугольник, ограничивающий точку вставки.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Не используется; должно быть равно нулю.</dd> <dt>

*lParam* 
</dt> <dd>Указатель на структуру <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> , содержащую координаты прямоугольника, ограничивающего точку вставки.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений.



| Код возврата                                                                      | Описание                          |
|----------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**0**</dt> </dl> | Точка вставки не найдена.<br/> |
| <dl> <dt>**1**</dt> </dl> | Найдена точка вставки.<br/>    |



 

## <a name="remarks"></a>Remarks

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

