---
title: Элемент title (Шовмессажетипе)
description: Содержит заголовок окна сообщения.
ms.assetid: 089d2043-41ed-4050-b794-af24ab7ac8b9
keywords:
- Элемент title планировщик задач
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca5baa7135579ff673ba9b01a672a126924d1d49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135343"
---
# <a name="title-showmessagetype-element"></a>Элемент title (Шовмессажетипе)

Содержит заголовок окна сообщения.

``` syntax
<xs:element name="Title"
    type="nonEmptyString"
 />
```

Элемент **Title** определяется сложным типом [**шовмессажетипе**](taskschedulerschema-showmessagetype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                  | Унаследован от                                                               | Описание                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [**ShowMessage (actionGroup)**](taskschedulerschema-showmessage-actiongroup-element.md) | [**шовмессажетипе**](taskschedulerschema-showmessagetype-complextype.md) | Представляет действие, показывающее окно сообщения.<br/> |



## <a name="remarks"></a>Комментарии

Сведения о разработке на языке C++ см. в разделе [**свойство Title объекта ишовмессажеактион**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title).

Сведения о разработке сценариев см. в разделе [**шовмессажеактион. Title**](showmessageaction-title.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





