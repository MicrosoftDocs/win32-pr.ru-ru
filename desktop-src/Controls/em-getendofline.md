---
title: Сообщение EM_GETENDOFLINE (Коммктрл. h)
description: Получает символ конца строки, используемый при вставке LineBreak. Отправьте это сообщение явным образом или с помощью \_ макроса Edit жетендофлине.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- Элементы управления Windows для EM_GETENDOFLINE сообщений
topic_type:
- apiref
api_name:
- EM_GETENDOFLINE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 98d537d2ea4239ab3f511666aeba46be93a2b881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489465"
---
# <a name="em_getendofline-message"></a>\_Сообщение ЖЕТЕНДОФЛИНЕ EM

Извлекает символ конца строки для элемента управления "поле ввода". Отправьте это сообщение явным образом или с помощью макроса [**Edit \_ жетендофлине**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает символ конца строки, используемый элементом управления "поле ввода". Это может быть одно из следующих значений.

| Значение                                                                                                                                                   | Значение                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <dt>**EC \_ ендофлине \_ CRLF**</dt> </dl> | Символ конца строки, используемый для New линебреакс, — возврат каретки, за которым следует перевод строки (CRLF).<br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <dt>**EC \_ ендофлине \_ CR**</dt> </dl>       | Символ конца строки, используемый для New линебреакс, — возврат каретки (CR).<br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <dt>**EC \_ ендофлине \_ LF**</dt> </dl>       | Символ конца строки, используемый для New линебреакс, — перевод строки (LF).<br/>                               |

## <a name="remarks"></a>Комментарии

Если в качестве символа конца строки задано **EC \_ ендофлине \_ Детектфромконтент** с помощью [**Edit \_ сетендофлине**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline), это сообщение вернет обнаруженный символ конца строки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1809\]<br/>                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2019\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EM \_ сетендофлине*](em-setendofline.md)
</dt> </dl>
 

 





