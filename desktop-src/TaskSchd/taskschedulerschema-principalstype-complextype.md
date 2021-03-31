---
title: Сложный тип ПринЦипалстипе
description: Определяет дочерний элемент для Principal-элемента.
ms.assetid: a501534b-eb0f-480f-a2c9-d2015262a9a7
keywords:
- планировщик задач сложного типа ПринЦипалстипе
topic_type:
- apiref
api_name:
- principalsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56cd26a4dff31ce86b218e5a4a2662d678327625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988292"
---
# <a name="principalstype-complex-type"></a><span data-ttu-id="5ef1b-104">Сложный тип ПринЦипалстипе</span><span class="sxs-lookup"><span data-stu-id="5ef1b-104">principalsType Complex Type</span></span>

<span data-ttu-id="5ef1b-105">Определяет дочерний элемент для [**Principal**](taskschedulerschema-principals-tasktype-element.md) -элемента.</span><span class="sxs-lookup"><span data-stu-id="5ef1b-105">Defines the child element for the [**Principals**](taskschedulerschema-principals-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="principalsType">
    <xs:sequence>
        <xs:element name="Principal"
            type="principalType"
            maxOccurs="1"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="5ef1b-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5ef1b-106">Child elements</span></span>



| <span data-ttu-id="5ef1b-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="5ef1b-107">Element</span></span>                                                                  | <span data-ttu-id="5ef1b-108">Тип</span><span class="sxs-lookup"><span data-stu-id="5ef1b-108">Type</span></span>                                                                   | <span data-ttu-id="5ef1b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5ef1b-109">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="5ef1b-110">**Основного**</span><span class="sxs-lookup"><span data-stu-id="5ef1b-110">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="5ef1b-111">**principalType**</span><span class="sxs-lookup"><span data-stu-id="5ef1b-111">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="5ef1b-112">Указывает учетные данные безопасности для участника.</span><span class="sxs-lookup"><span data-stu-id="5ef1b-112">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5ef1b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5ef1b-113">Requirements</span></span>



| <span data-ttu-id="5ef1b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5ef1b-114">Requirement</span></span> | <span data-ttu-id="5ef1b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5ef1b-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5ef1b-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ef1b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5ef1b-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5ef1b-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5ef1b-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ef1b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5ef1b-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5ef1b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





