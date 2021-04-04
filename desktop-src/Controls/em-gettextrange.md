---
title: Сообщение EM_GETTEXTRANGE (RichEdit. h)
description: Извлекает указанный диапазон символов из элемента управления Rich Edit.
ms.assetid: 18398963-eb2c-4f64-99f5-9614a5d34b52
keywords:
- Элементы управления Windows для EM_GETTEXTRANGE сообщений
topic_type:
- apiref
api_name:
- EM_GETTEXTRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d68c4089bbe2cc09daa39d69e9094a4abaead787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989088"
---
# <a name="em_gettextrange-message"></a>\_Сообщение ЖЕТТЕКСТРАНЖЕ EM

Извлекает указанный диапазон символов из элемента управления Rich Edit.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется; оно должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) , указывающую диапазон извлекаемых символов, и буфер для копирования символов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Сообщение возвращает число скопированных символов, не включая завершающий символ null.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea)
</dt> </dl>

 

 





