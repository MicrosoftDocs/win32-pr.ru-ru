---
title: Сообщение RB_GETROWHEIGHT (Коммктрл. h)
description: Получает высоту указанной строки в элементе управления "Главная панель".
ms.assetid: 1ff6a32e-b344-4dbc-b4a4-fb13f11a9d8c
keywords:
- элементы управления Windows сообщений RB_GETROWHEIGHT
topic_type:
- apiref
api_name:
- RB_GETROWHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ac650fb50f1b6594964ec0bf10d23a8c8b6b75ff82e14af44bb63e2c9cf8af8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409418"
---
# <a name="rb_getrowheight-message"></a>\_Сообщение ЖЕТРОВХЕИГХТ RB

Получает высоту указанной строки в элементе управления "Главная панель".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Отсчитываемый от нуля индекс диапазона. Будет извлечена высота строки, содержащей указанный диапазон.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа **uint** , представляющее высоту строки в пикселях.

## <a name="remarks"></a>Remarks

Чтобы получить количество строк в элементе управления "Главная панель", используйте [**сообщение \_ RB**](rb-getrowcount.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





