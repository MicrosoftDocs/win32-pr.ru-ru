---
title: Сообщение LM_GETIDEALHEIGHT (Коммктрл. h)
description: Извлекает предпочтительную высоту ссылки для текущей ширины элемента управления.
ms.assetid: bf6ef3c1-89bc-4c56-9384-085fd00234e1
keywords:
- Элементы управления Windows для LM_GETIDEALHEIGHT сообщений
topic_type:
- apiref
api_name:
- LM_GETIDEALHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a92f24d63cc8f58e260d79dafd0555429d65d20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891454"
---
# <a name="lm_getidealheight-message"></a>\_Сообщение ЖЕТИДЕАЛХЕИГХТ LM

Извлекает предпочтительную высоту ссылки для текущей ширины элемента управления.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Целое число, представляющее предпочтительную высоту текста ссылки в пикселях.

## <a name="remarks"></a>Комментарии

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





