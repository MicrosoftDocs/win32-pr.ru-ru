---
title: Сообщение EM_GETPARAFORMAT (RichEdit. h)
description: Извлекает форматирование абзаца текущего выделения в элементе управления Rich Edit.
ms.assetid: 79a7d34f-5da1-452d-b31f-b2eec913f5cb
keywords:
- элементы управления Windows сообщений EM_GETPARAFORMAT
topic_type:
- apiref
api_name:
- EM_GETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eda99d1fefc0e2a13cc989726c86588103b7f94d7042b98393709cf4a2cd5f29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048854"
---
# <a name="em_getparaformat-message"></a>\_Сообщение ЖЕТПАРАФОРМАТ EM

Извлекает форматирование абзаца текущего выделения в элементе управления Rich Edit.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется; оно должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**формата**](/windows/desktop/api/Richedit/ns-richedit-paraformat) с параметром, которая получает атрибуты форматирования абзаца для текущего выделения.

Если выбрано более одного абзаца, то структура получает атрибуты первого абзаца, а элемент **двмаск** указывает, какие атрибуты согласованы по всему выделению.

Microsoft Rich Edit 2,0 и более поздние версии: этот параметр может быть указателем на структуру [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) , которая является РАСШИРЕНИЕМ структуры [**формата**](/windows/desktop/api/Richedit/ns-richedit-paraformat) данных. Перед отправкой сообщения **EM \_ жетпараформат** установите элемент **кбсизе** в структуре, чтобы указать версию структуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение возвращает значение элемента **двмаск** структуры [**формата**](/windows/desktop/api/Richedit/ns-richedit-paraformat) данных.

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

[**ФОРМАТ \**](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





