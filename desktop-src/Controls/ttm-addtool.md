---
title: Сообщение TTM_ADDTOOL (Коммктрл. h)
description: Регистрирует инструмент с помощью элемента управления ToolTip.
ms.assetid: c974866b-20e7-45bc-914e-9dcf9af161e0
keywords:
- Элементы управления Windows для TTM_ADDTOOL сообщений
topic_type:
- apiref
api_name:
- TTM_ADDTOOL
- TTM_ADDTOOLA
- TTM_ADDTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29dad3e297f8c3430f18286afa9a998eaf578a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654507"
---
# <a name="ttm_addtool-message"></a>\_Сообщение ТТМ аддтул

Регистрирует инструмент с помощью элемента управления ToolTip.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , содержащую сведения, необходимые элементу управления ToolTip для показа текста для инструмента. Перед отправкой этого сообщения необходимо заполнить элемент **кбсизе** этой структуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТТМ \_ АДДТУЛВ** (Юникод) и **ТТМ \_ аддтула** (ANSI)<br/>                   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**ТТМ \_ делтул**](ttm-deltool.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Сведения об элементах управления ToolTip](tooltip-controls.md)
</dt> </dl>

 

 





