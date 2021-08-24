---
title: Сообщение PBM_GETBKCOLOR (Коммктрл. h)
description: Возвращает цвет фона индикатора выполнения.
ms.assetid: 9526ed78-08d9-468f-831b-72bb7c8c92d1
keywords:
- элементы управления Windows сообщений PBM_GETBKCOLOR
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
ms.openlocfilehash: 1462d864df0440cd0567e6d6b1d04261818bb98ab4a6b5a803272e63abcb8d5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919524"
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

## <a name="remarks"></a>Remarks

Это цвет, заданный в сообщении [**\_ сетбкколор PBM**](pbm-setbkcolor.md) . Значение по умолчанию — CLR \_ по умолчанию, которое определено в коммктрл. h.

Эта функция влияет только на классический режим, а не на визуальный стиль.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





