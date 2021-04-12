---
title: Элемент File (Аттачментстипе)
description: Содержит путь к файлу, отправленному в виде вложения в сообщение электронной почты.
ms.assetid: a53f591b-ac59-43b4-8cc2-661e76d307cc
keywords:
- планировщик задач элемента File
topic_type:
- apiref
api_name:
- File
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed07d4b31f9054f6caefcff0585d9683faa90c7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415237"
---
# <a name="file-attachmentstype-element"></a>Элемент File (Аттачментстипе)

Содержит путь к файлу, отправленному в виде вложения в сообщение электронной почты.

``` syntax
<xs:element name="File"
    type="nonEmptyString"
 />
```

Элемент **File** определяется сложным типом [**аттачментстипе**](taskschedulerschema-attachmentstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                      | Унаследован от                                                               | Описание                                                     |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**Вложения (Сендемаилтипе)**](taskschedulerschema-attachments-sendemailtype-element.md) | [**аттачментстипе**](taskschedulerschema-attachmentstype-complextype.md) | Содержит список вложений в сообщении электронной почты.<br/> |



## <a name="remarks"></a>Комментарии

Сведения о разработке на языке C++ см. в разделе [**свойство вложений иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).

Сведения о разработке сценариев см. в разделе [**емаилактион. вложениям**](emailaction-attachments.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





