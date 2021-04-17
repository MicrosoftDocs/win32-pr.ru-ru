---
title: Сообщение HDM_SETUNICODEFORMAT (Коммктрл. h)
description: Задает флаг формата символов Юникода для элемента управления.
ms.assetid: 18161fe5-c779-4be0-9e7a-1b5948e42b80
keywords:
- Элементы управления Windows для HDM_SETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- HDM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3fe3497413b265510426fab4ef2e71666f46312
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490863"
---
# <a name="hdm_setunicodeformat-message"></a>\_Сообщение СЕТУНИКОДЕФОРМАТ HDM

Задает флаг формата символов Юникода для элемента управления. Это сообщение позволяет изменить кодировку, используемую элементом управления во время выполнения, вместо того, чтобы повторно создавать элемент управления. Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ сетуникодеформат**](/windows/desktop/api/Commctrl/nf-commctrl-header_setunicodeformat) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Кодировка, используемая элементом управления. Если это значение не равно нулю, элемент управления будет использовать символы Юникода. Если это значение равно нулю, элемент управления будет использовать символы ANSI.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает предыдущий флаг формата Юникода для элемента управления.

## <a name="remarks"></a>Комментарии

Обсуждение этого сообщения см. в примечаниях по [**CCM \_ сетуникодеформат**](ccm-setunicodeformat.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ЖЕТУНИКОДЕФОРМАТ HDM**](hdm-getunicodeformat.md)
</dt> </dl>

 

 





