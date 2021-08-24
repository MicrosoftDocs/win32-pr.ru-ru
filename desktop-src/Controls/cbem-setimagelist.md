---
title: Сообщение CBEM_SETIMAGELIST (Коммктрл. h)
description: Задает список изображений для элемента управления ComboBoxEx.
ms.assetid: a4a8ed61-a532-4cf8-8291-c157ab0e7f31
keywords:
- элементы управления Windows сообщений CBEM_SETIMAGELIST
topic_type:
- apiref
api_name:
- CBEM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd83336d27bf8e47900554a6f3c36d2d767e5e8ddd4b8680b50050d87da79bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699264"
---
# <a name="cbem_setimagelist-message"></a>\_Сообщение кбем сетимажелист

Задает список изображений для элемента управления ComboBoxEx.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Описатель для списка изображений, который должен быть задан для элемента управления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер для списка изображений, который ранее был связан с элементом управления, или возвращает **значение NULL** , если список изображений ранее не был задан.

## <a name="remarks"></a>Remarks

> [!IMPORTANT]
> Высота изображений в списке изображений может изменить требования к размеру элемента управления ComboBoxEx. Рекомендуется изменить размер элемента управления после отправки этого сообщения, чтобы убедиться, что оно отображается правильно.

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





