---
title: Элемент subject (Сендемаилтипе)
description: Содержит тему сообщения электронной почты.
ms.assetid: 2ccaa983-4dca-4e45-ba8d-2a93e23f7e8c
keywords:
- Элемент subject планировщик задач
topic_type:
- apiref
api_name:
- Subject
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 15bf3c84befd9dd8f4c9c4a544fc920b7066184c6bf367c404bb14f22f573b92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611192"
---
# <a name="subject-sendemailtype-element"></a>Элемент subject (Сендемаилтипе)

Содержит тему сообщения электронной почты.

``` syntax
<xs:element name="Subject"
    type="string"
 />
```

Элемент **subject** определяется сложным типом [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                              | Унаследован от                                                           | Описание                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) | Представляет действие, которое отправляет сообщение электронной почты.<br/> |



## <a name="remarks"></a>Remarks

Сведения о разработке на языке C++ см. в разделе [**свойство Subject объекта иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject).

Сведения о разработке сценариев см. в разделе [**емаилактион. subject**](emailaction-subject.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





