---
title: Сообщение EM_GETPUNCTUATION (RichEdit. h)
description: Возвращает текущие знаки пунктуации для элемента управления Rich Edit.
ms.assetid: 1c04967b-d75e-4f54-b35b-cd50bac9cdfa
keywords:
- Элементы управления Windows для EM_GETPUNCTUATION сообщений
topic_type:
- apiref
api_name:
- EM_GETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 158c26deca3328d9cdbed7ffe7cf885b0582d1a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136978"
---
# <a name="em_getpunctuation-message"></a>\_Сообщение EM

Возвращает текущие знаки пунктуации для элемента управления Rich Edit.

> [!Note]  
> Это сообщение поддерживается только в версиях Microsoft Rich Edit 1,0, поддерживающих азиатские языки. Он не поддерживается в каких-либо более поздних версиях расширенного редактирования.

 

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Тип пунктуации может иметь одно из следующих значений.



| Значение                                                                                                                                                      | Значение                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <dt>**\_ведущий ПК**</dt> </dl>       | Начальные знаки пунктуации<br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <dt>**ПК \_ ниже**</dt> </dl> | Следующие знаки пунктуации<br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <dt>**\_Разделитель компьютеров**</dt> </dl> | Разделитель<br/>                        |
| <span id="PC_OVERFLOW"></span><span id="pc_overflow"></span><dl> <dt>**\_переполнение ПК**</dt> </dl>    | Не поддерживается<br/>                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**пунктуации**](/windows/desktop/api/Richedit/ns-richedit-punctuation) , которая получает символы пунктуации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если операция завершилась удачно, возвращаемое значение будет ненулевым.

Если операция завершается ошибкой, возвращаемое значение равно нулю.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**EM \_ сетпунктуатион**](em-setpunctuation.md)
</dt> <dt>

[**ЗНАКИ ПРЕПИНАНИЯ**](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





