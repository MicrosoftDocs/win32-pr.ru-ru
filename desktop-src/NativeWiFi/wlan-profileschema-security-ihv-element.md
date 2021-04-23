---
description: Содержит различные параметры безопасности, используемые независимыми поставщиками оборудования.
ms.assetid: 237c5d98-3f3c-4279-b2ad-b0d05df041f9
title: Элемент безопасности (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ace1bb0ca31f40fdc9d10fba13832797d8d4306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673898"
---
# <a name="security-ihv-element"></a><span data-ttu-id="b3997-103">Элемент безопасности (IHV)</span><span class="sxs-lookup"><span data-stu-id="b3997-103">security (IHV) Element</span></span>

<span data-ttu-id="b3997-104">Элемент Security (IHV) содержит различные параметры безопасности, используемые независимыми поставщиками оборудования.</span><span class="sxs-lookup"><span data-stu-id="b3997-104">The security (IHV) element contains various security settings used by independent hardware vendors.</span></span>

<span data-ttu-id="b3997-105">Параметры безопасности Microsoft и параметры безопасности IHV являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="b3997-105">Microsoft security settings and IHV security settings are mutually exclusive.</span></span> <span data-ttu-id="b3997-106">Если оба набора параметров безопасности находятся в одном профиле, профиль будет недействительным.</span><span class="sxs-lookup"><span data-stu-id="b3997-106">If both sets of security settings are present in the same profile, the profile is invalid.</span></span>

<span data-ttu-id="b3997-107">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b3997-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="security">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="b3997-108">Элемент **безопасности** определяется элементом [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b3997-108">The **security** element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3997-109">Требования</span><span class="sxs-lookup"><span data-stu-id="b3997-109">Requirements</span></span>



| <span data-ttu-id="b3997-110">Требование</span><span class="sxs-lookup"><span data-stu-id="b3997-110">Requirement</span></span> | <span data-ttu-id="b3997-111">Значение</span><span class="sxs-lookup"><span data-stu-id="b3997-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b3997-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b3997-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b3997-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3997-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b3997-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b3997-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b3997-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3997-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b3997-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3997-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="b3997-117">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="b3997-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b3997-118">**АППАРАТ**</span><span class="sxs-lookup"><span data-stu-id="b3997-118">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="b3997-119">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="b3997-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b3997-120">**IHV (Вланпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="b3997-120">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




