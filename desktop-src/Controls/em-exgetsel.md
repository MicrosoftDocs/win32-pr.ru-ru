---
title: Сообщение EM_EXGETSEL (RichEdit. h)
description: Получает позиции начального и конечного символов выделения в элементе управления Rich Edit.
ms.assetid: 60fcf13e-6c45-4f4e-9b54-70f0985122fb
keywords:
- Элементы управления Windows для EM_EXGETSEL сообщений
topic_type:
- apiref
api_name:
- EM_EXGETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b97fb43a76f0f8ac91dd16c0cfa5700c5431eb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491487"
---
# <a name="em_exgetsel-message"></a>\_Сообщение ЕКСЖЕТСЕЛ EM

Получает позиции начального и конечного символов выделения в элементе управления Rich Edit.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется; оно должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Структура [**чарранже**](/windows/desktop/api/Richedit/ns-richedit-charrange) , которая получает диапазон выбора.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**чарранже**](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> </dl>

 

 





