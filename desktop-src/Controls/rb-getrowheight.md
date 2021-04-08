---
title: Сообщение RB_GETROWHEIGHT (Коммктрл. h)
description: Получает высоту указанной строки в элементе управления "Главная панель".
ms.assetid: 1ff6a32e-b344-4dbc-b4a4-fb13f11a9d8c
keywords:
- Элементы управления Windows для RB_GETROWHEIGHT сообщений
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
ms.openlocfilehash: 27ce137eef6168d95abfe493a6f22ab66d58460b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892237"
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

## <a name="remarks"></a>Комментарии

Чтобы получить количество строк в элементе управления "Главная панель", используйте [**сообщение \_ RB**](rb-getrowcount.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





