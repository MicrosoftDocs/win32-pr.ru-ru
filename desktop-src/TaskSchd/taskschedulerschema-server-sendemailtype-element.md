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
ms.openlocfilehash: d6052ebb5e648c040c321a311a6ba18313244ab20340d5a7f6c4185e3d35f5df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002252"
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



## <a name="remarks"></a>Remarks

Сведения о разработке на языке C++ см. в разделе [**свойство сервера иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server).

Сведения о разработке сценариев см. в разделе [**емаилактион. Server**](emailaction-server.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





