---
title: Сообщение EM_GETOPTIONS (RichEdit. h)
description: Возвращает широкие параметры элемента управления редактированием.
ms.assetid: 183f0fed-8666-4ed5-ac48-362c818378d2
keywords:
- элементы управления Windows сообщений EM_GETOPTIONS
topic_type:
- apiref
api_name:
- EM_GETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cba85b5fe3ffd47763d25b9ca13bf10f6202a6876e25d300f66d9af3852edd5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019522"
---
# <a name="em_getoptions-message"></a>\_Сообщение о параметре EM

Возвращает широкие параметры элемента управления редактированием.

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

Это сообщение Возвращает сочетание текущих значений флагов параметров, описанных в сообщении [**EM \_ сетоптионс**](em-setoptions.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**EM \_ сетоптионс**](em-setoptions.md)
</dt> </dl>

 

 





