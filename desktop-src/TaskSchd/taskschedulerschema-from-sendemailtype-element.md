---
title: From (Сендемаилтипе), элемент
description: Содержит адрес электронной почты отправителя электронной почты.
ms.assetid: b80733de-e050-4026-a2fe-f63833ec2660
keywords:
- Из планировщик задач элемента
topic_type:
- apiref
api_name:
- From
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f50704212fe6a4fec7ce0fc21bacd7ea33e402c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071410"
---
# <a name="from-sendemailtype-element"></a>From (Сендемаилтипе), элемент

Содержит адрес электронной почты отправителя электронной почты.

``` syntax
<xs:element name="From"
    type="string"
 />
```

Элемент **from** определяется сложным типом [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                              | Унаследован от                                                           | Описание                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) | Представляет действие, которое отправляет сообщение электронной почты.<br/> |



## <a name="remarks"></a>Комментарии

Для разработки на C++ см. [**свойство From объекта иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from).

Сведения о разработке сценариев см. [**в разделе емаилактион. from**](emailaction-from.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





