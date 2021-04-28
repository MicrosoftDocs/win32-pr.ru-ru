---
title: Сообщение TBM_GETUNICODEFORMAT (Коммктрл. h)
description: TBM_GETUNICODEFORMAT сообщение — получает флаг формата символов Юникода для элемента управления.
ms.assetid: cecd7e55-f482-4381-bde8-a60b8c5173eb
keywords:
- Элементы управления Windows для TBM_GETUNICODEFORMAT сообщений
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
ms.openlocfilehash: 82e7424a4e561ee8f8be79135309089fe4bb0bf9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104092"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ТБМ \_ сетуникодеформат**](tbm-setunicodeformat.md)
</dt> </dl>

 

 





