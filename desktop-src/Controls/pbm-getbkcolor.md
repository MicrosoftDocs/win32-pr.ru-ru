---
title: Сообщение PBM_GETBKCOLOR (Коммктрл. h)
description: Возвращает цвет фона индикатора выполнения.
ms.assetid: 9526ed78-08d9-468f-831b-72bb7c8c92d1
keywords:
- Элементы управления Windows для PBM_GETBKCOLOR сообщений
topic_type:
- apiref
api_name:
- PBM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2240025629bbcc242ea7ed47be2e3db42ae73b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892285"
---
# <a name="pbm_getbkcolor-message"></a>\_Сообщение ЖЕТБККОЛОР PBM

Возвращает цвет фона индикатора выполнения.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает цвет фона индикатора выполнения.

## <a name="remarks"></a>Комментарии

Это цвет, заданный в сообщении [**\_ сетбкколор PBM**](pbm-setbkcolor.md) . Значение по умолчанию — CLR \_ по умолчанию, которое определено в коммктрл. h.

Эта функция влияет только на классический режим, а не на визуальный стиль.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





