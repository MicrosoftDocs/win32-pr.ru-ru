---
title: Сообщение TBM_SETSEL (Коммктрл. h)
description: Задает начальную и конечную позиции для доступного диапазона выбора в TrackBar.
ms.assetid: 71f5b9f8-4850-44a8-8acf-adca9bda84c3
keywords:
- элементы управления Windows сообщений TBM_SETSEL
topic_type:
- apiref
api_name:
- TBM_SETSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d055b317cc6db5e17edbe57bc57e6dbfe287274788718e8e2a920e1f25d9316b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829336"
---
# <a name="tbm_setsel-message"></a>\_Сообщение ТБМ сетсел

Задает начальную и конечную позиции для доступного диапазона выбора в TrackBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Флаг перерисовки. Если этот параметр имеет **значение true**, сообщение перерисовывается после установки диапазона выбора. Если этот параметр имеет **значение false**, то сообщение задает диапазон выбора, но не перерисовывает линейку.

</dd> <dt>

*lParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) задает начальную логическую точку для диапазона выбора, а [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает конечную логическую точку.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Это сообщение пропускается, если значение TrackBar не имеет стиля [**TBS \_ енаблеселранже**](trackbar-control-styles.md) .

**ТБМ \_ СЕТСЕЛ** позволяет ограничить указатель только частью диапазона, доступного индикатору выполнения.

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

[**ТБМ \_ сетселенд**](tbm-setselend.md)
</dt> <dt>

[**ТБМ \_ сетселстарт**](tbm-setselstart.md)
</dt> </dl>

 

