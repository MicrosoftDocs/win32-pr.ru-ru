---
title: Сообщение TBM_GETUNICODEFORMAT (Коммктрл. h)
description: TBM_GETUNICODEFORMAT сообщение — получает флаг формата символов Юникода для элемента управления.
ms.assetid: cecd7e55-f482-4381-bde8-a60b8c5173eb
keywords:
- элементы управления Windows сообщений TBM_GETUNICODEFORMAT
topic_type:
- apiref
api_name:
- TBM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e15f5b12a60b58958dad1364848120f391c91906bb6057727f3a4e22b8a7813
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046174"
---
# <a name="tbm_getunicodeformat-message"></a>\_Сообщение ТБМ жетуникодеформат

Возвращает флаг формата символов Юникода для элемента управления.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает флаг формата Юникода для элемента управления. Если это значение не равно нулю, то элемент управления использует символы Юникода. Если это значение равно нулю, то элемент управления использует символы ANSI.

## <a name="remarks"></a>Remarks

Обсуждение этого сообщения см. в примечаниях по [**CCM \_ жетуникодеформат**](ccm-getunicodeformat.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ТБМ \_ сетуникодеформат**](tbm-setunicodeformat.md)
</dt> </dl>

 

 





