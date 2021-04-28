---
title: Сообщение LM_GETIDEALHEIGHT (Коммктрл. h)
description: LM_GETIDEALHEIGHT сообщение — получает предпочтительную высоту ссылки для текущей ширины элемента управления.
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
ms.openlocfilehash: 1d6e82f259124e6da285ed2357d48ca07d5f8c08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112402"
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

## <a name="remarks"></a>Remarks

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





