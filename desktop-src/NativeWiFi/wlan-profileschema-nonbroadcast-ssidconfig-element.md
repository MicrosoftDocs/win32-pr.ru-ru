---
description: Указывает, следует ли подключаться к скрытой сети.
ms.assetid: 31b859e9-adc7-49e2-91d9-4fb63a35addb
title: нешироковещательный элемент (Ссидконфиг)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nonBroadcast
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 695bede631b19c028a55a2f3ca82ba994ca12ada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673441"
---
# <a name="nonbroadcast-ssidconfig-element"></a><span data-ttu-id="14af1-103">нешироковещательный элемент (Ссидконфиг)</span><span class="sxs-lookup"><span data-stu-id="14af1-103">nonBroadcast (SSIDConfig) Element</span></span>

<span data-ttu-id="14af1-104">Элемент нешироковещательной рассылки (Ссидконфиг) указывает, следует ли подключиться к скрытой сети.</span><span class="sxs-lookup"><span data-stu-id="14af1-104">The nonBroadcast (SSIDConfig) element indicates whether to connect to a hidden network.</span></span> <span data-ttu-id="14af1-105">Если сеть не выполняет широковещательную рассылку своего идентификатора SSID, она называется скрытой сетью.</span><span class="sxs-lookup"><span data-stu-id="14af1-105">If a network does not broadcast its SSID, then it is known as a hidden network.</span></span> <span data-ttu-id="14af1-106">Если в профиле задано несколько идентификаторов SSID, все они должны иметь одинаковое нешироковещательное значение.</span><span class="sxs-lookup"><span data-stu-id="14af1-106">If multiple SSIDs are set within the profile, they must all have the same nonBroadcast value.</span></span>

<span data-ttu-id="14af1-107">Если параметру [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) присвоено значение **ESS**, это может быть либо "true", либо "false".</span><span class="sxs-lookup"><span data-stu-id="14af1-107">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to **ESS**, this value can be either "true" or "false".</span></span> <span data-ttu-id="14af1-108">Если этот элемент отсутствует, по умолчанию используется значение false.</span><span class="sxs-lookup"><span data-stu-id="14af1-108">If this element is not present, the default value is "false".</span></span>

<span data-ttu-id="14af1-109">Если параметр [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) имеет значение **ибсс**, это значение должно быть равно "false".</span><span class="sxs-lookup"><span data-stu-id="14af1-109">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to **IBSS**, this value must be "false".</span></span> <span data-ttu-id="14af1-110">Если этот элемент отсутствует, по умолчанию используется значение false.</span><span class="sxs-lookup"><span data-stu-id="14af1-110">If this element is not present, the default value is "false".</span></span>

<span data-ttu-id="14af1-111">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="14af1-111">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="nonBroadcast"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="14af1-112">Элемент определяется элементом [**ссидконфиг**](wlan-profileschema-ssidconfig-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="14af1-112">The element is defined by the [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="14af1-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="14af1-113">Examples</span></span>

<span data-ttu-id="14af1-114">Пример профиля, в котором используется элемент **нешироковещательной рассылки** , см. в разделе [пример профиля без широковещательной рассылки](non-broadcast-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="14af1-114">To view a sample profile that uses the **nonBroadcast** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="14af1-115">Требования</span><span class="sxs-lookup"><span data-stu-id="14af1-115">Requirements</span></span>



| <span data-ttu-id="14af1-116">Требование</span><span class="sxs-lookup"><span data-stu-id="14af1-116">Requirement</span></span> | <span data-ttu-id="14af1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="14af1-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="14af1-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14af1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="14af1-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="14af1-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="14af1-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14af1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="14af1-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="14af1-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14af1-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14af1-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="14af1-123">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="14af1-123">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="14af1-124">**SSIDConfig**</span><span class="sxs-lookup"><span data-stu-id="14af1-124">**SSIDConfig**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="14af1-125">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="14af1-125">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="14af1-126">**Ссидконфиг (Вланпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="14af1-126">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




