---
title: Класс MDM_Firewall_PublicProfile02
description: '\_ \_ Класс PUBLICPROFILE02 брандмауэра MDM используется для настройки параметров брандмауэра защитника Windows.'
ms.assetid: 5524b931-10fa-43dc-8901-238312ecb6a8
keywords:
- Класс MDM_Firewall_PublicProfile02
- MDM_Firewall_PublicProfile02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Firewall_PublicProfile02
- MDM_Firewall_PublicProfile02.InstanceID
- MDM_Firewall_PublicProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530bac28c33b9ed3937f962a7f040e82b2ee1919
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489936"
---
# <a name="mdm_firewall_publicprofile02-class"></a><span data-ttu-id="9bae7-105">\_ \_ Класс PUBLICPROFILE02 брандмауэра MDM</span><span class="sxs-lookup"><span data-stu-id="9bae7-105">MDM\_Firewall\_PublicProfile02 class</span></span>

<span data-ttu-id="9bae7-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="9bae7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9bae7-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="9bae7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9bae7-108">\_ \_ Класс PUBLICPROFILE02 брандмауэра MDM используется для настройки параметров брандмауэра защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="9bae7-108">The MDM\_Firewall\_PublicProfile02 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="9bae7-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="9bae7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bae7-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bae7-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_PublicProfile02
{
  string InstanceID;
  string ParentID;
  sint32 EnableFirewall;
  sint32 DisableStealthMode;
  sint32 Shielded;
  sint32 DisableUnicastResponsesToMulticastBroadcast;
  sint32 DisableInboundNotifications;
  sint32 AuthAppsAllowUserPrefMerge;
  sint32 GlobalPortsAllowUserPrefMerge;
  sint32 AllowLocalPolicyMerge;
  sint32 AllowLocalIpsecPolicyMerge;
  sint32 DefaultOutboundAction;
  sint32 DefaultInboundAction;
  sint32 DisableStealthModeIpsecSecuredPacketExemption;
};
```

## <a name="members"></a><span data-ttu-id="9bae7-111">Члены</span><span class="sxs-lookup"><span data-stu-id="9bae7-111">Members</span></span>

<span data-ttu-id="9bae7-112">Класс **\_ \_ PublicProfile02 брандмауэра MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9bae7-112">The **MDM\_Firewall\_PublicProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="9bae7-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="9bae7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9bae7-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="9bae7-114">Properties</span></span>

<span data-ttu-id="9bae7-115">Класс **\_ \_ PublicProfile02 брандмауэра MDM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9bae7-115">The **MDM\_Firewall\_PublicProfile02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9bae7-116">алловлокалипсекполицимерже</span><span class="sxs-lookup"><span data-stu-id="9bae7-116">AllowLocalIpsecPolicyMerge</span></span>](/windows/client-management/mdm/firewall-csp#allowlocalipsecpolicymerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bae7-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9bae7-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bae7-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9bae7-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9bae7-119">алловлокалполицимерже</span><span class="sxs-lookup"><span data-stu-id="9bae7-119">AllowLocalPolicyMerge</span></span>](/windows/client-management/mdm/firewall-csp#allowlocalpolicymerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bae7-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9bae7-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bae7-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9bae7-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9bae7-122">аусаппсалловусерпрефмерже</span><span class="sxs-lookup"><span data-stu-id="9bae7-122">AuthAppsAllowUserPrefMerge</span></span>](/windows/client-management/mdm/firewall-csp#authappsallowuserprefmerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bae7-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9bae7-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bae7-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9bae7-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9bae7-125">дефаултинбаундактион</span><span class="sxs-lookup"><span data-stu-id="9bae7-125">DefaultInboundAction</span></span>](/windows/client-management/mdm/firewall-csp#defaultinboundaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bae7-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9bae7-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bae7-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9bae7-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9bae7-128">дефаултаутбаундактион</span><span class="sxs-lookup"><span data-stu-id="9bae7-128">DefaultOutboundAction</span></span>](/windows/client-management/mdm/firewall-csp#defaultoutboundaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bae7-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9bae7-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bae7-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9bae7-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9bae7-131">дисаблеинбаунднотификатионс</span><span class="sxs-lookup"><span data-stu-id="9bae7-131">DisableInboundNotifications</span></span>](/windows/client-management/mdm/firewall-csp#disableinboundnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bae7-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9bae7-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bae7-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9bae7-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9bae7-134">дисаблестеалсмоде</span><span class="sxs-lookup"><span data-stu-id="9bae7-134">DisableStealthMode</span></span>](/windows/client-management/mdm/firewall-csp#disablestealthmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bae7-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9bae7-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bae7-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9bae7-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9bae7-137">дисаблестеалсмодеипсексекуредпаккетексемптион</span><span class="sxs-lookup"><span data-stu-id="9bae7-137">DisableStealthModeIpsecSecuredPacketExemption</span></span>](/windows/client-management/mdm/firewall-csp#disablestealthmodeipsecsecuredpacketexemption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bae7-138">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9bae7-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bae7-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9bae7-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9bae7-140">дисаблеуникастреспонсестомултикастброадкаст</span><span class="sxs-lookup"><span data-stu-id="9bae7-140">DisableUnicastResponsesToMulticastBroadcast</span></span>](/windows/client-management/mdm/firewall-csp#disableunicastresponsestomulticastbroadcast)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bae7-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9bae7-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bae7-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9bae7-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9bae7-143">енаблефиревалл</span><span class="sxs-lookup"><span data-stu-id="9bae7-143">EnableFirewall</span></span>](/windows/client-management/mdm/firewall-csp#enablefirewall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bae7-144">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9bae7-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bae7-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9bae7-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9bae7-146">глобалпортсалловусерпрефмерже</span><span class="sxs-lookup"><span data-stu-id="9bae7-146">GlobalPortsAllowUserPrefMerge</span></span>](/windows/client-management/mdm/firewall-csp#globalportsallowuserprefmerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bae7-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9bae7-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bae7-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9bae7-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9bae7-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9bae7-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bae7-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9bae7-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bae7-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bae7-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bae7-152">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9bae7-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9bae7-153">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9bae7-153">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bae7-154">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9bae7-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bae7-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bae7-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bae7-156">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9bae7-156">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9bae7-157">Экранирование</span><span class="sxs-lookup"><span data-stu-id="9bae7-157">Shielded</span></span>](/windows/client-management/mdm/firewall-csp#shielded)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bae7-158">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9bae7-158">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bae7-159">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9bae7-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9bae7-160">Требования</span><span class="sxs-lookup"><span data-stu-id="9bae7-160">Requirements</span></span>



| <span data-ttu-id="9bae7-161">Требование</span><span class="sxs-lookup"><span data-stu-id="9bae7-161">Requirement</span></span> | <span data-ttu-id="9bae7-162">Значение</span><span class="sxs-lookup"><span data-stu-id="9bae7-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bae7-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9bae7-163">Minimum supported client</span></span><br/> | <span data-ttu-id="9bae7-164">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9bae7-164">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9bae7-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9bae7-165">Minimum supported server</span></span><br/> | <span data-ttu-id="9bae7-166">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9bae7-166">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="9bae7-167">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9bae7-167">Namespace</span></span><br/>                | <span data-ttu-id="9bae7-168">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="9bae7-168">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="9bae7-169">MOF</span><span class="sxs-lookup"><span data-stu-id="9bae7-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9bae7-170"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9bae7-170"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="9bae7-171">DLL</span><span class="sxs-lookup"><span data-stu-id="9bae7-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bae7-172"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bae7-172"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

