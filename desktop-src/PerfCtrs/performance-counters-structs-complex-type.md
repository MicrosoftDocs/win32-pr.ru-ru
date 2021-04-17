---
description: Определяет список структур, содержащих значения счетчиков.
ms.assetid: 6f6b33ed-6440-456c-8379-61a37798c95f
title: Составной тип структур
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c36de698d1e0eb136f17034e0740851fc751d157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663175"
---
# <a name="structs-complex-type"></a><span data-ttu-id="445db-103">Составной тип структур</span><span class="sxs-lookup"><span data-stu-id="445db-103">structs Complex Type</span></span>

<span data-ttu-id="445db-104">Определяет список структур, содержащих значения счетчиков.</span><span class="sxs-lookup"><span data-stu-id="445db-104">Defines a list of structures that contain counter values.</span></span>

``` syntax
<xs:complexType name="structs">
    <xs:choice
        minOccurs="1"
        maxOccurs="unbounded"
    >
        <xs:element name="struct"
            type="man:struct"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="445db-105">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="445db-105">Child elements</span></span>



| <span data-ttu-id="445db-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="445db-106">Element</span></span>    | <span data-ttu-id="445db-107">Тип</span><span class="sxs-lookup"><span data-stu-id="445db-107">Type</span></span>                                                           | <span data-ttu-id="445db-108">Описание</span><span class="sxs-lookup"><span data-stu-id="445db-108">Description</span></span>                                                      |
|------------|----------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="445db-109">**struct**</span><span class="sxs-lookup"><span data-stu-id="445db-109">**struct**</span></span> | [<span data-ttu-id="445db-110">**Man: структура**</span><span class="sxs-lookup"><span data-stu-id="445db-110">**man:struct**</span></span>](performance-counters-struct-complex-type.md) | <span data-ttu-id="445db-111">Имя структуры, содержащей значения счетчика.</span><span class="sxs-lookup"><span data-stu-id="445db-111">The name of a structure that contains counter values.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="445db-112">Требования</span><span class="sxs-lookup"><span data-stu-id="445db-112">Requirements</span></span>



| <span data-ttu-id="445db-113">Требование</span><span class="sxs-lookup"><span data-stu-id="445db-113">Requirement</span></span> | <span data-ttu-id="445db-114">Значение</span><span class="sxs-lookup"><span data-stu-id="445db-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="445db-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="445db-115">Minimum supported client</span></span><br/> | <span data-ttu-id="445db-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="445db-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="445db-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="445db-117">Minimum supported server</span></span><br/> | <span data-ttu-id="445db-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="445db-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




