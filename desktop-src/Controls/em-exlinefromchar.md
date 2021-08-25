---
title: Сообщение EM_EXLINEFROMCHAR (RichEdit. h)
description: Определяет, какая строка содержит указанный символ в элементе управления Rich Edit.
ms.assetid: 497482fb-9640-4063-a9f5-e0691b65225d
keywords:
- элементы управления Windows сообщений EM_EXLINEFROMCHAR
topic_type:
- apiref
api_name:
- EM_EXLINEFROMCHAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c41f5fbe540a4d765a48292d4ffd5b4af5849681dd1a82f4512b79348a6249d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915644"
---
# <a name="em_exlinefromchar-message"></a>\_Сообщение ЕКСЛИНЕФРОМЧАР EM

Определяет, какая строка содержит указанный символ в элементе управления Rich Edit.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется; оно должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Отсчитываемый от нуля индекс символа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение возвращает отсчитываемый от нуля индекс строки.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





