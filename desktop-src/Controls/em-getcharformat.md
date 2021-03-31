---
title: Сообщение EM_GETCHARFORMAT (RichEdit. h)
description: Определяет форматирование символов в элементе управления Rich Edit.
ms.assetid: 210b8719-5ed7-49f2-bd93-8a4e1efab1e8
keywords:
- Элементы управления Windows для EM_GETCHARFORMAT сообщений
topic_type:
- apiref
api_name:
- EM_GETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd71db4d3a13f2acfe33c2843b0d9aad46c6f9fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071708"
---
# <a name="em_getcharformat-message"></a>\_Сообщение ЖЕТЧАРФОРМАТ EM

Определяет форматирование символов в элементе управления Rich Edit.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Задает диапазон текста, из которого извлекается форматирование. Может быть одним из указанных далее.



| Значение                                                                                                                                                         | Значение                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <dt>**\_по умолчанию — SCF**</dt> </dl>       | Форматирование символов по умолчанию.<br/>             |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <dt>**Выбор параметров SCF \_**</dt> </dl> | Форматирование символов текущего выделения.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Структура [**чарформат**](/windows/win32/api/richedit/ns-richedit-charformata) , которая получает атрибуты первого символа. Элемент **двмаск** указывает, какие атрибуты согласованы по всему выделению. Например, если все выделенные фрагменты выделены курсивом или не курсивом, то \_ устанавливается курсивом. Если выделение частично выделено курсивом, а частично нет, \_ значит, не задано значение CFM Italic.

Microsoft Rich Edit 2,0 и более поздние версии: этот параметр может быть указателем на структуру [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) , которая является расширением структуры [**чарформат**](/windows/win32/api/richedit/ns-richedit-charformata) . Перед отправкой сообщения **EM \_ жетчарформат** установите элемент **кбсизе** в структуре, чтобы указать версию структуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение возвращает значение элемента **двмаск** структуры [**чарформат**](/windows/win32/api/richedit/ns-richedit-charformata) .

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

[**чарформат**](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





