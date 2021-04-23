---
description: Указывает, будет ли клиент использовать предварительную проверку подлинности.
ms.assetid: 305d77b6-fe2d-45c6-ac91-5769f91de152
title: Преаусмоде (Security), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ac74f193fb89c260b1a121b673f239147658865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673238"
---
# <a name="preauthmode-security-element"></a><span data-ttu-id="1f7c0-103">Преаусмоде (Security), элемент</span><span class="sxs-lookup"><span data-stu-id="1f7c0-103">preAuthMode (security) Element</span></span>

<span data-ttu-id="1f7c0-104">Элемент Преаусмоде (Security) указывает, будет ли клиент использовать предварительную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="1f7c0-104">The preAuthMode (security) element indicates whether pre-authentication will be used by the client.</span></span> <span data-ttu-id="1f7c0-105">Предварительная проверка подлинности необходима для безопасного быстрого роуминга WPA2.</span><span class="sxs-lookup"><span data-stu-id="1f7c0-105">Pre-authentication is necessary for WPA2 secure fast roaming.</span></span> <span data-ttu-id="1f7c0-106">Этот элемент допустим только для сетей, определенных с помощью WPA2, для [**пмккачемоде**](wlan-profileschema-pmkcachemode-security-element.md) задано значение "Enabled".</span><span class="sxs-lookup"><span data-stu-id="1f7c0-106">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="1f7c0-107">Если **пмккачемоде** включен и этот элемент отсутствует, по умолчанию используется значение Disabled (отключено).</span><span class="sxs-lookup"><span data-stu-id="1f7c0-107">If **PMKCacheMode** is enabled, and this element is absent, the default value is "disabled".</span></span>

<span data-ttu-id="1f7c0-108">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1f7c0-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="preAuthMode"
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

<span data-ttu-id="1f7c0-109">Элемент определяется элементом [**безопасности**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1f7c0-109">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f7c0-110">Требования</span><span class="sxs-lookup"><span data-stu-id="1f7c0-110">Requirements</span></span>



| <span data-ttu-id="1f7c0-111">Требование</span><span class="sxs-lookup"><span data-stu-id="1f7c0-111">Requirement</span></span> | <span data-ttu-id="1f7c0-112">Значение</span><span class="sxs-lookup"><span data-stu-id="1f7c0-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1f7c0-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1f7c0-113">Minimum supported client</span></span><br/> | <span data-ttu-id="1f7c0-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1f7c0-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1f7c0-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1f7c0-115">Minimum supported server</span></span><br/> | <span data-ttu-id="1f7c0-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1f7c0-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1f7c0-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f7c0-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="1f7c0-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="1f7c0-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="1f7c0-119">**бюллетеня**</span><span class="sxs-lookup"><span data-stu-id="1f7c0-119">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="1f7c0-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="1f7c0-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="1f7c0-121">**безопасность (MSM)**</span><span class="sxs-lookup"><span data-stu-id="1f7c0-121">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




