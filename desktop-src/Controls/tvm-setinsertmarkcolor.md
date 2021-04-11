---
title: Сообщение TVM_SETINSERTMARKCOLOR (Коммктрл. h)
description: Задает цвет, используемый для отображения метки вставки для представления в виде дерева. Это сообщение можно отправить явно или с помощью \_ макроса Сетинсертмаркколор TreeView.
ms.assetid: c82304a8-3726-42c0-81e7-90d8f8205ead
keywords:
- Элементы управления Windows для TVM_SETINSERTMARKCOLOR сообщений
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92668b1137b089f9a09cc9a34d63d472742bce4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136230"
---
# <a name="tvm_setinsertmarkcolor-message"></a>\_Сообщение TVM сетинсертмаркколор

Задает цвет, используемый для отображения метки вставки для представления в виде дерева. Это сообщение можно отправить явно или с помощью макроса [**\_ сетинсертмаркколор TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Значение [**COLORREF**](/windows/desktop/gdi/colorref) , содержащее новый цвет метки вставки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **COLORREF** , содержащее предыдущий цвет отметки вставки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**TVM \_ жетинсертмаркколор**](tvm-getinsertmarkcolor.md)
</dt> </dl>

 

