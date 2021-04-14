---
title: Евентрекордид (Системпропертиестипе), элемент
description: Номер записи, назначенный событию при регистрации.
ms.assetid: d042de4d-e532-432e-bba2-1876a26860a4
keywords:
- Журнал событий элемента Евентрекордид
topic_type:
- apiref
api_name:
- EventRecordID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5cb937d075bc0ff5fc1cf8bf1335d1274aee4fba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414884"
---
# <a name="eventrecordid-systempropertiestype-element"></a><span data-ttu-id="7dbe7-104">Евентрекордид (Системпропертиестипе), элемент</span><span class="sxs-lookup"><span data-stu-id="7dbe7-104">EventRecordID (SystemPropertiesType) Element</span></span>

<span data-ttu-id="7dbe7-105">Номер записи, назначенный событию при регистрации.</span><span class="sxs-lookup"><span data-stu-id="7dbe7-105">The record number assigned to the event when it was logged.</span></span>

``` syntax
<xs:element name="EventRecordID">
    <xs:complexType>
        <xs:simpleContent>
            <xs:extension
                base="unsignedLong"
             />
        </xs:simpleContent>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="7dbe7-106">Элемент **евентрекордид** определяется сложным типом [**системпропертиестипе**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7dbe7-106">The **EventRecordID** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dbe7-107">Требования</span><span class="sxs-lookup"><span data-stu-id="7dbe7-107">Requirements</span></span>



| <span data-ttu-id="7dbe7-108">Требование</span><span class="sxs-lookup"><span data-stu-id="7dbe7-108">Requirement</span></span> | <span data-ttu-id="7dbe7-109">Значение</span><span class="sxs-lookup"><span data-stu-id="7dbe7-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7dbe7-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7dbe7-110">Minimum supported client</span></span><br/> | <span data-ttu-id="7dbe7-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7dbe7-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7dbe7-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7dbe7-112">Minimum supported server</span></span><br/> | <span data-ttu-id="7dbe7-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7dbe7-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





