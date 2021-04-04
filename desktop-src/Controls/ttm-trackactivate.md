---
title: Сообщение TTM_TRACKACTIVATE (Коммктрл. h)
description: Активирует или деактивирует подсказку отслеживания.
ms.assetid: 6cf43377-a772-4749-81c4-a685998092e5
keywords:
- Элементы управления Windows для TTM_TRACKACTIVATE сообщений
topic_type:
- apiref
api_name:
- TTM_TRACKACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3d0a6caf110045d694208c63aa81d63c265c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988901"
---
# <a name="ttm_trackactivate-message"></a>\_Сообщение ТТМ траккактивате

Активирует или деактивирует подсказку отслеживания.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Значение, указывающее, активируется или деактивируется отслеживание. Значение может быть одним из следующих.



| Значение                                                                                                                                | Значение                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>**УСЛОВИЯ**</dt> </dl>    | Активация отслеживания.<br/>   |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>**ISFALSE**</dt> </dl> | Отключить отслеживание.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , определяющую инструмент, к которому применяется это сообщение. Элементы **HWND** и **uId** определяют средство, а член **кбсизе** задает размер структуры. Все остальные элементы игнорируются.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение для этого сообщения не используется.

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

[**ТТМ \_ траккпоситион**](ttm-trackposition.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Использование элементов управления ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

 





