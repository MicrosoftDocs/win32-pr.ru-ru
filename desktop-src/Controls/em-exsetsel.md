---
title: Сообщение EM_EXSETSEL (RichEdit. h)
description: Выбирает диапазон символов или объектов модели COM в элементе управления Microsoft Rich Edit.
ms.assetid: 85a0d1d4-1826-4ac5-b823-de81a051441d
keywords:
- Элементы управления Windows для EM_EXSETSEL сообщений
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
ms.openlocfilehash: 6939156fb1a8f35e03527e64a4c6f5185180668d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892173"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





