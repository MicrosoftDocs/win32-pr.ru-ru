---
title: Сообщение EM_GETIMEOPTIONS (RichEdit. h)
description: Извлекает текущие параметры редактора метода ввода (IME).
ms.assetid: 81ec89b9-dabd-487e-805e-e3c2e58e3068
keywords:
- Элементы управления Windows для EM_GETIMEOPTIONS сообщений
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
ms.openlocfilehash: 7bd805f2407fbe9e055df3d9174f106d33991aca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136659"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EM \_ сетимеоптионс**](em-setimeoptions.md)
</dt> </dl>

 

 





