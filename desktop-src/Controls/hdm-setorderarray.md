---
title: Сообщение HDM_SETORDERARRAY (Коммктрл. h)
description: Задает порядок элементов заголовка слева направо. Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса сетордераррай.
ms.assetid: 094c424f-10bd-484d-8236-937811b703a6
keywords:
- Элементы управления Windows для HDM_SETORDERARRAY сообщений
topic_type:
- apiref
api_name:
- HDM_SETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f07874bfc102babec18b142a087b14e330044ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490866"
---
# <a name="hdm_setorderarray-message"></a>\_Сообщение СЕТОРДЕРАРРАЙ HDM

Задает порядок элементов заголовка слева направо. Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ сетордераррай**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Размер буфера в параметре *lParam* в элементах. Это значение должно равняться значению, возвращаемому [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на массив, указывающий порядок отображения элементов слева направо. Например, если содержимое массива равно {2,0,1} , элемент управления отображает элемент 2, элемент 0 и элемент 1, слева направо.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





