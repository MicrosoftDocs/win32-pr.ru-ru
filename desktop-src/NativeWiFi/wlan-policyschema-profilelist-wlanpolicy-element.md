---
description: Элемент Профилелист (Вланполици) — содержит список профилей, применяемых на уровне домена или компьютера.
ms.assetid: b78cb095-a1da-4b1b-91d3-c5085325be05
title: Профилелист (Вланполици), элемент
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
ms.openlocfilehash: 4c7478f38ba7336738325bac6872866cd570288b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109202"
---
# <a name="profilelist-wlanpolicy-element"></a><span data-ttu-id="ff273-103">Профилелист (Вланполици), элемент</span><span class="sxs-lookup"><span data-stu-id="ff273-103">profileList (WLANPolicy) Element</span></span>

<span data-ttu-id="ff273-104">Элемент Профилелист (Вланполици) содержит список профилей, применяемых на уровне домена или компьютера.</span><span class="sxs-lookup"><span data-stu-id="ff273-104">The profileList (WLANPolicy) element contains a list of profiles to be applied at the domain or machine level.</span></span> <span data-ttu-id="ff273-105">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ff273-105">This element is optional.</span></span> <span data-ttu-id="ff273-106">Если этот элемент имеется, он должен содержать по крайней мере один профиль.</span><span class="sxs-lookup"><span data-stu-id="ff273-106">If this element is present, it must contain at least one profile.</span></span>

<span data-ttu-id="ff273-107">Профили должны основываться на [ \_ схеме профиля WLAN](wlan-profileschema-schema.md)с корневым элементом [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md).</span><span class="sxs-lookup"><span data-stu-id="ff273-107">Profiles should be based on the [WLAN\_profile schema](wlan-profileschema-schema.md), with a root element of [**WLANProfile**](wlan-profileschema-wlanprofile-element.md).</span></span>

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

<span data-ttu-id="ff273-108">Элемент **профилелист** определяется элементом [**вланполици**](wlan-policyschema-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ff273-108">The **profileList** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff273-109">Требования</span><span class="sxs-lookup"><span data-stu-id="ff273-109">Requirements</span></span>



| <span data-ttu-id="ff273-110">Требование</span><span class="sxs-lookup"><span data-stu-id="ff273-110">Requirement</span></span> | <span data-ttu-id="ff273-111">Значение</span><span class="sxs-lookup"><span data-stu-id="ff273-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ff273-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff273-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ff273-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ff273-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ff273-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff273-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ff273-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ff273-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ff273-116">См. также</span><span class="sxs-lookup"><span data-stu-id="ff273-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="ff273-117">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="ff273-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ff273-118">**вланполици**</span><span class="sxs-lookup"><span data-stu-id="ff273-118">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="ff273-119">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="ff273-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ff273-120">**вланполици**</span><span class="sxs-lookup"><span data-stu-id="ff273-120">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




