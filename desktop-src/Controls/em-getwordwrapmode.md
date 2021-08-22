---
title: Сообщение EM_GETWORDWRAPMODE (RichEdit. h)
description: Возвращает текущие параметры переноса по словам и разрыва слов для элемента управления Rich Edit.
ms.assetid: a87d80d6-2e9e-40ba-9348-a1cc1ef8ec10
keywords:
- элементы управления Windows сообщений EM_GETWORDWRAPMODE
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
ms.openlocfilehash: aef3127e5ce3652e9103dfa0e030d66ec7b1b085bc4b60d0cf0bb3f03a30d3fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437954"
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

## <a name="remarks"></a>Remarks

Это сообщение не должно отправляться с помощью определяемой приложением, процедурой разбиения по словам.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





