---
title: Пользовательские значения Draw (Коммктрл. h)
description: В этом разделе перечислены значения, используемые для обнаружения частей элемента управления TrackBar.
ms.assetid: 154321c7-99f8-4ed5-a5ff-fb96126b43c7
topic_type:
- apiref
api_name:
- TBCD_CHANNEL
- TBCD_THUMB
- TBCD_TICS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccf05ab951fdc83ec5be414688be56d710ba0d98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648637"
---
# <a name="custom-draw-values"></a>Пользовательские значения рисования

В этом разделе перечислены значения, используемые для обнаружения частей элемента управления TrackBar.



| Константа                                                                                                                                                   | Описание                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <dt>**\_канал тбкд**</dt> </dl> | Определяет канал, вдоль которого проводятся маркеры Thumb элемента управления TrackBar.<br/>                        |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <dt>**ТБКД \_ бегунок**</dt> </dl>       | Определяет маркер Thumb элемента управления TrackBar. Это часть элемента управления, который перемещает пользователь.<br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <dt>**ТБКД \_ ТИКС**</dt> </dl>          | Определяет деления, отображаемые вдоль границы элемента управления TrackBar.<br/>                      |



## <a name="remarks"></a>Комментарии

Пользовательские значения рисования, например, задаются в элементе **двитемспек** структуры [**нмкустомдрав**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





