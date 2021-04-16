---
title: To (Сендемаилтипе), элемент
description: Содержит адреса электронной почты, на которые будет отправлено электронное письмо.
ms.assetid: bf3aa878-967b-4ebd-9397-a2a499686a9f
keywords:
- В элемент планировщик задач
topic_type:
- apiref
api_name:
- To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9e0643220915ecb1c8f2cd1fe842e0dc3f21d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672527"
---
# <a name="to-sendemailtype-element"></a>To (Сендемаилтипе), элемент

Содержит адреса электронной почты, на которые будет отправлено электронное письмо.

``` syntax
<xs:element name="To"
    type="string"
 />
```

Элемент **to** определяется сложным типом [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                              | Унаследован от                                                           | Описание                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) | Представляет действие, которое отправляет сообщение электронной почты.<br/> |



## <a name="remarks"></a>Комментарии

Сведения о разработке на языке C++ см. [**в разделе свойство объекта иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to).

Сведения о разработке сценариев см. в разделе [**EmailAction.to**](emailaction-to.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





