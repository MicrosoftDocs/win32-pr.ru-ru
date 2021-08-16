---
title: Элемент BCC (Сендемаилтипе)
description: Содержит адреса электронной почты, используемые в строке СК сообщения электронной почты.
ms.assetid: c80407d0-3b3f-4efe-91de-7a3a7abc996f
keywords:
- Элемент скрытой планировщик задач
topic_type:
- apiref
api_name:
- Bcc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1409d50a0317758534724b9e2c3a9796c4dd0cb40e666f58fc65ca0771da9762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659044"
---
# <a name="bcc-sendemailtype-element"></a>Элемент BCC (Сендемаилтипе)

Содержит адреса электронной почты, используемые в строке СК сообщения электронной почты.

``` syntax
<xs:element name="Bcc"
    type="string"
 />
```

Элемент **BCC** определяется сложным типом [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                              | Унаследован от                                                           | Описание                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) | Представляет действие, которое отправляет сообщение электронной почты.<br/> |



## <a name="remarks"></a>Remarks

Сведения о разработке на языке C++ см. в разделе [**свойство BCC объекта иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc).

Сведения о разработке сценариев см. в разделе [**емаилактион. BCC**](emailaction-bcc.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





