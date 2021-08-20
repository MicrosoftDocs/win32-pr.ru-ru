---
title: Сообщение TBM_CLEARTICS (Коммктрл. h)
description: Удаляет текущие деления из TrackBar. Это сообщение не удаляет первый и последний деления, которые создаются автоматически с помощью TrackBar.
ms.assetid: 2830497c-2cf0-4068-810c-c05d4e0abb8b
keywords:
- элементы управления Windows сообщений TBM_CLEARTICS
topic_type:
- apiref
api_name:
- TBM_CLEARTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9390fc45c5b96a7b85d3b1b366e34d24c3b4bf0bc60ec066ead28357bcec1439
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046774"
---
# <a name="tbm_cleartics-message"></a>\_Сообщение ТБМ клеартикс

Удаляет текущие деления из TrackBar. Это сообщение не удаляет первый и последний деления, которые создаются автоматически с помощью TrackBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Флаг перерисовки. Если этот параметр имеет **значение true**, линейка перерисовывается после очистки делений. Если этот параметр имеет **значение false**, сообщение очищает деления, но не перерисовывает TrackBar.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





