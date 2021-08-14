---
title: Элемент вложений (Сендемаилтипе)
description: Содержит список вложений в сообщении электронной почты.
ms.assetid: 5ae22481-af70-42eb-a964-e63d800be17d
keywords:
- Элемент вложений планировщик задач
topic_type:
- apiref
api_name:
- Attachments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8aa87679c6d6db725c26deee817fe04acacca85e39d3a8f75c04cba9680ea846
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132069"
---
# <a name="attachments-sendemailtype-element"></a>Элемент вложений (Сендемаилтипе)

Содержит список вложений в сообщении электронной почты.

``` syntax
<xs:element name="Attachments"
    type="attachmentsType"
 />
```

Элемент **вложениям** определяется сложным типом [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                              | Унаследован от                                                           | Описание                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) | Представляет действие, которое отправляет сообщение электронной почты.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                          | Тип                                                                    | Описание                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**Файл**](taskschedulerschema-file-attachmentstype-element.md) | [**нонемптистринг**](taskschedulerschema-nonemptystring-simpletype.md) | Указывает путь к файлу, который отправляется в виде вложения в сообщение электронной почты.<br/> |



## <a name="remarks"></a>Remarks

Сведения о разработке на языке C++ см. в разделе [**свойство вложений иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).

Сведения о разработке сценариев см. в разделе [**емаилактион. вложениям**](emailaction-attachments.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





