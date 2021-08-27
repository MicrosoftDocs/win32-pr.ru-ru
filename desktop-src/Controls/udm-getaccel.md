---
title: Сообщение UDM_GETACCEL (Коммктрл. h)
description: Получает сведения о ускорении для элемента управления "вверх/вниз".
ms.assetid: 794538d6-ca01-4f05-82d1-ce7bc0f76f64
keywords:
- элементы управления Windows сообщений UDM_GETACCEL
topic_type:
- apiref
api_name:
- UDM_GETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3603f364a6caa4f4726460e4b5b71e0d79564fbe9178414576fbed2ce5f5777d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132194"
---
# <a name="udm_getaccel-message"></a>\_Сообщение о неполучении UDM

Получает сведения о ускорении для элемента управления "вверх/вниз".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Число элементов в массиве, заданном параметром *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на массив структур [**удакцел**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) , которые получают сведения о ускорении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение — это число ускорителей, установленных в данный момент для элемента управления.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_СЕТАКЦЕЛ UDM**](udm-setaccel.md)
</dt> </dl>

 

 





