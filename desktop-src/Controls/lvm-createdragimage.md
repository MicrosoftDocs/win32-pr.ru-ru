---
title: Сообщение LVM_CREATEDRAGIMAGE (Коммктрл. h)
description: Создает список изображений для перетаскивания для указанного элемента. Это сообщение можно отправить явно или с помощью \_ макроса Креатедрагимаже ListView.
ms.assetid: face4c8f-01ff-4f5a-a468-e306a50dae35
keywords:
- элементы управления Windows сообщений LVM_CREATEDRAGIMAGE
topic_type:
- apiref
api_name:
- LVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d551dfa7b14ecff8c9fd1efe015e173403c1b5981f294a18b3180a42cc03de63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412002"
---
# <a name="lvm_createdragimage-message"></a>\_Сообщение LVM креатедрагимаже

Создает список изображений для перетаскивания для указанного элемента. Это сообщение можно отправить явно или с помощью макроса [**\_ креатедрагимаже ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс элемента.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**точек**](/previous-versions//dd162805(v=vs.85)) , которая получает начальное расположение верхнего левого угла изображения в координатах представления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер в список изображений перетаскивания в случае успеха или **значение NULL** в противном случае.

## <a name="remarks"></a>Remarks

Приложение несет ответственность за уничтожение списка изображений, когда он больше не нужен.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

