---
title: Сообщение EM_GETENDOFLINE (Коммктрл. h)
description: Получает символ конца строки, используемый при вставке LineBreak. Отправьте это сообщение явным образом или с помощью \_ макроса Edit жетендофлине.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- элементы управления Windows сообщений EM_GETENDOFLINE
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
ms.openlocfilehash: 64ddb55ce592b71c7abaa8c35b1bf14a004b324586094f27a3b418a67e5b24e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019692"
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

## <a name="remarks"></a>Remarks

Если в качестве символа конца строки задано **EC \_ ендофлине \_ Детектфромконтент** с помощью [**Edit \_ сетендофлине**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline), это сообщение вернет обнаруженный символ конца строки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, версия 1809 \[ только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2019\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EM \_ сетендофлине*](em-setendofline.md)
</dt> </dl>
 

 





