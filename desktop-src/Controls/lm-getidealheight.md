---
title: Сообщение LM_GETIDEALHEIGHT (Коммктрл. h)
description: LM_GETIDEALHEIGHT сообщение — получает предпочтительную высоту ссылки для текущей ширины элемента управления.
ms.assetid: bf6ef3c1-89bc-4c56-9384-085fd00234e1
keywords:
- элементы управления Windows сообщений LM_GETIDEALHEIGHT
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
ms.openlocfilehash: 7b0cd4b56da08baefe36d9ce1d669c4dbc4939883005c1cd45e59760566b468b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920444"
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

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





