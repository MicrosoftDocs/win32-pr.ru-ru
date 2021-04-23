---
title: Сложный тип Намедвалуес
description: Определяет пару "имя-значение", в которой имя связано со значением.
ms.assetid: 07c512fd-3eab-4238-8d75-83827a958a1e
keywords:
- планировщик задач сложного типа Намедвалуес
topic_type:
- apiref
api_name:
- namedValues
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f18c9fddab58f33ffc724a3e8df7bd65583cb88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802771"
---
# <a name="namedvalues-complex-type"></a><span data-ttu-id="df45e-104">Сложный тип Намедвалуес</span><span class="sxs-lookup"><span data-stu-id="df45e-104">namedValues Complex Type</span></span>

<span data-ttu-id="df45e-105">Определяет пару "имя-значение", в которой имя связано со значением.</span><span class="sxs-lookup"><span data-stu-id="df45e-105">Defines a name-value pair in which the name is associated with the value.</span></span>

``` syntax
<xs:complexType name="namedValues">
    <xs:sequence>
        <xs:element name="Value"
            type="namedValue"
            minOccurs="1"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="df45e-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="df45e-106">Child elements</span></span>



| <span data-ttu-id="df45e-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="df45e-107">Element</span></span>                                                        | <span data-ttu-id="df45e-108">Тип</span><span class="sxs-lookup"><span data-stu-id="df45e-108">Type</span></span>                                                | <span data-ttu-id="df45e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="df45e-109">Description</span></span>                                                                         |
|----------------------------------------------------------------|-----------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="df45e-110">**Значение**</span><span class="sxs-lookup"><span data-stu-id="df45e-110">**Value**</span></span>](taskschedulerschema-value-namedvalues-element.md) | [<span data-ttu-id="df45e-111">**намедвалуе**</span><span class="sxs-lookup"><span data-stu-id="df45e-111">**namedValue**</span></span>](schema-namedvalue-complextype.md) | <span data-ttu-id="df45e-112">Указывает значение, связанное с именем в паре «имя-значение».</span><span class="sxs-lookup"><span data-stu-id="df45e-112">Specifies the value that is associated with a name in a name-value pair.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="df45e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="df45e-113">Requirements</span></span>



| <span data-ttu-id="df45e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="df45e-114">Requirement</span></span> | <span data-ttu-id="df45e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="df45e-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="df45e-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df45e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="df45e-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="df45e-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="df45e-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df45e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="df45e-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="df45e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





