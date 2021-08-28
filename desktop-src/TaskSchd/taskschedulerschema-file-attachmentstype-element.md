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
ms.openlocfilehash: 793b23bc6b9d75ac809c42063fa9c300542705b718cd22253f6f2d3a1a76caa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125854"
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



## <a name="remarks"></a>Remarks

Сведения о разработке на языке C++ см. в разделе [**свойство вложений иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).

Сведения о разработке сценариев см. в разделе [**емаилактион. вложениям**](emailaction-attachments.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





