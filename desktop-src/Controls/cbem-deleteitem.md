---
title: Сообщение CBEM_DELETEITEM (Коммктрл. h)
description: Удаляет элемент из элемента управления ComboBoxEx.
ms.assetid: 688cf388-54ba-4b45-88d7-628da49d8615
keywords:
- Элементы управления Windows для CBEM_DELETEITEM сообщений
topic_type:
- apiref
api_name:
- CBEM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa3034f79dffabcd7d7aa780582646e17d30b62f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654709"
---
# <a name="cbem_deleteitem-message"></a>\_Сообщение кбем DELETEITEM

Удаляет элемент из элемента управления ComboBoxEx.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Отсчитываемый от нуля индекс удаляемого элемента.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа INT, представляющее количество элементов, остающихся в элементе управления. Если *ииндекс* является недопустимым, сообщение ВОЗВРАЩАЕТ значение CB \_ Err.

## <a name="remarks"></a>Комментарии

Это сообщение сопоставляется с полем со списком элемент управления "сообщение [**CB \_ делетестринг**](cb-deletestring.md)".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





