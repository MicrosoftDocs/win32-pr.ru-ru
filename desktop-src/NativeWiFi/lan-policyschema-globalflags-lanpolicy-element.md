---
description: Содержит глобальные параметры для автоматической настройки проводных сетей.
ms.assetid: 172cf15c-cd51-43d4-ae5d-f9460c2a40e2
title: Глобалфлагс (Ланполици), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- globalFlags
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c9a244fbbc616e3092e2293fe187da1d7be0fa53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265406"
---
# <a name="globalflags-lanpolicy-element"></a><span data-ttu-id="ef79f-103">Глобалфлагс (Ланполици), элемент</span><span class="sxs-lookup"><span data-stu-id="ef79f-103">globalFlags (LANPolicy) Element</span></span>

<span data-ttu-id="ef79f-104">Элемент Глобалфлагс (Ланполици) содержит глобальные параметры для автоматической настройки проводных сетей.</span><span class="sxs-lookup"><span data-stu-id="ef79f-104">The globalFlags (LANPolicy) element contains the global settings for the automatic configuration of wired networks.</span></span>

``` syntax
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
```

<span data-ttu-id="ef79f-105">Элемент **глобалфлагс** определяется элементом [**ланполици**](lan-policyschema-lanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ef79f-105">The **globalFlags** element is defined by the [**LANPolicy**](lan-policyschema-lanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ef79f-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ef79f-106">Child elements</span></span>



| <span data-ttu-id="ef79f-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="ef79f-107">Element</span></span>                                                                           | <span data-ttu-id="ef79f-108">Тип</span><span class="sxs-lookup"><span data-stu-id="ef79f-108">Type</span></span>    | <span data-ttu-id="ef79f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ef79f-109">Description</span></span>                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef79f-110">**енаблеаутоконфиг**</span><span class="sxs-lookup"><span data-stu-id="ef79f-110">**enableAutoConfig**</span></span>](lan-policyschema-enableautoconfig-globalflags-element.md) | <span data-ttu-id="ef79f-111">Логическое</span><span class="sxs-lookup"><span data-stu-id="ef79f-111">boolean</span></span> | <span data-ttu-id="ef79f-112">Указывает, используют ли компьютеры встроенную службу автоматической настройки для управления подключениями к проводным сетям, для которых требуется проверка подлинности уровня 2 (например, 802.1 X).</span><span class="sxs-lookup"><span data-stu-id="ef79f-112">Specifies whether machines use the built-in automatic configuration service to manage connections to wired networks that require layer 2 authentication (such as 802.1X).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ef79f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ef79f-113">Requirements</span></span>



| <span data-ttu-id="ef79f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ef79f-114">Requirement</span></span> | <span data-ttu-id="ef79f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ef79f-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ef79f-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef79f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ef79f-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ef79f-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ef79f-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef79f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ef79f-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ef79f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ef79f-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef79f-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="ef79f-121">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="ef79f-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ef79f-122">**ланполици**</span><span class="sxs-lookup"><span data-stu-id="ef79f-122">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="ef79f-123">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="ef79f-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ef79f-124">**ланполици**</span><span class="sxs-lookup"><span data-stu-id="ef79f-124">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




