---
title: Сообщение LM_GETIDEALSIZE (Коммктрл. h)
description: LM_GETIDEALSIZE сообщение — получает предпочтительную высоту ссылки для текущей ширины элемента управления.
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- элементы управления Windows сообщений LM_GETIDEALSIZE
topic_type:
- apiref
api_name:
- LM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035a919aabeb5d07587c7d9e4fc97e5edc728de4ec8fc476448dca62658f1ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958381"
---
# <a name="lm_getidealsize-message"></a>\_Сообщение ЖЕТИДЕАЛСИЗЕ LM

Извлекает предпочтительную высоту ссылки для текущей ширины элемента управления.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Максимальная ширина ссылки в пикселях.</dd> <dt>

*lParam* \[ заполняет\]
</dt> <dd>При возвращении этого сообщения содержит указатель на структуру <a href="/previous-versions//dd145106(v=vs.85)">**размера**</a> . Элемент **CY** этой структуры указывает идеальную высоту элемента управления для заданной ширины. Он корректирует элемент **CX** на фактически необходимый объем пространства.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Целое число, представляющее предпочтительную высоту текста ссылки в пикселях.

## <a name="remarks"></a>Remarks

> [!Note]  
> Чтобы использовать этот API, необходимо предоставить манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

