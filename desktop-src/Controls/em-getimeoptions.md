---
title: Сообщение EM_GETIMEOPTIONS (RichEdit. h)
description: Извлекает текущие параметры редактора метода ввода (IME).
ms.assetid: 81ec89b9-dabd-487e-805e-e3c2e58e3068
keywords:
- элементы управления Windows сообщений EM_GETIMEOPTIONS
topic_type:
- apiref
api_name:
- EM_GETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea4513189014969dbfdf69a0ad257cbfde6a4ff99c2499f478c4865100a23c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049064"
---
# <a name="em_getimeoptions-message"></a>\_Сообщение ЖЕТИМЕОПТИОНС EM

Извлекает текущие параметры редактора метода ввода (IME).

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

Это сообщение возвращает один или несколько значений флагов параметров IME, описанных в сообщении [**EM \_ сетимеоптионс**](em-setimeoptions.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**EM \_ сетимеоптионс**](em-setimeoptions.md)
</dt> </dl>

 

 





