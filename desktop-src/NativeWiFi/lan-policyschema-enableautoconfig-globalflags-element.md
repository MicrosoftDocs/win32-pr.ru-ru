---
description: Указывает, используют ли компьютеры встроенную службу автоматической настройки для управления подключениями к проводным сетям, для которых требуется проверка подлинности уровня 2 (например, 802.1 X).
ms.assetid: c7a0f6bc-4d42-4d95-8483-2c480f4d8db9
title: Элемент Енаблеаутоконфиг (Глобалфлагс) (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- enableAutoConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: af1ca32f177140bbfc6563f74df5afc519ee0c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815424"
---
# <a name="enableautoconfig-globalflags-element-lan_policy"></a><span data-ttu-id="0e8c3-103">Элемент Енаблеаутоконфиг (Глобалфлагс) (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="0e8c3-103">enableAutoConfig (globalFlags) Element (LAN_policy)</span></span>

<span data-ttu-id="0e8c3-104">Элемент **енаблеаутоконфиг** (глобалфлагс) указывает, используют ли компьютеры встроенную службу автоматической настройки для управления подключениями к проводным сетям, для которых требуется проверка подлинности уровня 2 (например, 802.1 x).</span><span class="sxs-lookup"><span data-stu-id="0e8c3-104">The **enableAutoConfig** (globalFlags) element specifies whether machines use the built-in automatic configuration service to manage connections to wired networks that require layer 2 authentication (such as 802.1X).</span></span>

<span data-ttu-id="0e8c3-105">Если **енаблеаутоконфиг** имеет значение false, компьютеры не должны использовать встроенную службу автоматической настройки для управления подключениями, требующими проверки подлинности уровня 2.</span><span class="sxs-lookup"><span data-stu-id="0e8c3-105">When **enableAutoConfig** has a value of FALSE, machines must not use built-in automatic configuration service to manage connections that require layer 2 authentication.</span></span> <span data-ttu-id="0e8c3-106">Вместо этого сеть, указанная в элементе [**профилелист**](lan-policyschema-profilelist-lanpolicy-element.md) , является единственной сетью, доступной для подключения.</span><span class="sxs-lookup"><span data-stu-id="0e8c3-106">Instead, the network specified in the [**profileList**](lan-policyschema-profilelist-lanpolicy-element.md) element is the only network available for connection.</span></span> <span data-ttu-id="0e8c3-107">Служба автоматической настройки будет отвечать только на запросы на включение службы.</span><span class="sxs-lookup"><span data-stu-id="0e8c3-107">The automatic configuration service will only respond to requests to enable the service.</span></span>

<span data-ttu-id="0e8c3-108">Если **енаблеаутоконфиг** имеет значение true, компьютеры могут использовать встроенную службу автоматической настройки для подключения к проводным сетям, для которых требуется проверка подлинности уровня 2.</span><span class="sxs-lookup"><span data-stu-id="0e8c3-108">When **enableAutoConfig** has a value of TRUE, machines may use the built-in automatic configuration service to connect to wired networks that require layer 2 authentication.</span></span>

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

<span data-ttu-id="0e8c3-109">Элемент **енаблеаутоконфиг** определяется элементом [**глобалфлагс**](lan-policyschema-globalflags-lanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0e8c3-109">The **enableAutoConfig** element is defined by the [**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e8c3-110">Требования</span><span class="sxs-lookup"><span data-stu-id="0e8c3-110">Requirements</span></span>



| <span data-ttu-id="0e8c3-111">Требование</span><span class="sxs-lookup"><span data-stu-id="0e8c3-111">Requirement</span></span> | <span data-ttu-id="0e8c3-112">Значение</span><span class="sxs-lookup"><span data-stu-id="0e8c3-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0e8c3-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e8c3-113">Minimum supported client</span></span><br/> | <span data-ttu-id="0e8c3-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0e8c3-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0e8c3-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e8c3-115">Minimum supported server</span></span><br/> | <span data-ttu-id="0e8c3-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0e8c3-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0e8c3-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e8c3-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="0e8c3-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="0e8c3-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0e8c3-119">**глобалфлагс**</span><span class="sxs-lookup"><span data-stu-id="0e8c3-119">**globalFlags**</span></span>](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="0e8c3-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="0e8c3-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="0e8c3-121">**Глобалфлагс (Ланполици)**</span><span class="sxs-lookup"><span data-stu-id="0e8c3-121">**globalFlags (LANPolicy)**</span></span>](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> </dl>

 

 




