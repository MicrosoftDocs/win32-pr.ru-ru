---
title: Сообщение TTM_TRACKPOSITION (Коммктрл. h)
description: Задает расположение подсказки для отслеживания.
ms.assetid: 9eb7c86c-78e6-442a-ad77-5fb919cab591
keywords:
- Элементы управления Windows для TTM_TRACKPOSITION сообщений
topic_type:
- apiref
api_name:
- TTM_TRACKPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6eab8184049d8bf876a7e782b9adc2091d5fac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071775"
---
# <a name="ttm_trackposition-message"></a>\_Сообщение ТТМ траккпоситион

Задает расположение подсказки для отслеживания.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) Указывает координату x точки, в которой будет отображаться подсказка отслеживания, в экранных координатах. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) Указывает координату y точки, в которой будет отображаться подсказка отслеживания, в экранных координатах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение для этого сообщения не используется.

## <a name="remarks"></a>Комментарии

Элемент управления ToolTip выбирает, где отображать окно подсказки в соответствии с координатами, предоставленными этим сообщением. В результате окно подсказки появится рядом с инструментом, которому оно соответствует. Чтобы окна подсказки отображались по конкретным координатам, включите флаг "TTF \_ Absolute" в элемент **Уфлагс** структуры [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) при добавлении средства.

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

[**ТТМ \_ траккактивате**](ttm-trackactivate.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Использование элементов управления ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

