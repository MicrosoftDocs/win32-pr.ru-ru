---
title: Класс MDM_Firewall_Global02
description: '\_ \_ Класс GLOBAL02 брандмауэра MDM используется для настройки параметров брандмауэра защитника Windows.'
ms.assetid: 387a60c6-6dc9-4710-a1e3-0468ac004395
keywords:
- Класс MDM_Firewall_Global02
- MDM_Firewall_Global02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Firewall_Global02
- MDM_Firewall_Global02.InstanceID
- MDM_Firewall_Global02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cef2a8b11585848ac10035528db176b78d2e66b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262190"
---
# <a name="mdm_firewall_global02-class"></a><span data-ttu-id="5a355-105">\_ \_ Класс GLOBAL02 брандмауэра MDM</span><span class="sxs-lookup"><span data-stu-id="5a355-105">MDM\_Firewall\_Global02 class</span></span>

<span data-ttu-id="5a355-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="5a355-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5a355-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="5a355-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5a355-108">\_ \_ Класс GLOBAL02 брандмауэра MDM используется для настройки параметров брандмауэра защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="5a355-108">The MDM\_Firewall\_Global02 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="5a355-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="5a355-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a355-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a355-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_Global02
{
  string  InstanceID;
  string  ParentID;
  sint32  PolicyVersionSupported;
  sint32  CurrentProfiles;
  boolean DisableStatefulFtp;
  sint32  SaIdleTime;
  sint32  PresharedKeyEncoding;
  sint32  IPsecExempt;
  sint32  CRLcheck;
  string  PolicyVersion;
  string  BinaryVersionSupported;
  boolean OpportunisticallyMatchAuthSetPerKM;
  sint32  EnablePacketQueue;
};
```

## <a name="members"></a><span data-ttu-id="5a355-111">Члены</span><span class="sxs-lookup"><span data-stu-id="5a355-111">Members</span></span>

<span data-ttu-id="5a355-112">Класс **\_ \_ Global02 брандмауэра MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5a355-112">The **MDM\_Firewall\_Global02** class has these types of members:</span></span>

-   [<span data-ttu-id="5a355-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="5a355-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5a355-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="5a355-114">Properties</span></span>

<span data-ttu-id="5a355-115">Класс **\_ \_ Global02 брандмауэра MDM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5a355-115">The **MDM\_Firewall\_Global02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5a355-116">бинариверсионсуппортед</span><span class="sxs-lookup"><span data-stu-id="5a355-116">BinaryVersionSupported</span></span>](/windows/client-management/mdm/firewall-csp#binaryversionsupported)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a355-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5a355-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a355-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5a355-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5a355-119">крлчекк</span><span class="sxs-lookup"><span data-stu-id="5a355-119">CRLcheck</span></span>](/windows/client-management/mdm/firewall-csp#crlcheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a355-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="5a355-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a355-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5a355-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5a355-122">куррентпрофилес</span><span class="sxs-lookup"><span data-stu-id="5a355-122">CurrentProfiles</span></span>](/windows/client-management/mdm/firewall-csp#currentprofiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a355-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="5a355-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a355-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5a355-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5a355-125">дисаблестатефулфтп</span><span class="sxs-lookup"><span data-stu-id="5a355-125">DisableStatefulFtp</span></span>](/windows/client-management/mdm/firewall-csp#disablestatefulftp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a355-126">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="5a355-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a355-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5a355-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5a355-128">енаблепаккеткуеуе</span><span class="sxs-lookup"><span data-stu-id="5a355-128">EnablePacketQueue</span></span>](/windows/client-management/mdm/firewall-csp#enablepacketqueue)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a355-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="5a355-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a355-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5a355-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5a355-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5a355-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a355-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5a355-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a355-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5a355-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a355-134">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5a355-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5a355-135">ипсецексемпт</span><span class="sxs-lookup"><span data-stu-id="5a355-135">IPsecExempt</span></span>](/windows/client-management/mdm/firewall-csp#ipsecexempt)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a355-136">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="5a355-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a355-137">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5a355-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5a355-138">оппортунистикаллиматчауссетперкм</span><span class="sxs-lookup"><span data-stu-id="5a355-138">OpportunisticallyMatchAuthSetPerKM</span></span>](/windows/client-management/mdm/firewall-csp#opportunisticallymatchauthsetperkm)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a355-139">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="5a355-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a355-140">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5a355-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5a355-141">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5a355-141">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a355-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5a355-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a355-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5a355-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a355-144">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5a355-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5a355-145">PolicyVersion</span><span class="sxs-lookup"><span data-stu-id="5a355-145">PolicyVersion</span></span>](/windows/client-management/mdm/firewall-csp#policyversion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a355-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5a355-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a355-147">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5a355-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5a355-148">полициверсионсуппортед</span><span class="sxs-lookup"><span data-stu-id="5a355-148">PolicyVersionSupported</span></span>](/windows/client-management/mdm/firewall-csp#policyversionsupported)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a355-149">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="5a355-149">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a355-150">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5a355-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5a355-151">прешаредкэйенкодинг</span><span class="sxs-lookup"><span data-stu-id="5a355-151">PresharedKeyEncoding</span></span>](/windows/client-management/mdm/firewall-csp#presharedkeyencoding)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a355-152">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="5a355-152">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a355-153">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5a355-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5a355-154">саидлетиме</span><span class="sxs-lookup"><span data-stu-id="5a355-154">SaIdleTime</span></span>](/windows/client-management/mdm/firewall-csp#saidletime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a355-155">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="5a355-155">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a355-156">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5a355-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a355-157">Требования</span><span class="sxs-lookup"><span data-stu-id="5a355-157">Requirements</span></span>



| <span data-ttu-id="5a355-158">Требование</span><span class="sxs-lookup"><span data-stu-id="5a355-158">Requirement</span></span> | <span data-ttu-id="5a355-159">Значение</span><span class="sxs-lookup"><span data-stu-id="5a355-159">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a355-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a355-160">Minimum supported client</span></span><br/> | <span data-ttu-id="5a355-161">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5a355-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5a355-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a355-162">Minimum supported server</span></span><br/> | <span data-ttu-id="5a355-163">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5a355-163">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="5a355-164">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5a355-164">Namespace</span></span><br/>                | <span data-ttu-id="5a355-165">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="5a355-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="5a355-166">MOF</span><span class="sxs-lookup"><span data-stu-id="5a355-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a355-167"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a355-167"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="5a355-168">DLL</span><span class="sxs-lookup"><span data-stu-id="5a355-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a355-169"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a355-169"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

