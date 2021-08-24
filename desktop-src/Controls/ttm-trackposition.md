---
title: Сообщение TTM_TRACKPOSITION (Коммктрл. h)
description: Задает расположение подсказки для отслеживания.
ms.assetid: 9eb7c86c-78e6-442a-ad77-5fb919cab591
keywords:
- элементы управления Windows сообщений TTM_TRACKPOSITION
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
ms.openlocfilehash: 547af5014bbf897d320894c4924911b830997ec3d8532e2ce2c7b63f361a11da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119542833"
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

## <a name="remarks"></a>Remarks

Элемент управления ToolTip выбирает, где отображать окно подсказки в соответствии с координатами, предоставленными этим сообщением. В результате окно подсказки появится рядом с инструментом, которому оно соответствует. Чтобы окна подсказки отображались по конкретным координатам, включите флаг "TTF \_ Absolute" в элемент **Уфлагс** структуры [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) при добавлении средства.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
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

 

