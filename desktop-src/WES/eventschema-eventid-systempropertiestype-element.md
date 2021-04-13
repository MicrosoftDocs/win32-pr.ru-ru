---
title: Элемент EventID (Системпропертиестипе)
description: Идентификатор, используемый поставщиком для идентификации события.
ms.assetid: 2d5ac44b-4157-4b87-bd8f-e992e85dd0b1
keywords:
- Журнал событий элемента EventID
topic_type:
- apiref
api_name:
- EventID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ac1b2edd671f06d88c8c51b49c16f759fd05e087
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489489"
---
# <a name="eventid-systempropertiestype-element"></a><span data-ttu-id="6ce8e-104">Элемент EventID (Системпропертиестипе)</span><span class="sxs-lookup"><span data-stu-id="6ce8e-104">EventID (SystemPropertiesType) Element</span></span>

<span data-ttu-id="6ce8e-105">Идентификатор, используемый поставщиком для идентификации события.</span><span class="sxs-lookup"><span data-stu-id="6ce8e-105">The identifier that the provider used to identify the event.</span></span>

``` syntax
<xs:element name="EventID">
    <xs:complexType>
        <xs:simpleContent>
            <xs:extension
                base="unsignedInt"
             />
        </xs:simpleContent>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="6ce8e-106">Элемент **EventID** определяется сложным типом [**системпропертиестипе**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6ce8e-106">The **EventID** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ce8e-107">Требования</span><span class="sxs-lookup"><span data-stu-id="6ce8e-107">Requirements</span></span>



| <span data-ttu-id="6ce8e-108">Требование</span><span class="sxs-lookup"><span data-stu-id="6ce8e-108">Requirement</span></span> | <span data-ttu-id="6ce8e-109">Значение</span><span class="sxs-lookup"><span data-stu-id="6ce8e-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6ce8e-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ce8e-110">Minimum supported client</span></span><br/> | <span data-ttu-id="6ce8e-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6ce8e-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6ce8e-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ce8e-112">Minimum supported server</span></span><br/> | <span data-ttu-id="6ce8e-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6ce8e-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6ce8e-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ce8e-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="6ce8e-115">**Родительский элемент**</span><span class="sxs-lookup"><span data-stu-id="6ce8e-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="6ce8e-116">**Система (EventType)**</span><span class="sxs-lookup"><span data-stu-id="6ce8e-116">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





