---
description: Содержит политику проводной локальной сети.
ms.assetid: c06bdbc4-4199-4eec-a22f-684745912970
title: Ланполици, элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1b424a47405aa8f32276019a85902bd51b173cc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683836"
---
# <a name="lanpolicy-element"></a><span data-ttu-id="58c74-103">Ланполици, элемент</span><span class="sxs-lookup"><span data-stu-id="58c74-103">LANPolicy Element</span></span>

<span data-ttu-id="58c74-104">Элемент Ланполици содержит политику проводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="58c74-104">The LANPolicy element contains a wired LAN policy.</span></span> <span data-ttu-id="58c74-105">Этот элемент является уникальным корневым элементом для профиля политики проводных сетей.</span><span class="sxs-lookup"><span data-stu-id="58c74-105">This element is the unique root element for a wired network policy profile.</span></span>

<span data-ttu-id="58c74-106">Целевое пространство имен для элемента **ланполици** — `https://www.microsoft.com/networking/LAN/policy/v1` .</span><span class="sxs-lookup"><span data-stu-id="58c74-106">The target namespace for the **LANPolicy** element is `https://www.microsoft.com/networking/LAN/policy/v1`.</span></span>

``` syntax
<xs:element name="LANPolicy">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="globalFlags">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enableAutoConfig"
                            type="boolean"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="profileList"
                minOccurs="0"
            >
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
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="58c74-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="58c74-107">Child elements</span></span>



| <span data-ttu-id="58c74-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="58c74-108">Element</span></span>                                                                           | <span data-ttu-id="58c74-109">Тип</span><span class="sxs-lookup"><span data-stu-id="58c74-109">Type</span></span>                                                     | <span data-ttu-id="58c74-110">Описание</span><span class="sxs-lookup"><span data-stu-id="58c74-110">Description</span></span>                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58c74-111">**nописание**</span><span class="sxs-lookup"><span data-stu-id="58c74-111">**description**</span></span>](lan-policyschema-description-lanpolicy-element.md)             | [<span data-ttu-id="58c74-112">**наметипе**</span><span class="sxs-lookup"><span data-stu-id="58c74-112">**nameType**</span></span>](lan-policyschema-nametype-simpletype.md) | <span data-ttu-id="58c74-113">Содержит описание политики проводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="58c74-113">Contains the description of a wired LAN policy.</span></span> <br/>                                                                                                                          |
| [<span data-ttu-id="58c74-114">**енаблеаутоконфиг**</span><span class="sxs-lookup"><span data-stu-id="58c74-114">**enableAutoConfig**</span></span>](lan-policyschema-enableautoconfig-globalflags-element.md) | <span data-ttu-id="58c74-115">Логическое</span><span class="sxs-lookup"><span data-stu-id="58c74-115">boolean</span></span>                                                  | <span data-ttu-id="58c74-116">Указывает, используют ли компьютеры встроенную службу автоматической настройки для управления подключениями к проводным сетям, для которых требуется проверка подлинности уровня 2 (например, 802.1 X).</span><span class="sxs-lookup"><span data-stu-id="58c74-116">Specifies whether machines use the built-in automatic configuration service to manage connections to wired networks that require layer 2 authentication (such as 802.1X).</span></span><br/> |
| [<span data-ttu-id="58c74-117">**глобалфлагс**</span><span class="sxs-lookup"><span data-stu-id="58c74-117">**globalFlags**</span></span>](lan-policyschema-globalflags-lanpolicy-element.md)             |                                                          | <span data-ttu-id="58c74-118">Содержит глобальные параметры для автоматической настройки проводных сетей.</span><span class="sxs-lookup"><span data-stu-id="58c74-118">Contains the global settings for the automatic configuration of wired networks.</span></span> <br/>                                                                                          |
| [<span data-ttu-id="58c74-119">**безымян**</span><span class="sxs-lookup"><span data-stu-id="58c74-119">**name**</span></span>](lan-policyschema-name-lanpolicy-element.md)                           | [<span data-ttu-id="58c74-120">**наметипе**</span><span class="sxs-lookup"><span data-stu-id="58c74-120">**nameType**</span></span>](lan-policyschema-nametype-simpletype.md) | <span data-ttu-id="58c74-121">Содержит имя политики проводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="58c74-121">Contains the name of a wired LAN policy.</span></span> <br/>                                                                                                                                 |
| [<span data-ttu-id="58c74-122">**профилелист**</span><span class="sxs-lookup"><span data-stu-id="58c74-122">**profileList**</span></span>](lan-policyschema-profilelist-lanpolicy-element.md)             |                                                          | <span data-ttu-id="58c74-123">Содержит список профилей, применяемых на уровне домена или компьютера.</span><span class="sxs-lookup"><span data-stu-id="58c74-123">Contains a list of profiles to be applied at the domain or machine level.</span></span> <br/>                                                                                                |



## <a name="remarks"></a><span data-ttu-id="58c74-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58c74-124">Remarks</span></span>

<span data-ttu-id="58c74-125">Сведения о просмотре списка дочерних элементов в древовидной структуре см. в разделе [ \_ элементы схемы политики локальной сети](lan-policyschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="58c74-125">To view the list of child elements in a tree-like structure, see [LAN\_policy Schema Elements](lan-policyschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="58c74-126">Требования</span><span class="sxs-lookup"><span data-stu-id="58c74-126">Requirements</span></span>



| <span data-ttu-id="58c74-127">Требование</span><span class="sxs-lookup"><span data-stu-id="58c74-127">Requirement</span></span> | <span data-ttu-id="58c74-128">Значение</span><span class="sxs-lookup"><span data-stu-id="58c74-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="58c74-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="58c74-129">Minimum supported client</span></span><br/> | <span data-ttu-id="58c74-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="58c74-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="58c74-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="58c74-131">Minimum supported server</span></span><br/> | <span data-ttu-id="58c74-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="58c74-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




