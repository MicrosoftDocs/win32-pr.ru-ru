---
title: Сложный тип Усердататипе
description: Определяет фрагмент XML, указывающий макет данных события.
ms.assetid: 25147ace-cc36-43cc-ad85-6a1714f43dbe
keywords:
- Журнал событий сложных типов Усердататипе
topic_type:
- apiref
api_name:
- UserDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 747f2e30f6b2588cdfd6a9f0dd50187b73817996bd3725a571283a7929c91b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904194"
---
# <a name="userdatatype-complex-type"></a>Сложный тип Усердататипе

Определяет фрагмент XML, указывающий макет данных события.

``` syntax
<xs:complexType name="UserDataType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





