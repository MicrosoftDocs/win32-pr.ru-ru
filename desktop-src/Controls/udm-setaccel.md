---
title: Сообщение UDM_SETACCEL (Коммктрл. h)
description: Задает ускорение для элемента управления "вверх/вниз".
ms.assetid: af1d0a34-13ba-4bda-82f5-d7afab6bb1ed
keywords:
- элементы управления Windows сообщений UDM_SETACCEL
topic_type:
- apiref
api_name:
- UDM_SETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc746e33c14de0dd177ecc31fc237be7cb8be36280bb2a5ceadff31d2b286ec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957743"
---
# <a name="udm_setaccel-message"></a>\_Сообщение СЕТАКЦЕЛ UDM

Задает ускорение для элемента управления "вверх/вниз".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Число структур [**удакцел**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) , заданных параметром *аакцелс*.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на массив структур [**удакцел**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) , содержащих сведения об ускорении. Элементы должны быть отсортированы в порядке возрастания на основе элемента **NSEC** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_UDM**](udm-getaccel.md)
</dt> </dl>

 

 





