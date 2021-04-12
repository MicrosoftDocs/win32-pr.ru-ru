---
title: Сообщение EM_GETWORDWRAPMODE (RichEdit. h)
description: Возвращает текущие параметры переноса по словам и разрыва слов для элемента управления Rich Edit.
ms.assetid: a87d80d6-2e9e-40ba-9348-a1cc1ef8ec10
keywords:
- Элементы управления Windows для EM_GETWORDWRAPMODE сообщений
topic_type:
- apiref
api_name:
- EM_GETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efc8a2b6d17623964eb0d3714c1c099f47fc788a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489459"
---
# <a name="em_getwordwrapmode-message"></a>\_Сообщение ЖЕТВОРДВРАПМОДЕ EM

Возвращает текущие параметры переноса по словам и разрыва слов для элемента управления Rich Edit.

> [!Note]  
> Это сообщение поддерживается только в версиях Microsoft Rich Edit 1,0, поддерживающих азиатские языки. Он не поддерживается в каких-либо более поздних версиях расширенного редактирования.

 

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Сообщение возвращает текущие параметры переноса по словам и разрыва слов.

## <a name="remarks"></a>Комментарии

Это сообщение не должно отправляться с помощью определяемой приложением, процедурой разбиения по словам.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





