---
title: Класс MDM_Firewall_FirewallRules02_01
description: '\_Класс брандмауэра MDM \_ FirewallRules02 \_ 01 используется для настройки параметров брандмауэра защитника Windows.'
ms.assetid: b09cbd98-152e-486c-acb5-4e1d83e5f8e2
keywords:
- Класс MDM_Firewall_FirewallRules02_01
- MDM_Firewall_FirewallRules02_01 класс, описание
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_Firewall_FirewallRules02_01
- MDM_Firewall_FirewallRules02_01.InstanceID
- MDM_Firewall_FirewallRules02_01.ParentID
- MDM_Firewall_FirewallRules02_01.IcmpTypesAndCodes
- MDM_Firewall_FirewallRules02_01.FriendlyName
api_type:
- DllExport
api_location:
- DMWmiBridgeProv.dll
ms.openlocfilehash: 494be18ece91e7a1776780542f988b80cb822e42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135567"
---
# <a name="mdm_firewall_firewallrules02_01-class"></a><span data-ttu-id="a44a3-105">\_Класс брандмауэра MDM \_ FirewallRules02 \_ 01</span><span class="sxs-lookup"><span data-stu-id="a44a3-105">MDM\_Firewall\_FirewallRules02\_01 class</span></span>

<span data-ttu-id="a44a3-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="a44a3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a44a3-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="a44a3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a44a3-108">\_Класс брандмауэра MDM \_ FirewallRules02 \_ 01 используется для настройки параметров брандмауэра защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="a44a3-108">The MDM\_Firewall\_FirewallRules02\_01 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="a44a3-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="a44a3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a44a3-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a44a3-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_FirewallRules02_01
{
  string  InstanceID;
  string  ParentID;
  sint32  Protocol;
  string  LocalPortRanges;
  string  RemotePortRanges;
  string  LocalAddressRanges;
  string  RemoteAddressRanges;
  string  Description;
  boolean Enabled;
  sint32  Profiles;
  string  Direction;
  string  InterfaceTypes;
  string  IcmpTypesAndCodes;
  boolean EdgeTraversal;
  string  LocalUserAuthorizedList;
  string  Status;
  string  FriendlyName;
  string  Name;
};
```

## <a name="members"></a><span data-ttu-id="a44a3-111">Члены</span><span class="sxs-lookup"><span data-stu-id="a44a3-111">Members</span></span>

<span data-ttu-id="a44a3-112">Класс **\_ брандмауэра MDM \_ FirewallRules02 \_ 01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a44a3-112">The **MDM\_Firewall\_FirewallRules02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="a44a3-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="a44a3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a44a3-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="a44a3-114">Properties</span></span>

<span data-ttu-id="a44a3-115">Класс **\_ брандмауэра MDM \_ FirewallRules02 \_ 01** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="a44a3-115">The **MDM\_Firewall\_FirewallRules02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a44a3-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a44a3-116">Description</span></span>](/windows/client-management/mdm/firewall-csp#description)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a44a3-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a44a3-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a44a3-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a44a3-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a44a3-119">Направление</span><span class="sxs-lookup"><span data-stu-id="a44a3-119">Direction</span></span>](/windows/client-management/mdm/firewall-csp#direction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a44a3-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a44a3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a44a3-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a44a3-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a44a3-122">еджетраверсал</span><span class="sxs-lookup"><span data-stu-id="a44a3-122">EdgeTraversal</span></span>](/windows/client-management/mdm/firewall-csp#edgetraversal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a44a3-123">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a44a3-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a44a3-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a44a3-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a44a3-125">Enabled</span><span class="sxs-lookup"><span data-stu-id="a44a3-125">Enabled</span></span>](/windows/client-management/mdm/firewall-csp#enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a44a3-126">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a44a3-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a44a3-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a44a3-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a44a3-128">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="a44a3-128">**FriendlyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a44a3-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a44a3-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a44a3-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a44a3-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a44a3-131">TBD</span><span class="sxs-lookup"><span data-stu-id="a44a3-131">TBD</span></span>

</dd> <dt>

<span data-ttu-id="a44a3-132">**икмптипесандкодес**</span><span class="sxs-lookup"><span data-stu-id="a44a3-132">**IcmpTypesAndCodes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a44a3-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a44a3-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a44a3-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a44a3-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a44a3-135">TBD</span><span class="sxs-lookup"><span data-stu-id="a44a3-135">TBD</span></span>

</dd> <dt>

<span data-ttu-id="a44a3-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a44a3-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a44a3-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a44a3-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a44a3-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a44a3-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a44a3-139">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a44a3-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a44a3-140">интерфацетипес</span><span class="sxs-lookup"><span data-stu-id="a44a3-140">InterfaceTypes</span></span>](/windows/client-management/mdm/firewall-csp#interfacetypes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a44a3-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a44a3-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a44a3-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a44a3-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a44a3-143">локаладдрессранжес</span><span class="sxs-lookup"><span data-stu-id="a44a3-143">LocalAddressRanges</span></span>](/windows/client-management/mdm/firewall-csp#localaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a44a3-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a44a3-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a44a3-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a44a3-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a44a3-146">локалпортранжес</span><span class="sxs-lookup"><span data-stu-id="a44a3-146">LocalPortRanges</span></span>](/windows/client-management/mdm/firewall-csp#localportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a44a3-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a44a3-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a44a3-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a44a3-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a44a3-149">локалусераусоризедлист</span><span class="sxs-lookup"><span data-stu-id="a44a3-149">LocalUserAuthorizedList</span></span>](/windows/client-management/mdm/firewall-csp#localuserauthorizedlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a44a3-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a44a3-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a44a3-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a44a3-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a44a3-152">Name</span><span class="sxs-lookup"><span data-stu-id="a44a3-152">Name</span></span>](/windows/client-management/mdm/firewall-csp#name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a44a3-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a44a3-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a44a3-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a44a3-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a44a3-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a44a3-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a44a3-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a44a3-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a44a3-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a44a3-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a44a3-158">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a44a3-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a44a3-159">Профили</span><span class="sxs-lookup"><span data-stu-id="a44a3-159">Profiles</span></span>](/windows/client-management/mdm/firewall-csp#profiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a44a3-160">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="a44a3-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a44a3-161">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a44a3-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a44a3-162">Протокол</span><span class="sxs-lookup"><span data-stu-id="a44a3-162">Protocol</span></span>](/windows/client-management/mdm/firewall-csp#protocol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a44a3-163">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="a44a3-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a44a3-164">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a44a3-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a44a3-165">ремотеаддрессранжес</span><span class="sxs-lookup"><span data-stu-id="a44a3-165">RemoteAddressRanges</span></span>](/windows/client-management/mdm/firewall-csp#remoteaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a44a3-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a44a3-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a44a3-167">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a44a3-167">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a44a3-168">ремотепортранжес</span><span class="sxs-lookup"><span data-stu-id="a44a3-168">RemotePortRanges</span></span>](/windows/client-management/mdm/firewall-csp#remoteportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a44a3-169">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a44a3-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a44a3-170">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a44a3-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a44a3-171">Состояние</span><span class="sxs-lookup"><span data-stu-id="a44a3-171">Status</span></span>](/windows/client-management/mdm/firewall-csp#status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a44a3-172">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a44a3-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a44a3-173">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a44a3-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a44a3-174">Требования</span><span class="sxs-lookup"><span data-stu-id="a44a3-174">Requirements</span></span>



| <span data-ttu-id="a44a3-175">Требование</span><span class="sxs-lookup"><span data-stu-id="a44a3-175">Requirement</span></span> | <span data-ttu-id="a44a3-176">Значение</span><span class="sxs-lookup"><span data-stu-id="a44a3-176">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a44a3-177">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a44a3-177">Minimum supported client</span></span><br/> | <span data-ttu-id="a44a3-178">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a44a3-178">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a44a3-179">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a44a3-179">Minimum supported server</span></span><br/> | <span data-ttu-id="a44a3-180">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a44a3-180">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="a44a3-181">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a44a3-181">Namespace</span></span><br/>                | <span data-ttu-id="a44a3-182">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="a44a3-182">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="a44a3-183">MOF</span><span class="sxs-lookup"><span data-stu-id="a44a3-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a44a3-184"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a44a3-184"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="a44a3-185">DLL</span><span class="sxs-lookup"><span data-stu-id="a44a3-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a44a3-186"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a44a3-186"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

