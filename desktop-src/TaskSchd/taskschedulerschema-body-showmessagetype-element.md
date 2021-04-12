---
title: Элемент Body (Шовмессажетипе)
description: Содержит текст, отображаемый в тексте окна сообщения.
ms.assetid: 69ea872a-7ca1-4464-9380-b35f74c9cb8e
keywords:
- Элемент Body планировщик задач
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3486601153f8e9dd7dac14f83800dae00a79a9f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491361"
---
# <a name="body-showmessagetype-element"></a>Элемент Body (Шовмессажетипе)

Содержит текст, отображаемый в тексте окна сообщения.

``` syntax
<xs:element name="Body"
    type="nonEmptyString"
 />
```

Элемент **Body** определяется сложным типом [**шовмессажетипе**](taskschedulerschema-showmessagetype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                  | Унаследован от                                                               | Описание                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [**ShowMessage (actionGroup)**](taskschedulerschema-showmessage-actiongroup-element.md) | [**шовмессажетипе**](taskschedulerschema-showmessagetype-complextype.md) | Представляет действие, показывающее окно сообщения.<br/> |



## <a name="remarks"></a>Комментарии

Сведения о разработке на языке C++ см. в разделе [**свойство MessageBody объекта ишовмессажеактион**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody).

Сведения о разработке сценариев см. в разделе [**шовмессажеактион. MessageBody**](showmessageaction-messagebody.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





