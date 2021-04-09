---
title: Сообщение LVM_CREATEDRAGIMAGE (Коммктрл. h)
description: Создает список изображений для перетаскивания для указанного элемента. Это сообщение можно отправить явно или с помощью \_ макроса Креатедрагимаже ListView.
ms.assetid: face4c8f-01ff-4f5a-a468-e306a50dae35
keywords:
- Элементы управления Windows для LVM_CREATEDRAGIMAGE сообщений
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
ms.openlocfilehash: ace975b178fee85e2794b518a78b40b375c65ae7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135139"
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

## <a name="remarks"></a>Комментарии

Приложение несет ответственность за уничтожение списка изображений, когда он больше не нужен.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

