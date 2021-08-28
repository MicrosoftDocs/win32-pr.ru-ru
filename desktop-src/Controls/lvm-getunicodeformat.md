---
title: Сообщение LVM_GETUNICODEFORMAT (Коммктрл. h)
description: Возвращает флаг формата символов Юникода для элемента управления. Это сообщение можно отправить явным образом или использовать \_ макрос Жетуникодеформат ListView.
ms.assetid: b0598b60-4d0e-4c68-b63a-e614c6268129
keywords:
- элементы управления Windows сообщений LVM_GETUNICODEFORMAT
topic_type:
- apiref
api_name:
- LVM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b3166d7349bf138fa853523c019a4c1db86e3f1a2d81a6da86c4ef25b5ed405
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019262"
---
# <a name="lvm_getunicodeformat-message"></a>\_Сообщение LVM жетуникодеформат

Возвращает флаг формата символов Юникода для элемента управления. Это сообщение можно отправить явным образом или использовать макрос [**\_ жетуникодеформат ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getunicodeformat) .

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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**LVM \_ сетуникодеформат**](lvm-setunicodeformat.md)
</dt> </dl>

 

 





