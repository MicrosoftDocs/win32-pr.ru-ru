---
title: Сообщение TTM_DELTOOL (Коммктрл. h)
description: Удаляет инструмент из элемента управления ToolTip.
ms.assetid: 433b6f1c-3e9f-4e3a-9834-d447a3f9e6a5
keywords:
- элементы управления Windows сообщений TTM_DELTOOL
topic_type:
- apiref
api_name:
- TTM_DELTOOL
- TTM_DELTOOLA
- TTM_DELTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea54eefd2b9cc84b3aabe5dd600c5fcc32c7468cae01d1819b5fda7b631aeabd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166387"
---
# <a name="ttm_deltool-message"></a>\_Сообщение ТТМ делтул

Удаляет инструмент из элемента управления ToolTip.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . Элементы **HWND** и **uId** определяют средство, которое необходимо удалить, а член **кбсизе** должен задавать размер структуры. Все остальные элементы игнорируются.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТТМ \_ ДЕЛТУЛВ** (Юникод) и **ТТМ \_ делтула** (ANSI)<br/>                   |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**ТТМ \_ аддтул**](ttm-addtool.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Сведения об элементах управления ToolTip](tooltip-controls.md)
</dt> </dl>

 

 





