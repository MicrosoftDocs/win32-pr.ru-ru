---
description: Указывает имя и тип беспроводной сети.
ms.assetid: 839afae0-b8e1-489f-8811-19a82c173627
title: Сложный тип Нетворкитемтипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkItemType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5db7c5fc4d9b5227d9cd29c5e2dfc69da6fad139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674216"
---
# <a name="networkitemtype-complex-type"></a><span data-ttu-id="ac385-103">Сложный тип Нетворкитемтипе</span><span class="sxs-lookup"><span data-stu-id="ac385-103">networkItemType Complex Type</span></span>

<span data-ttu-id="ac385-104">Сложный тип Нетворкитемтипе указывает имя и тип беспроводной сети.</span><span class="sxs-lookup"><span data-stu-id="ac385-104">The networkItemType complex type specifies the name and type of a wireless network.</span></span>

``` syntax
<xs:complexType name="networkItemType">
    <xs:sequence>
        <xs:element name="networkName"
            type="networkNameType"
         />
        <xs:element name="networkType"
            type="networkTypeType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="ac385-105">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ac385-105">Child elements</span></span>



| <span data-ttu-id="ac385-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="ac385-106">Element</span></span>                                                                      | <span data-ttu-id="ac385-107">Тип</span><span class="sxs-lookup"><span data-stu-id="ac385-107">Type</span></span>                                                                    | <span data-ttu-id="ac385-108">Описание</span><span class="sxs-lookup"><span data-stu-id="ac385-108">Description</span></span>                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="ac385-109">**networkName**</span><span class="sxs-lookup"><span data-stu-id="ac385-109">**networkName**</span></span>](wlan-policyschema-networkname-networkitemtype-element.md) | [<span data-ttu-id="ac385-110">**нетворкнаметипе**</span><span class="sxs-lookup"><span data-stu-id="ac385-110">**networkNameType**</span></span>](wlan-policyschema-networknametype-simpletype.md) | <span data-ttu-id="ac385-111">Идентификатор набора служб (SSID) сети.</span><span class="sxs-lookup"><span data-stu-id="ac385-111">The service set identifier (SSID) of the network.</span></span> <br/> |
| [<span data-ttu-id="ac385-112">**нетворктипе**</span><span class="sxs-lookup"><span data-stu-id="ac385-112">**networkType**</span></span>](wlan-policyschema-networktype-networkitemtype-element.md) | [<span data-ttu-id="ac385-113">**нетворктипетипе**</span><span class="sxs-lookup"><span data-stu-id="ac385-113">**networkTypeType**</span></span>](wlan-policyschema-networktypetype-simpletype.md) | <span data-ttu-id="ac385-114">Тип сети.</span><span class="sxs-lookup"><span data-stu-id="ac385-114">The network type.</span></span> <br/>                                 |



## <a name="requirements"></a><span data-ttu-id="ac385-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ac385-115">Requirements</span></span>



| <span data-ttu-id="ac385-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ac385-116">Requirement</span></span> | <span data-ttu-id="ac385-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ac385-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ac385-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac385-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ac385-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ac385-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ac385-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac385-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ac385-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ac385-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




