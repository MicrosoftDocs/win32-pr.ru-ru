---
title: Сложный тип Намедвалуе
description: Определяет имя, связанное со значением в паре "имя-значение".
ms.assetid: 5e3ce01a-9be6-4f12-be02-42065aba46cd
keywords:
- планировщик задач сложного типа Намедвалуе
topic_type:
- apiref
api_name:
- namedValue
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39d6990194350dcc032d42838f30bdd7339b0d38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988951"
---
# <a name="namedvalue-complex-type"></a><span data-ttu-id="2d62b-104">Сложный тип Намедвалуе</span><span class="sxs-lookup"><span data-stu-id="2d62b-104">namedValue Complex Type</span></span>

<span data-ttu-id="2d62b-105">Определяет имя, связанное со значением в паре "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="2d62b-105">Defines a name that is associated with a value in a name-value pair.</span></span>

``` syntax
<xs:complexType name="namedValue">
    <xs:simpleContent>
        <xs:extension
            base="nonEmptyString"
        >
            <xs:attribute name="name"
                type="nonEmptyString"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="2d62b-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2d62b-106">Attributes</span></span>



| <span data-ttu-id="2d62b-107">Имя</span><span class="sxs-lookup"><span data-stu-id="2d62b-107">Name</span></span> | <span data-ttu-id="2d62b-108">Тип</span><span class="sxs-lookup"><span data-stu-id="2d62b-108">Type</span></span>                                                                    | <span data-ttu-id="2d62b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="2d62b-109">Description</span></span>                                                                          |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2d62b-110">name</span><span class="sxs-lookup"><span data-stu-id="2d62b-110">name</span></span> | [<span data-ttu-id="2d62b-111">**нонемптистринг**</span><span class="sxs-lookup"><span data-stu-id="2d62b-111">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="2d62b-112">Указывает имя, связанное со значением в паре «имя-значение».</span><span class="sxs-lookup"><span data-stu-id="2d62b-112">Specifies the name that is associated with a value in a name-value pair.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="2d62b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="2d62b-113">Requirements</span></span>



| <span data-ttu-id="2d62b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="2d62b-114">Requirement</span></span> | <span data-ttu-id="2d62b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2d62b-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2d62b-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d62b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2d62b-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2d62b-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2d62b-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d62b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2d62b-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2d62b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





