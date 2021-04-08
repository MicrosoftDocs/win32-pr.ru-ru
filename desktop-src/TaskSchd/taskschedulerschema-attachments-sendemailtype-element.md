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
ms.openlocfilehash: 67eed8f82f0caa27f44070bd109d4fa4560472eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803227"
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



## <a name="remarks"></a>Комментарии

Сведения о разработке на языке C++ см. в разделе [**свойство вложений иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).

Сведения о разработке сценариев см. в разделе [**емаилактион. вложениям**](emailaction-attachments.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





