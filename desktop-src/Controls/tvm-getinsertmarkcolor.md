---
title: Сообщение TVM_GETINSERTMARKCOLOR (Коммктрл. h)
description: Извлекает цвет, используемый для рисования метки вставки в представлении в виде дерева. Это сообщение можно отправить явно или с помощью \_ макроса Жетинсертмаркколор TreeView.
ms.assetid: d1fba4bb-1bdb-44e0-8083-b564cdafc055
keywords:
- Элементы управления Windows для TVM_GETINSERTMARKCOLOR сообщений
topic_type:
- apiref
api_name:
- TVM_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61416a428fed88ece8f50ca640dd9a05ec131614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989282"
---
# <a name="tvm_getinsertmarkcolor-message"></a>\_Сообщение TVM жетинсертмаркколор

Извлекает цвет, используемый для рисования метки вставки в представлении в виде дерева. Это сообщение можно отправить явно или с помощью макроса [**\_ жетинсертмаркколор TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение [**COLORREF**](/windows/desktop/gdi/colorref) , содержащее текущий цвет отметки вставки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**TVM \_ сетинсертмаркколор**](tvm-setinsertmarkcolor.md)
</dt> </dl>

 

