---
description: Определяет режим роуминга для автоматической подключенной сети при наличии более предпочтительной сети в диапазоне.
ms.assetid: 095dc797-1249-43aa-a8b7-5fa6eaee2a74
title: Элемент автопереключателя (Вланпрофиле)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- autoSwitch
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7ae05b18f58927e05c952edbbfc1b6a6190cec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898114"
---
# <a name="autoswitch-wlanprofile-element"></a><span data-ttu-id="34b37-103">Элемент автопереключателя (Вланпрофиле)</span><span class="sxs-lookup"><span data-stu-id="34b37-103">autoSwitch (WLANProfile) Element</span></span>

<span data-ttu-id="34b37-104">Элемент автопереключения (Вланпрофиле) определяет поведение при роуминге для автоматической подключенной сети в том случае, если используется более Предпочтительная сеть.</span><span class="sxs-lookup"><span data-stu-id="34b37-104">The autoSwitch (WLANProfile) element determines the roaming behavior of an auto-connected network when a more preferred network is in range.</span></span> <span data-ttu-id="34b37-105">.</span><span class="sxs-lookup"><span data-stu-id="34b37-105">.</span></span> <span data-ttu-id="34b37-106">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="34b37-106">This element is optional.</span></span>

<span data-ttu-id="34b37-107">Если для параметра автопереключения задано значение "true", а для [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) задано значение "Auto", попытка подключения к более предпочтительной сети должна выполняться, когда сеть будет находиться в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="34b37-107">If autoSwitch is "true" and [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) is set to "auto", a connection to a more preferred network must be attempted whenever a more preferred network comes into range.</span></span> <span data-ttu-id="34b37-108">Более предпочтительной является сеть, которая выше в списке предпочтительных беспроводных сетей.</span><span class="sxs-lookup"><span data-stu-id="34b37-108">A more preferred network is one that is ordered higher in the list of preferred wireless networks.</span></span> <span data-ttu-id="34b37-109">Эта попытка подключения происходит при подключении к другой сети.</span><span class="sxs-lookup"><span data-stu-id="34b37-109">This connection attempt occurs when connected to another network.</span></span>

<span data-ttu-id="34b37-110">Если для [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) задано значение "Auto", это может быть либо "true", либо "false".</span><span class="sxs-lookup"><span data-stu-id="34b37-110">If [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) is set to "auto", this value can be either "true" or "false".</span></span>

<span data-ttu-id="34b37-111">Если для [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) задано значение "вручную", для этого значения должно быть задано "false".</span><span class="sxs-lookup"><span data-stu-id="34b37-111">If [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) is set to "manual", this value must be set to "false".</span></span> <span data-ttu-id="34b37-112">Этот элемент не влияет на сеть, подключенную вручную.</span><span class="sxs-lookup"><span data-stu-id="34b37-112">This element has no effect on a manually connected network.</span></span>

<span data-ttu-id="34b37-113">Значение автопереключения, заданное как "true", приводит к более высокой частоте периодического сканирования для новых сетей.</span><span class="sxs-lookup"><span data-stu-id="34b37-113">An autoSwitch value set to "true" results in a higher frequency of periodic scanning for new networks.</span></span> <span data-ttu-id="34b37-114">Это может привести к увеличению числа радиочастотных проверок и увеличению энергопотребления, используемого беспроводным сетевым адаптером.</span><span class="sxs-lookup"><span data-stu-id="34b37-114">This may result in increased radio frequency pollution from these periodic scans and increased power consumption used by the wireless network adapter.</span></span>

<span data-ttu-id="34b37-115">**Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети:** Изменения реализуются в Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети для оптимизации производительности беспроводных сетей.</span><span class="sxs-lookup"><span data-stu-id="34b37-115">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="34b37-116">Эти изменения призваны снизить засоренность радиочастотой, энергопотребление и прерывание трафика в режиме реального времени через беспроводные сети.</span><span class="sxs-lookup"><span data-stu-id="34b37-116">These changes are designed to reduce radio frequency pollution, power consumption, and disruption to real-time traffic over wireless networks.</span></span> <span data-ttu-id="34b37-117">Параметр по умолчанию для **автопереключения** , если этот элемент не задан в профиле беспроводной локальной сети, изменился.</span><span class="sxs-lookup"><span data-stu-id="34b37-117">The default setting for **autoSwitch** when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="34b37-118">Значение по умолчанию изменено на "false" в Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="34b37-118">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="34b37-119">Значение по умолчанию — true в Windows Server 2008 и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="34b37-119">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="34b37-120">Рекомендуется, чтобы значение элемента **Автопереключателя** , используемое приложением в профиле беспроводной локальной сети, было равно "false", чтобы снизить частоту периодического сканирования для новых сетей, если нет абсолютной необходимости в приложении установить это значение "true".</span><span class="sxs-lookup"><span data-stu-id="34b37-120">It is recommended that the value of the **autoSwitch** element used by an application in a wireless LAN profile be set to "false" to reduce the frequency of periodic scanning for new networks, unless it is absolutely necessary for an application to set this value to "true".</span></span>

<span data-ttu-id="34b37-121">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="34b37-121">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="autoSwitch"
    type="boolean"
 />
```

<span data-ttu-id="34b37-122">Элемент **автопереключения** определяется элементом [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="34b37-122">The **autoSwitch** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="34b37-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="34b37-123">Examples</span></span>

<span data-ttu-id="34b37-124">Чтобы просмотреть образцы профилей, в которых используется элемент **автопереключения** , см. раздел [образцы профиля беспроводной связи](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="34b37-124">To view sample profiles that use the **autoSwitch** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="34b37-125">Требования</span><span class="sxs-lookup"><span data-stu-id="34b37-125">Requirements</span></span>



| <span data-ttu-id="34b37-126">Требование</span><span class="sxs-lookup"><span data-stu-id="34b37-126">Requirement</span></span> | <span data-ttu-id="34b37-127">Значение</span><span class="sxs-lookup"><span data-stu-id="34b37-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="34b37-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34b37-128">Minimum supported client</span></span><br/> | <span data-ttu-id="34b37-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="34b37-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="34b37-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34b37-130">Minimum supported server</span></span><br/> | <span data-ttu-id="34b37-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="34b37-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="34b37-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34b37-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="34b37-133">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="34b37-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="34b37-134">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="34b37-134">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="34b37-135">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="34b37-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="34b37-136">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="34b37-136">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




