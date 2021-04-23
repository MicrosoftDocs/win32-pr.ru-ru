---
description: Указывает, используют ли компьютеры встроенную службу автоматической настройки (автоконфигурации) для управления беспроводными подключениями.
ms.assetid: c255e0a0-65ae-44a8-95cb-1a000394109d
title: Элемент Енаблеаутоконфиг (Глобалфлагс) (LAN_policy) для WLAN
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
ms.openlocfilehash: 5105b8e634aa5affa8648b763a82bbd60cbaec17
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106188041"
---
# <a name="enableautoconfig-globalflags-element-lan_policy-for-wlan"></a><span data-ttu-id="867e1-103">Элемент Енаблеаутоконфиг (Глобалфлагс) (LAN_policy) для WLAN</span><span class="sxs-lookup"><span data-stu-id="867e1-103">enableAutoConfig (globalFlags) Element (LAN_policy) for WLAN</span></span> 

<span data-ttu-id="867e1-104">Элемент **енаблеаутоконфиг** (глобалфлагс) указывает, используют ли компьютеры встроенную службу автоматической настройки (автоконфигурации) для управления беспроводными подключениями.</span><span class="sxs-lookup"><span data-stu-id="867e1-104">The **enableAutoConfig** (globalFlags) element specifies whether machines use the built-in automatic configuration (AutoConfig) service to manage wireless connections.</span></span> <span data-ttu-id="867e1-105">Если **енаблеаутоконфиг** имеет значение false, то компьютеры не должны использовать автоконфигурацию для управления беспроводными подключениями, а служба автонастройки реагирует только на запросы на включение службы.</span><span class="sxs-lookup"><span data-stu-id="867e1-105">When **enableAutoConfig** has a value of FALSE, machines must not use AutoConfig to manage wireless connections, and the AutoConfig service only responds to requests to enable the service.</span></span> <span data-ttu-id="867e1-106">Если **енаблеаутоконфиг** имеет значение true, компьютеры могут использовать службу автонастройки.</span><span class="sxs-lookup"><span data-stu-id="867e1-106">When **enableAutoConfig** has a value of TRUE, machines may use the AutoConfig service.</span></span>

<span data-ttu-id="867e1-107">Этот элемент является обязательным.</span><span class="sxs-lookup"><span data-stu-id="867e1-107">This element is mandatory.</span></span> <span data-ttu-id="867e1-108">При создании профиля службой автонастройки этот элемент будет иметь значение по умолчанию TRUE.</span><span class="sxs-lookup"><span data-stu-id="867e1-108">When a profile is created by the AutoConfig service, this element will have the default value of TRUE.</span></span>

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

<span data-ttu-id="867e1-109">Элемент **енаблеаутоконфиг** определяется элементом [**глобалфлагс**](wlan-policyschema-globalflags-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="867e1-109">The **enableAutoConfig** element is defined by the [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="867e1-110">Требования</span><span class="sxs-lookup"><span data-stu-id="867e1-110">Requirements</span></span>



| <span data-ttu-id="867e1-111">Требование</span><span class="sxs-lookup"><span data-stu-id="867e1-111">Requirement</span></span> | <span data-ttu-id="867e1-112">Значение</span><span class="sxs-lookup"><span data-stu-id="867e1-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="867e1-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="867e1-113">Minimum supported client</span></span><br/> | <span data-ttu-id="867e1-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="867e1-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="867e1-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="867e1-115">Minimum supported server</span></span><br/> | <span data-ttu-id="867e1-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="867e1-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="867e1-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="867e1-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="867e1-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="867e1-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="867e1-119">**глобалфлагс**</span><span class="sxs-lookup"><span data-stu-id="867e1-119">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="867e1-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="867e1-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="867e1-121">**Глобалфлагс (Вланполици)**</span><span class="sxs-lookup"><span data-stu-id="867e1-121">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




