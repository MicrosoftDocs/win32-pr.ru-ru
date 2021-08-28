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
ms.openlocfilehash: 2af801385c74fa26221556b713faf8db915037ef4cf7439d71a2e2d4004193d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100034"
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



## <a name="remarks"></a>Remarks

Сведения о разработке на языке C++ см. в разделе [**свойство хеадерфиелдс объекта иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).

Сведения о разработке сценариев см. в разделе [**емаилактион. хеадерфиелдс**](emailaction-headerfields.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





