---
title: Сообщение EM_EXSETSEL (RichEdit. h)
description: Выбирает диапазон символов или объектов модели COM в элементе управления Microsoft Rich Edit.
ms.assetid: 85a0d1d4-1826-4ac5-b823-de81a051441d
keywords:
- элементы управления Windows сообщений EM_EXSETSEL
topic_type:
- apiref
api_name:
- EM_EXSETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e35840e404f295b7d3ed6ddd5dddf4c77076c236eb3260f6f719b152cef207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915654"
---
# <a name="em_exsetsel-message"></a>\_Сообщение ЕКССЕТСЕЛ EM

Выбирает диапазон символов или объектов модели COM в элементе управления Microsoft Rich Edit.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется; оно должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Структура [**чарранже**](/windows/desktop/api/Richedit/ns-richedit-charrange) , указывающая диапазон выбора.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение является фактически установленным выделением.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





