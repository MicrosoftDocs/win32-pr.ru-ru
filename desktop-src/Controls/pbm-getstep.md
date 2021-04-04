---
title: Сообщение PBM_GETSTEP (Коммктрл. h)
description: Извлекает шаг шага из индикатора выполнения. Шаг приращения — это величина, на которую индикатор выполнения увеличивает текущее местоположение при получении \_ сообщения СТЕПИТ PBM. По умолчанию шаг с шагом равен 10.
ms.assetid: 0cf3052a-cf86-4c0e-ad59-ddab7c6e3602
keywords:
- Элементы управления Windows для PBM_GETSTEP сообщений
topic_type:
- apiref
api_name:
- PBM_GETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dcc4adb18d2b60d2936c2cdc7ab79d00389b3ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988999"
---
# <a name="pbm_getstep-message"></a>\_ПОшаговое сообщение PBM

Извлекает шаг шага из индикатора выполнения. Шаг приращения — это величина, на которую индикатор выполнения увеличивает текущее местоположение при получении сообщения [**\_ степит PBM**](pbm-stepit.md) . По умолчанию шаг с шагом равен 10.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает текущий шаг шага.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





