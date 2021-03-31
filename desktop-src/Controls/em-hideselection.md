---
title: Сообщение EM_HIDESELECTION (RichEdit. h)
description: Сообщение EM \_ хидеселектион скрывает или отображает выделенный фрагмент в элементе управления Rich Edit.
ms.assetid: 1245618f-c9e6-4876-9133-6009370cdb97
keywords:
- Элементы управления Windows для EM_HIDESELECTION сообщений
topic_type:
- apiref
api_name:
- EM_HIDESELECTION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a5690e52c2a25f5a359de205ac1584e1ef45ed4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988267"
---
# <a name="em_hideselection-message"></a>\_Сообщение ХИДЕСЕЛЕКТИОН EM

Сообщение **EM \_ хидеселектион** скрывает или отображает выделенный фрагмент в элементе управления Rich Edit.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Значение, указывающее, следует ли скрывать или отображать выделенный фрагмент. Если этот параметр равен нулю, выводится выбранный фрагмент. В противном случае выделение будет скрыто.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется; оно должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





