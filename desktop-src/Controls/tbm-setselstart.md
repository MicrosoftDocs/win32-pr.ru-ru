---
title: Сообщение TBM_SETSELSTART (Коммктрл. h)
description: Задает начальную логическую точку текущего диапазона выбора в TrackBar. Это сообщение пропускается, если значение TrackBar не имеет \_ стиля TBS енаблеселранже.
ms.assetid: eec1019c-6dbe-48c4-9c9d-72d657e80b83
keywords:
- элементы управления Windows сообщений TBM_SETSELSTART
topic_type:
- apiref
api_name:
- TBM_SETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f8cfdc938da5c7f5904e79f55177fe6f8eccba10f37dfdadb613c581cc809fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829318"
---
# <a name="tbm_setselstart-message"></a>\_Сообщение ТБМ сетселстарт

Задает начальную логическую точку текущего диапазона выбора в TrackBar. Это сообщение пропускается, если значение TrackBar не имеет стиля [**TBS \_ енаблеселранже**](trackbar-control-styles.md) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Флаг перерисовки. Если этот параметр имеет **значение true**, сообщение перерисовывается после установки диапазона выбора. Если этот параметр имеет **значение false**, то сообщение задает диапазон выбора, но не перерисовывает линейку.

</dd> <dt>

*lParam* 
</dt> <dd>

Начальное расположение диапазона выбора.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**ТБМ \_ жетселенд**](tbm-getselend.md)
</dt> <dt>

[**ТБМ \_ жетселстарт**](tbm-getselstart.md)
</dt> <dt>

[**ТБМ \_ сетсел**](tbm-setsel.md)
</dt> <dt>

[**ТБМ \_ сетселенд**](tbm-setselend.md)
</dt> </dl>

 

 





