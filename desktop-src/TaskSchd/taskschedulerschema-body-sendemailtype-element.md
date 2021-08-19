---
title: Элемент Body (Сендемаилтипе)
description: Содержит текст в тексте сообщения электронной почты.
ms.assetid: fac6ddd5-6f73-427b-b213-ab946512c87a
keywords:
- Элемент Body планировщик задач
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a924062b3a382bc8362bdfa45e1477b4e841222bdd1f5ac70fbb8adbc9b070b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118857967"
---
# <a name="body-sendemailtype-element"></a>Элемент Body (Сендемаилтипе)

Содержит текст в тексте сообщения электронной почты.

``` syntax
<xs:element name="Body"
    type="string"
 />
```

Элемент **Body** определяется сложным типом [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                              | Унаследован от                                                           | Описание                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) | Представляет действие, которое отправляет сообщение электронной почты.<br/> |



## <a name="remarks"></a>Remarks

Сведения о разработке на языке C++ см. в разделе [**свойство Body объекта иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body).

Сведения о разработке сценариев см. в разделе [**емаилактион. Body**](emailaction-body.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





