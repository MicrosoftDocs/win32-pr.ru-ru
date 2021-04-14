---
title: Сервер (Сендемаилтипе), элемент
description: Содержит почтовый сервер, используемый для отправки сообщения электронной почты.
ms.assetid: 4c6084d1-70c5-4d8b-8fcb-ab4cd8aab441
keywords:
- Серверный элемент планировщик задач
topic_type:
- apiref
api_name:
- Server
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5fc57ddf5deee52ff9b118a8267eec4069108030
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414972"
---
# <a name="server-sendemailtype-element"></a>Сервер (Сендемаилтипе), элемент

Содержит почтовый сервер, используемый для отправки сообщения электронной почты.

``` syntax
<xs:element name="Server"
    type="nonEmptyString"
 />
```

Элемент **Server** определяется сложным типом [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                              | Унаследован от                                                           | Описание                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) | Представляет действие, которое отправляет сообщение электронной почты.<br/> |



## <a name="remarks"></a>Комментарии

Сведения о разработке на языке C++ см. в разделе [**свойство сервера иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server).

Сведения о разработке сценариев см. в разделе [**емаилактион. Server**](emailaction-server.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





