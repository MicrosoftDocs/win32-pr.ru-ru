---
title: Сообщение HDM_GETUNICODEFORMAT (Коммктрл. h)
description: Возвращает флаг формата символов Юникода для элемента управления. Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса жетуникодеформат.
ms.assetid: 2b36265a-023c-4083-a755-769461f3804b
keywords:
- Элементы управления Windows для HDM_GETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- HDM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce625cc9d4c0ede0c4ce9b54dc852025b22d4870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135958"
---
# <a name="hdm_getunicodeformat-message"></a>\_Сообщение ЖЕТУНИКОДЕФОРМАТ HDM

Возвращает флаг формата символов Юникода для элемента управления. Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ жетуникодеформат**](/windows/desktop/api/Commctrl/nf-commctrl-header_getunicodeformat) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает флаг формата Юникода для элемента управления. Если это значение не равно нулю, то элемент управления использует символы Юникода. Если это значение равно нулю, то элемент управления использует символы ANSI.

## <a name="remarks"></a>Комментарии

Обсуждение этого сообщения см. в примечаниях по [**CCM \_ жетуникодеформат**](ccm-getunicodeformat.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_СЕТУНИКОДЕФОРМАТ HDM**](hdm-setunicodeformat.md)
</dt> </dl>

 

 





