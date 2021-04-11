---
title: ReplyTo (Сендемаилтипе), элемент
description: Содержит адреса электронной почты, на которые дан ответ в сообщении электронной почты.
ms.assetid: c09b72f6-de2c-41dc-942c-d6184863e33c
keywords:
- Элемент ReplyTo планировщик задач
topic_type:
- apiref
api_name:
- ReplyTo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02055539d4557a60f182981f0d9cd7d3e1a63ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137683"
---
# <a name="replyto-sendemailtype-element"></a>ReplyTo (Сендемаилтипе), элемент

Содержит адреса электронной почты, на которые дан ответ в сообщении электронной почты.

``` syntax
<xs:element name="ReplyTo"
    type="string"
 />
```

Элемент **ReplyTo** определяется сложным типом [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                              | Унаследован от                                                           | Описание                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) | Представляет действие, которое отправляет сообщение электронной почты.<br/> |



## <a name="remarks"></a>Комментарии

Сведения о разработке с + + см. в разделе [**Свойство ReplyTo объекта иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto).

Сведения о разработке сценариев см. в разделе [**емаилактион. ReplyTo**](emailaction-replyto.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





