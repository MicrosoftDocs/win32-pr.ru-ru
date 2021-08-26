---
title: Сообщение EM_SETPUNCTUATION (RichEdit. h)
description: Задает знаки пунктуации для элемента управления Rich Edit.
ms.assetid: c0c8ad14-63e2-4be8-8fc0-6b8ef9be4522
keywords:
- элементы управления Windows сообщений EM_SETPUNCTUATION
topic_type:
- apiref
api_name:
- EM_SETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5e0856c1ee1882695dc5e6d7dfdd6b72ea0f6c4f16ee7396bbfde2b76b49b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062904"
---
# <a name="em_setpunctuation-message"></a>\_Сообщение СЕТПУНКТУАТИОН EM

Задает знаки пунктуации для элемента управления Rich Edit.

> [!Note]  
> Это сообщение поддерживается только в версиях Microsoft Rich Edit 1,0, поддерживающих азиатские языки. Он не поддерживается в каких-либо более поздних версиях.

 

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указывает тип пунктуации, который может принимать одно из следующих значений.



| Значение                                                                                                                                                      | Значение                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <dt>**\_ведущий ПК**</dt> </dl>       | Начальные знаки пунктуации.<br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <dt>**ПК \_ ниже**</dt> </dl> | Следующие знаки пунктуации.<br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <dt>**\_Разделитель компьютеров**</dt> </dl> | Разделитель.<br/>                        |
| <span id="PC_OVERFLOW_"></span><span id="pc_overflow_"></span><dl> <dt>**ПК \_ ПЕРЕПОЛНЕНие**</dt> </dl> | Не поддерживается.<br/>                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**пунктуации**](/windows/desktop/api/Richedit/ns-richedit-punctuation) , содержащую знаки препинания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если операция завершилась удачно, возвращаемое значение будет ненулевым.

Если операция завершается ошибкой, возвращаемое значение равно нулю.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**\_знаки EM**](em-getpunctuation.md)
</dt> <dt>

[**ЗНАКИ ПРЕПИНАНИЯ**](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





