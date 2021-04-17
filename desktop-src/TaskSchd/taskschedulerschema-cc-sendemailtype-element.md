---
title: Элемент CC (Сендемаилтипе)
description: Содержит адреса электронной почты, используемые в строке CC сообщения электронной почты.
ms.assetid: cb8bc5b3-c352-43e3-bf28-d2090a519c7f
keywords:
- планировщик задач элемента CC
topic_type:
- apiref
api_name:
- Cc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bc49f2d7eebc2fbb1b5818fee2efa0e54f579a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491685"
---
# <a name="cc-sendemailtype-element"></a>Элемент CC (Сендемаилтипе)

Содержит адреса электронной почты, используемые в строке CC сообщения электронной почты.

``` syntax
<xs:element name="Cc"
    type="string"
 />
```

Элемент **CC** определяется сложным типом [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                              | Унаследован от                                                           | Описание                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) | Представляет действие, которое отправляет сообщение электронной почты.<br/> |



## <a name="remarks"></a>Комментарии

Сведения о разработке C++ см. в разделе [**свойство CC объекта иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc).

Сведения о разработке сценариев см. в разделе [**EmailAction.CC**](emailaction-cc.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





