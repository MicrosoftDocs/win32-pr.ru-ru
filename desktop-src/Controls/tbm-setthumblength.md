---
title: Сообщение TBM_SETTHUMBLENGTH (Коммктрл. h)
description: Задает длину ползунка в TrackBar. Это сообщение пропускается, если значение TrackBar не имеет \_ стиля TBS FIXEDLENGTH.
ms.assetid: 027fe341-a60a-4dbe-a48a-5ddaadef0b4a
keywords:
- Элементы управления Windows для TBM_SETTHUMBLENGTH сообщений
topic_type:
- apiref
api_name:
- TBM_SETTHUMBLENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d4ac33d2df43a267766e14ab95fb9729692bbee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535126"
---
# <a name="tbm_setthumblength-message"></a>\_Сообщение ТБМ сетсумбленгс

Задает длину ползунка в TrackBar. Это сообщение пропускается, если значение TrackBar не имеет стиля [**TBS \_ FIXEDLENGTH**](trackbar-control-styles.md) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Длина ползунка в пикселях.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ТБМ \_ жетсумбленгс**](tbm-getthumblength.md)
</dt> </dl>

 

 





