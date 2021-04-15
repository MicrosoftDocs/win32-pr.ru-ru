---
title: Хеадерфиелдс (Сендемаилтипе), элемент
description: Задает поля заголовка и их значения, используемые в заголовке сообщения электронной почты.
ms.assetid: 6261f32e-3012-4ce7-b407-699374596333
keywords:
- планировщик задач элемента Хеадерфиелдс
topic_type:
- apiref
api_name:
- HeaderFields
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d108f1c31b8253046ccdbf09312df4f54c7335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534577"
---
# <a name="headerfields-sendemailtype-element"></a>Хеадерфиелдс (Сендемаилтипе), элемент

Задает поля заголовка и их значения, используемые в заголовке сообщения электронной почты.

``` syntax
<xs:element name="HeaderFields"
    type="headerFieldsType"
 />
```

Элемент **хеадерфиелдс** определяется сложным типом [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                              | Унаследован от                                                           | Описание                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) | Представляет действие, которое отправляет сообщение электронной почты.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                         | Тип                                                                       | Описание                                                    |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------|
| [**хеадерфиелд**](taskschedulerschema-headerfield-headerfieldstype-element.md) | [**хеадерфиелдтипе**](taskschedulerschema-headerfieldtype-complextype.md) | Содержит поле для заголовка в сообщении электронной почты. <br/> |



## <a name="remarks"></a>Комментарии

Сведения о разработке на языке C++ см. в разделе [**свойство хеадерфиелдс объекта иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).

Сведения о разработке сценариев см. в разделе [**емаилактион. хеадерфиелдс**](emailaction-headerfields.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





