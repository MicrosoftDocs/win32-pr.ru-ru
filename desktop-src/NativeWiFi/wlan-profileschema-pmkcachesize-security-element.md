---
description: Указывает количество записей в кэше PMK на клиенте.
ms.assetid: 3a53f7fd-7f12-43d3-94e6-a11bec389a34
title: Пмккачесизе (Security), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheSize
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1b21054ddc97c51212ea3a06207617ad85228270
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673240"
---
# <a name="pmkcachesize-security-element"></a><span data-ttu-id="a462a-103">Пмккачесизе (Security), элемент</span><span class="sxs-lookup"><span data-stu-id="a462a-103">PMKCacheSize (security) Element</span></span>

<span data-ttu-id="a462a-104">Элемент Пмккачесизе (Security) указывает количество записей в кэше PMK на клиенте.</span><span class="sxs-lookup"><span data-stu-id="a462a-104">The PMKCacheSize (security) element specifies the number of entries in the PMK cache on the client.</span></span> <span data-ttu-id="a462a-105">Этот элемент допустим только для сетей, определенных с помощью WPA2, для [**пмккачемоде**](wlan-profileschema-pmkcachemode-security-element.md) задано значение "Enabled".</span><span class="sxs-lookup"><span data-stu-id="a462a-105">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="a462a-106">Если **пмккачемоде** включен и этот элемент отсутствует, размер кэша по умолчанию составляет 128 записей.</span><span class="sxs-lookup"><span data-stu-id="a462a-106">If **PMKCacheMode** is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span>

<span data-ttu-id="a462a-107">Кэширование PMK описано в спецификации [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="a462a-107">PMK caching is described in the [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specification.</span></span>

<span data-ttu-id="a462a-108">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a462a-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="PMKCacheSize"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="255"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="a462a-109">Элемент определяется элементом [**безопасности**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a462a-109">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="a462a-110">Требования</span><span class="sxs-lookup"><span data-stu-id="a462a-110">Requirements</span></span>



| <span data-ttu-id="a462a-111">Требование</span><span class="sxs-lookup"><span data-stu-id="a462a-111">Requirement</span></span> | <span data-ttu-id="a462a-112">Значение</span><span class="sxs-lookup"><span data-stu-id="a462a-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a462a-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a462a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a462a-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a462a-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a462a-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a462a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a462a-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a462a-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a462a-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a462a-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="a462a-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="a462a-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a462a-119">**бюллетеня**</span><span class="sxs-lookup"><span data-stu-id="a462a-119">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="a462a-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="a462a-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a462a-121">**безопасность (MSM)**</span><span class="sxs-lookup"><span data-stu-id="a462a-121">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




