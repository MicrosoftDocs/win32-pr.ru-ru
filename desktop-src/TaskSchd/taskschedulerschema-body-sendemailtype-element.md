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
ms.openlocfilehash: 4659f2ff03f69b6bba40d9cd16e9b68515cc8889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681948"
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



## <a name="remarks"></a>Комментарии

Сведения о разработке на языке C++ см. в разделе [**свойство Body объекта иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body).

Сведения о разработке сценариев см. в разделе [**емаилактион. Body**](emailaction-body.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





