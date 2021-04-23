---
description: Указывает период времени в минутах, в течение которого будет храниться кэш PMK.
ms.assetid: d9e3b839-48f6-490c-ab83-067368cdcca2
title: Пмккачеттл (Security), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheTTL
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bdfe0edb163dc2bc9766ba8562defb026bbe21fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673239"
---
# <a name="pmkcachettl-security-element"></a><span data-ttu-id="ac834-103">Пмккачеттл (Security), элемент</span><span class="sxs-lookup"><span data-stu-id="ac834-103">PMKCacheTTL (security) Element</span></span>

<span data-ttu-id="ac834-104">Элемент Пмккачеттл (Security) указывает продолжительность времени в минутах, в течение которого будет храниться кэш PMK.</span><span class="sxs-lookup"><span data-stu-id="ac834-104">The PMKCacheTTL (security) element indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="ac834-105">Этот элемент допустим только для сетей, определенных с помощью WPA2, для [**пмккачемоде**](wlan-profileschema-pmkcachemode-security-element.md) задано значение "Enabled".</span><span class="sxs-lookup"><span data-stu-id="ac834-105">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span>

<span data-ttu-id="ac834-106">Кэширование PMK описано в спецификации [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="ac834-106">PMK caching is described in the [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specification.</span></span>

<span data-ttu-id="ac834-107">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ac834-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="PMKCacheTTL"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="5"
             />
            <xs:maxInclusive
                value="1440"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="ac834-108">Элемент определяется элементом [**безопасности**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ac834-108">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac834-109">Требования</span><span class="sxs-lookup"><span data-stu-id="ac834-109">Requirements</span></span>



| <span data-ttu-id="ac834-110">Требование</span><span class="sxs-lookup"><span data-stu-id="ac834-110">Requirement</span></span> | <span data-ttu-id="ac834-111">Значение</span><span class="sxs-lookup"><span data-stu-id="ac834-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ac834-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac834-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ac834-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ac834-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ac834-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac834-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ac834-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ac834-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ac834-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac834-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="ac834-117">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="ac834-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ac834-118">**бюллетеня**</span><span class="sxs-lookup"><span data-stu-id="ac834-118">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="ac834-119">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="ac834-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ac834-120">**безопасность (MSM)**</span><span class="sxs-lookup"><span data-stu-id="ac834-120">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




