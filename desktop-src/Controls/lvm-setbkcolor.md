---
title: Сообщение LVM_SETBKCOLOR (Коммктрл. h)
description: Задает цвет фона для элемента управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Сетбкколор ListView.
ms.assetid: d579249d-421d-4e7e-8992-4c7fd7277593
keywords:
- элементы управления Windows сообщений LVM_SETBKCOLOR
topic_type:
- apiref
api_name:
- LVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b8acfb07a91fae470d893facf6af051397fac2f0d9f4f6990ab4ff67744d8ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119391614"
---
# <a name="lvm_setbkcolor-message"></a>\_Сообщение LVM сетбкколор

Задает цвет фона для элемента управления "представление списка". Это сообщение можно отправить явно или с помощью макроса [**\_ сетбкколор ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Цвет фона для установки или значение CLR \_ None для отсутствия цвета фона. Элементы управления "представление списка" с фоновыми цветами перерисуются значительно быстрее, чем без фоновых цветов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





