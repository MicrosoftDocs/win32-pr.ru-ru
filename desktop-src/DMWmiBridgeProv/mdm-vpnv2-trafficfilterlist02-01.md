---
title: Класс MDM_VPNv2_TrafficFilterList02_01
description: Класс MDM \_ Поддержка vpnv2 \_ TrafficFilterList02 \_ 01 содержит необязательный список правил. Через интерфейс VPN можно отправить только трафик, который соответствует этим правилам.
ms.assetid: 3cffe96d-7454-43a1-aa5b-33e820369e7e
keywords:
- Класс MDM_VPNv2_TrafficFilterList02_01
- MDM_VPNv2_TrafficFilterList02_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_VPNv2_TrafficFilterList02_01
- MDM_VPNv2_TrafficFilterList02_01.InstanceID
- MDM_VPNv2_TrafficFilterList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3005026a85aa118a4122e073579fcb06389a9fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136750"
---
# <a name="mdm_vpnv2_trafficfilterlist02_01-class"></a><span data-ttu-id="8fcf7-106">\_Класс MDM поддержка vpnv2 \_ TrafficFilterList02 \_ 01</span><span class="sxs-lookup"><span data-stu-id="8fcf7-106">MDM\_VPNv2\_TrafficFilterList02\_01 class</span></span>

<span data-ttu-id="8fcf7-107">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="8fcf7-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8fcf7-108">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="8fcf7-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8fcf7-109">Класс **MDM \_ Поддержка vpnv2 \_ TrafficFilterList02 \_ 01** содержит необязательный список правил.</span><span class="sxs-lookup"><span data-stu-id="8fcf7-109">The **MDM\_VPNv2\_TrafficFilterList02\_01** class contains an optional list of rules.</span></span> <span data-ttu-id="8fcf7-110">Через интерфейс VPN можно отправить только трафик, который соответствует этим правилам.</span><span class="sxs-lookup"><span data-stu-id="8fcf7-110">Only traffic that matches these rules can be sent via the VPN Interface.</span></span>

<span data-ttu-id="8fcf7-111">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="8fcf7-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fcf7-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fcf7-112">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_TrafficFilterList02_01
{
  string InstanceID;
  string ParentID;
  string Claims;
  sint32 Protocol;
  string LocalPortRanges;
  string RemotePortRanges;
  string LocalAddressRanges;
  string RemoteAddressRanges;
  string RoutingPolicyType;
};
```

## <a name="members"></a><span data-ttu-id="8fcf7-113">Члены</span><span class="sxs-lookup"><span data-stu-id="8fcf7-113">Members</span></span>

<span data-ttu-id="8fcf7-114">Класс **MDM \_ Поддержка vpnv2 \_ TrafficFilterList02 \_ 01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8fcf7-114">The **MDM\_VPNv2\_TrafficFilterList02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="8fcf7-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="8fcf7-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8fcf7-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="8fcf7-116">Properties</span></span>

<span data-ttu-id="8fcf7-117">Класс **MDM \_ Поддержка vpnv2 \_ TrafficFilterList02 \_ 01** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="8fcf7-117">The **MDM\_VPNv2\_TrafficFilterList02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8fcf7-118">Утверждения</span><span class="sxs-lookup"><span data-stu-id="8fcf7-118">Claims</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-claims)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fcf7-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8fcf7-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fcf7-120">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8fcf7-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8fcf7-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8fcf7-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fcf7-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8fcf7-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fcf7-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8fcf7-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fcf7-124">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8fcf7-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8fcf7-125">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="8fcf7-125">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="8fcf7-126">локаладдрессранжес</span><span class="sxs-lookup"><span data-stu-id="8fcf7-126">LocalAddressRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-localaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fcf7-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8fcf7-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fcf7-128">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8fcf7-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8fcf7-129">локалпортранжес</span><span class="sxs-lookup"><span data-stu-id="8fcf7-129">LocalPortRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-localportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fcf7-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8fcf7-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fcf7-131">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8fcf7-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8fcf7-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8fcf7-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fcf7-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8fcf7-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fcf7-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8fcf7-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fcf7-135">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8fcf7-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8fcf7-136">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="8fcf7-136">Describes the full path to the parent node.</span></span> <span data-ttu-id="8fcf7-137">Для этого класса строка имеет значение "./Vendor/MSFT/VPNv2/*имя_профиля*/траффикфилтерлист"</span><span class="sxs-lookup"><span data-stu-id="8fcf7-137">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList"</span></span>

</dd> <dt>

[<span data-ttu-id="8fcf7-138">Протокол</span><span class="sxs-lookup"><span data-stu-id="8fcf7-138">Protocol</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-protocol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fcf7-139">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8fcf7-139">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8fcf7-140">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8fcf7-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8fcf7-141">ремотеаддрессранжес</span><span class="sxs-lookup"><span data-stu-id="8fcf7-141">RemoteAddressRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-remoteaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fcf7-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8fcf7-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fcf7-143">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8fcf7-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8fcf7-144">ремотепортранжес</span><span class="sxs-lookup"><span data-stu-id="8fcf7-144">RemotePortRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-remoteportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fcf7-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8fcf7-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fcf7-146">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8fcf7-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8fcf7-147">RoutingPolicyType</span><span class="sxs-lookup"><span data-stu-id="8fcf7-147">RoutingPolicyType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-routingpolicytype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fcf7-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8fcf7-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fcf7-149">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8fcf7-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8fcf7-150">Требования</span><span class="sxs-lookup"><span data-stu-id="8fcf7-150">Requirements</span></span>



| <span data-ttu-id="8fcf7-151">Требование</span><span class="sxs-lookup"><span data-stu-id="8fcf7-151">Requirement</span></span> | <span data-ttu-id="8fcf7-152">Значение</span><span class="sxs-lookup"><span data-stu-id="8fcf7-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fcf7-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8fcf7-153">Minimum supported client</span></span><br/> | <span data-ttu-id="8fcf7-154">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8fcf7-154">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8fcf7-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8fcf7-155">Minimum supported server</span></span><br/> | <span data-ttu-id="8fcf7-156">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8fcf7-156">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8fcf7-157">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8fcf7-157">Namespace</span></span><br/>                | <span data-ttu-id="8fcf7-158">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="8fcf7-158">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="8fcf7-159">MOF</span><span class="sxs-lookup"><span data-stu-id="8fcf7-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fcf7-160"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fcf7-160"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8fcf7-161">DLL</span><span class="sxs-lookup"><span data-stu-id="8fcf7-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fcf7-162"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fcf7-162"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fcf7-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8fcf7-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fcf7-164">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="8fcf7-164">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

