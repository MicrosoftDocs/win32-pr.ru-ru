---
title: Сообщение SB_GETICON (Коммктрл. h)
description: Возвращает значок для части в строке состояния.
ms.assetid: f99508e3-afa8-48fd-b87a-fce41c4410ff
keywords:
- элементы управления Windows сообщений SB_GETICON
topic_type:
- apiref
api_name:
- SB_GETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3df97598c1b002a794badb54f727632d58cc915f216947c019e452f5632a09fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168770"
---
# <a name="sb_geticon-message"></a>\_Сообщение о ПЕРЕзначке SB

Возвращает значок для части в строке состояния.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Отсчитываемый от нуля индекс части, содержащей извлекаемый значок. Если этот параметр имеет значение-1, строка состояния считается строкой состояния [простого режима](status-bars.md) .

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер для значка в случае успеха или **значение NULL** в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





