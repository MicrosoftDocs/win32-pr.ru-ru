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
ms.openlocfilehash: 31186fbcc833219b6523f1fdeb986532984eb7b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691778"
---
# <a name="userdatatype-complex-type"></a><span data-ttu-id="e6cc2-104">Сложный тип Усердататипе</span><span class="sxs-lookup"><span data-stu-id="e6cc2-104">UserDataType Complex Type</span></span>

<span data-ttu-id="e6cc2-105">Определяет фрагмент XML, указывающий макет данных события.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-105">Defines an XML fragment that specifies the layout of the event data.</span></span>

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

## <a name="requirements"></a><span data-ttu-id="e6cc2-106">Требования</span><span class="sxs-lookup"><span data-stu-id="e6cc2-106">Requirements</span></span>



| <span data-ttu-id="e6cc2-107">Требование</span><span class="sxs-lookup"><span data-stu-id="e6cc2-107">Requirement</span></span> | <span data-ttu-id="e6cc2-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e6cc2-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e6cc2-109">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6cc2-109">Minimum supported client</span></span><br/> | <span data-ttu-id="e6cc2-110">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6cc2-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e6cc2-111">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6cc2-111">Minimum supported server</span></span><br/> | <span data-ttu-id="e6cc2-112">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e6cc2-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





