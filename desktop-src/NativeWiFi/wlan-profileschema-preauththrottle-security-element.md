---
description: Указывает число попыток предварительной проверки подлинности при обращении к соседним ТД.
ms.assetid: 7e89e962-7544-4efb-9e3c-c108bee22aea
title: Преауссроттле (Security), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthThrottle
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 499401affb264238a065c0861f1230f23936206e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541031"
---
# <a name="preauththrottle-security-element"></a><span data-ttu-id="6aec4-103">Преауссроттле (Security), элемент</span><span class="sxs-lookup"><span data-stu-id="6aec4-103">preAuthThrottle (security) Element</span></span>

<span data-ttu-id="6aec4-104">Элемент Преауссроттле (Security) указывает номер, предпринимаемый предварительной проверкой подлинности при обращении к соседним ТД.</span><span class="sxs-lookup"><span data-stu-id="6aec4-104">The preAuthThrottle (security) element specifies the number pre-authentication attempts to try on neighboring APs.</span></span> <span data-ttu-id="6aec4-105">Этот элемент допустим только для сетей, определенных с помощью WPA2, для [**пмккачемоде**](wlan-profileschema-pmkcachemode-security-element.md) задано значение "Enabled".</span><span class="sxs-lookup"><span data-stu-id="6aec4-105">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="6aec4-106">Если **пмккачемоде** включен и этот элемент отсутствует, число попыток по умолчанию будет равно 3.</span><span class="sxs-lookup"><span data-stu-id="6aec4-106">If **PMKCacheMode** is enabled, and this element is absent, the number of tries defaults to 3.</span></span>

<span data-ttu-id="6aec4-107">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6aec4-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="preAuthThrottle"
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
                value="16"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="6aec4-108">Элемент определяется элементом [**безопасности**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6aec4-108">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="6aec4-109">Требования</span><span class="sxs-lookup"><span data-stu-id="6aec4-109">Requirements</span></span>



| <span data-ttu-id="6aec4-110">Требование</span><span class="sxs-lookup"><span data-stu-id="6aec4-110">Requirement</span></span> | <span data-ttu-id="6aec4-111">Значение</span><span class="sxs-lookup"><span data-stu-id="6aec4-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6aec4-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6aec4-112">Minimum supported client</span></span><br/> | <span data-ttu-id="6aec4-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6aec4-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6aec4-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6aec4-114">Minimum supported server</span></span><br/> | <span data-ttu-id="6aec4-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6aec4-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6aec4-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6aec4-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="6aec4-117">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="6aec4-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6aec4-118">**бюллетеня**</span><span class="sxs-lookup"><span data-stu-id="6aec4-118">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="6aec4-119">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="6aec4-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6aec4-120">**безопасность (MSM)**</span><span class="sxs-lookup"><span data-stu-id="6aec4-120">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




