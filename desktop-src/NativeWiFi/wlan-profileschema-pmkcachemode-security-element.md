---
description: Указывает, будет ли использоваться кэширование PMK.
ms.assetid: 5650c893-6047-4e99-a2be-22722d6a809a
title: Пмккачемоде (Security), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 609660d6f3161cbaaa5e0505daf9c6b9180b6c32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144548"
---
# <a name="pmkcachemode-security-element"></a><span data-ttu-id="59a56-103">Пмккачемоде (Security), элемент</span><span class="sxs-lookup"><span data-stu-id="59a56-103">PMKCacheMode (security) Element</span></span>

<span data-ttu-id="59a56-104">Элемент Пмккачемоде (Security) указывает, будет ли использоваться кэширование PMK.</span><span class="sxs-lookup"><span data-stu-id="59a56-104">The PMKCacheMode (security) element indicates whether PMK caching will be used.</span></span> <span data-ttu-id="59a56-105">Этот элемент допустим только для сетей, определенных WPA2.</span><span class="sxs-lookup"><span data-stu-id="59a56-105">This element is valid only for WPA2-defined networks.</span></span> <span data-ttu-id="59a56-106">Кэширование PMK описано в спецификации [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="59a56-106">PMK caching is described in the [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specification.</span></span>

<span data-ttu-id="59a56-107">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="59a56-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="PMKCacheMode"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="disabled"
             />
            <xs:enumeration
                value="enabled"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="59a56-108">Элемент определяется элементом [**безопасности**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="59a56-108">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="59a56-109">Требования</span><span class="sxs-lookup"><span data-stu-id="59a56-109">Requirements</span></span>



| <span data-ttu-id="59a56-110">Требование</span><span class="sxs-lookup"><span data-stu-id="59a56-110">Requirement</span></span> | <span data-ttu-id="59a56-111">Значение</span><span class="sxs-lookup"><span data-stu-id="59a56-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="59a56-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59a56-112">Minimum supported client</span></span><br/> | <span data-ttu-id="59a56-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59a56-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="59a56-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59a56-114">Minimum supported server</span></span><br/> | <span data-ttu-id="59a56-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="59a56-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59a56-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59a56-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="59a56-117">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="59a56-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="59a56-118">**бюллетеня**</span><span class="sxs-lookup"><span data-stu-id="59a56-118">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="59a56-119">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="59a56-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="59a56-120">**безопасность (MSM)**</span><span class="sxs-lookup"><span data-stu-id="59a56-120">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




