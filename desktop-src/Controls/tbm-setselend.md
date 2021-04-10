---
title: Сообщение TBM_SETSELEND (Коммктрл. h)
description: Задает конечную логическую точку текущего выделенного диапазона в TrackBar. Это сообщение пропускается, если значение TrackBar не имеет \_ стиля TBS енаблеселранже.
ms.assetid: 1feec14c-1607-49d5-a147-af2443f82dc1
keywords:
- Элементы управления Windows для TBM_SETSELEND сообщений
topic_type:
- apiref
api_name:
- TBM_SETSELEND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 146446df4daf8e8ac7c0f3499149ba0f46940880
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135095"
---
# <a name="tbm_setselend-message"></a>\_Сообщение ТБМ сетселенд

Задает конечную логическую точку текущего выделенного диапазона в TrackBar. Это сообщение пропускается, если значение TrackBar не имеет стиля [**TBS \_ енаблеселранже**](trackbar-control-styles.md) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Флаг перерисовки. Если этот параметр имеет **значение true**, сообщение перерисовывается после установки диапазона выбора. Если этот параметр имеет **значение false**, то сообщение задает диапазон выбора, но не перерисовывает линейку.

</dd> <dt>

*lParam* 
</dt> <dd>

Конечная логическая позиция диапазона выбора.

</dd> </dl>

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

**Ссылки**
</dt> <dt>

[**ТБМ \_ жетселенд**](tbm-getselend.md)
</dt> <dt>

[**ТБМ \_ жетселстарт**](tbm-getselstart.md)
</dt> <dt>

[**ТБМ \_ сетсел**](tbm-setsel.md)
</dt> <dt>

[**ТБМ \_ сетселстарт**](tbm-setselstart.md)
</dt> </dl>

 

 





