---
title: Сообщение TVM_GETINSERTMARKCOLOR (Коммктрл. h)
description: Извлекает цвет, используемый для рисования метки вставки в представлении в виде дерева. Это сообщение можно отправить явно или с помощью \_ макроса Жетинсертмаркколор TreeView.
ms.assetid: d1fba4bb-1bdb-44e0-8083-b564cdafc055
keywords:
- элементы управления Windows сообщений TVM_GETINSERTMARKCOLOR
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
ms.openlocfilehash: 38c784f6b3c363d68472270f0f52cb97cea7c13b6eb709d1aba4975d3cd97bca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834154"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**TVM \_ сетинсертмаркколор**](tvm-setinsertmarkcolor.md)
</dt> </dl>

 

