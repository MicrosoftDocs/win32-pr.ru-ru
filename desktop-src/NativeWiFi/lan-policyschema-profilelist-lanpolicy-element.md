---
description: Элемент Профилелист (Ланполици) — содержит список профилей, применяемых на уровне домена или компьютера.
ms.assetid: 4f010449-0c6b-4a01-8253-4f82cd628f0a
title: Профилелист (Ланполици), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- profileList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5d18ebc99f48bf72599afe750863d684b8158608
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090782"
---
# <a name="profilelist-lanpolicy-element"></a><span data-ttu-id="a98cd-103">Профилелист (Ланполици), элемент</span><span class="sxs-lookup"><span data-stu-id="a98cd-103">profileList (LANPolicy) Element</span></span>

<span data-ttu-id="a98cd-104">Элемент Профилелист (Ланполици) содержит список профилей, применяемых на уровне домена или компьютера.</span><span class="sxs-lookup"><span data-stu-id="a98cd-104">The profileList (LANPolicy) element contains a list of profiles to be applied at the domain or machine level.</span></span> <span data-ttu-id="a98cd-105">Профили должны быть основаны на [ \_ схеме профиля локальной сети](lan-profileschema-schema.md)с корневым элементом [**ланпрофиле**](lan-profileschema-lanprofile-element.md).</span><span class="sxs-lookup"><span data-stu-id="a98cd-105">Profiles must be based on the [LAN\_profile schema](lan-profileschema-schema.md), with a root element of [**LANProfile**](lan-profileschema-lanprofile-element.md).</span></span> <span data-ttu-id="a98cd-106">Профили, основанные на любой другой схеме, будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="a98cd-106">Profiles based on any other schema will be ignored.</span></span>

<span data-ttu-id="a98cd-107">Если [**енаблеаутоконфиг**](lan-policyschema-enableautoconfig-globalflags-element.md) имеет значение false, этот элемент не должен присутствовать в профиле политики локальной сети.</span><span class="sxs-lookup"><span data-stu-id="a98cd-107">When [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) is set to FALSE, this element must not be present in a LAN policy profile.</span></span> <span data-ttu-id="a98cd-108">Если **енаблеаутоконфиг** имеет значение true, этот элемент является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a98cd-108">When **enableAutoConfig** is set to TRUE, then this element is required.</span></span>

``` syntax
<xs:element name="profileList">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="a98cd-109">Элемент **профилелист** определяется элементом [**ланполици**](lan-policyschema-lanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a98cd-109">The **profileList** element is defined by the [**LANPolicy**](lan-policyschema-lanpolicy-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="a98cd-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="a98cd-110">Remarks</span></span>

<span data-ttu-id="a98cd-111">Этот элемент должен содержать только один сетевой профиль.</span><span class="sxs-lookup"><span data-stu-id="a98cd-111">This element should contain exactly one network profile.</span></span> <span data-ttu-id="a98cd-112">Если в политике указано более одного профиля, будет применена только первая сеть.</span><span class="sxs-lookup"><span data-stu-id="a98cd-112">If more than one profile is specified in the policy, only the first network will be applied.</span></span>

## <a name="requirements"></a><span data-ttu-id="a98cd-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a98cd-113">Requirements</span></span>



| <span data-ttu-id="a98cd-114">Требование</span><span class="sxs-lookup"><span data-stu-id="a98cd-114">Requirement</span></span> | <span data-ttu-id="a98cd-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a98cd-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a98cd-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a98cd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a98cd-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a98cd-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a98cd-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a98cd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a98cd-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a98cd-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a98cd-120">См. также</span><span class="sxs-lookup"><span data-stu-id="a98cd-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="a98cd-121">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="a98cd-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a98cd-122">**ланполици**</span><span class="sxs-lookup"><span data-stu-id="a98cd-122">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="a98cd-123">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="a98cd-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a98cd-124">**ланполици**</span><span class="sxs-lookup"><span data-stu-id="a98cd-124">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




