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
ms.openlocfilehash: c6b1fbacd450c05b8ff71521dacfa6e95c7efc70fc7d8909ca66f3390bf22295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010874"
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



## <a name="remarks"></a>Remarks

Сведения о разработке на языке C++ см. в разделе [**свойство MessageBody объекта ишовмессажеактион**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody).

Сведения о разработке сценариев см. в разделе [**шовмессажеактион. MessageBody**](showmessageaction-messagebody.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





