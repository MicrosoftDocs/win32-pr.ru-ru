---
title: Сообщение PBM_GETBARCOLOR (Коммктрл. h)
description: Возвращает цвет индикатора выполнения.
ms.assetid: d046f7e4-e21e-4dd9-a7be-2bf820c3c492
keywords:
- элементы управления Windows сообщений PBM_GETBARCOLOR
topic_type:
- apiref
api_name:
- PBM_GETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb42d878840ad05f0854ec7ca9cb50dc1b3be2a55b3b65ddf652d961b6d818b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119312444"
---
# <a name="pbm_getbarcolor-message"></a>\_Сообщение ЖЕТБАРКОЛОР PBM

Возвращает цвет индикатора выполнения.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает цвет индикатора выполнения.

## <a name="remarks"></a>Remarks

Это цвет, заданный в сообщении [**\_ сетбарколор PBM**](pbm-setbarcolor.md) . Значение по умолчанию — CLR \_ по умолчанию, которое определено в коммктрл. h.

Эта функция влияет только на классический режим, а не на визуальный стиль.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





