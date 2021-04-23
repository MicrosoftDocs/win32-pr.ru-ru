---
description: Определяет структуру, содержащую один или несколько значений счетчиков.
ms.assetid: 3085d490-4ac1-491c-bce0-8af46b16fab9
title: Сложный тип struct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc59103a1a98b0baf1559ead159221ea42288936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663178"
---
# <a name="struct-complex-type"></a><span data-ttu-id="b2f5f-103">Сложный тип struct</span><span class="sxs-lookup"><span data-stu-id="b2f5f-103">struct Complex Type</span></span>

<span data-ttu-id="b2f5f-104">Определяет структуру, содержащую один или несколько значений счетчиков.</span><span class="sxs-lookup"><span data-stu-id="b2f5f-104">Defines a structure that contains one or more counter values.</span></span>

``` syntax
<xs:complexType name="struct">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="man:CSymbolType"
                use="required"
             />
            <xs:attribute name="type"
                type="man:CSymbolType"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="b2f5f-105">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b2f5f-105">Attributes</span></span>



| <span data-ttu-id="b2f5f-106">Имя</span><span class="sxs-lookup"><span data-stu-id="b2f5f-106">Name</span></span> | <span data-ttu-id="b2f5f-107">Тип</span><span class="sxs-lookup"><span data-stu-id="b2f5f-107">Type</span></span>                                                                    | <span data-ttu-id="b2f5f-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b2f5f-108">Description</span></span>                                                                                                                                      |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2f5f-109">name</span><span class="sxs-lookup"><span data-stu-id="b2f5f-109">name</span></span> | [<span data-ttu-id="b2f5f-110">**мужчина: Ксимболтипе**</span><span class="sxs-lookup"><span data-stu-id="b2f5f-110">**man:CSymbolType**</span></span>](performance-counters-csymboltype-simple-type.md) | <span data-ttu-id="b2f5f-111">Имя структуры.</span><span class="sxs-lookup"><span data-stu-id="b2f5f-111">The name of the structure.</span></span><br/>                                                                                                            |
| <span data-ttu-id="b2f5f-112">тип</span><span class="sxs-lookup"><span data-stu-id="b2f5f-112">type</span></span> | [<span data-ttu-id="b2f5f-113">**мужчина: Ксимболтипе**</span><span class="sxs-lookup"><span data-stu-id="b2f5f-113">**man:CSymbolType**</span></span>](performance-counters-csymboltype-simple-type.md) | <span data-ttu-id="b2f5f-114">Символьное имя, идентифицирующее структуру.</span><span class="sxs-lookup"><span data-stu-id="b2f5f-114">A symbolic name that identifies the structure.</span></span> <span data-ttu-id="b2f5f-115">Средство [КТРПП](ctrpp.md) создает переменную структуры с таким именем, которую можно использовать.</span><span class="sxs-lookup"><span data-stu-id="b2f5f-115">The [CTRPP](ctrpp.md) tool creates a struct variable with this name that you can use.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b2f5f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b2f5f-116">Requirements</span></span>



| <span data-ttu-id="b2f5f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b2f5f-117">Requirement</span></span> | <span data-ttu-id="b2f5f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b2f5f-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b2f5f-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b2f5f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b2f5f-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b2f5f-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b2f5f-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b2f5f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b2f5f-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b2f5f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




