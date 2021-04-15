---
title: Сообщение EM_EXLINEFROMCHAR (RichEdit. h)
description: Определяет, какая строка содержит указанный символ в элементе управления Rich Edit.
ms.assetid: 497482fb-9640-4063-a9f5-e0691b65225d
keywords:
- Элементы управления Windows для EM_EXLINEFROMCHAR сообщений
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
ms.openlocfilehash: ce904725c5dc63732bae07cfaa95b41558db11d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493350"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





