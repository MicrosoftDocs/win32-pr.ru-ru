---
title: Класс Win32_TSLicenseReportSummaryEntry
description: Содержит сводку по установленным и выпущенным службы удаленных рабочих столов клиентских лицензий на доступ для пользователей (RDS \ 160; CAL на пользователя).
ms.assetid: 0FD3BFFE-58B9-4037-969F-8C2323136C9D
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSLicenseReportSummaryEntry службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSLicenseReportSummaryEntry, описание
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportSummaryEntry
- Win32_TSLicenseReportSummaryEntry.ProductVersion
- Win32_TSLicenseReportSummaryEntry.ProductVersionID
- Win32_TSLicenseReportSummaryEntry.TSCALType
- Win32_TSLicenseReportSummaryEntry.InstalledLicenses
- Win32_TSLicenseReportSummaryEntry.IssuedLicenses
- Win32_TSLicenseReportSummaryEntry.TSCALAvailability
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f34482e9c6199ef6586024d43d586421a54071ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672485"
---
# <a name="win32_tslicensereportsummaryentry-class"></a><span data-ttu-id="6fdd1-105">\_Класс Win32 тслиценсерепортсуммарентри</span><span class="sxs-lookup"><span data-stu-id="6fdd1-105">Win32\_TSLicenseReportSummaryEntry class</span></span>

<span data-ttu-id="6fdd1-106">Содержит сводку по установленным и выпущенным службы удаленных рабочих столов клиентских лицензий на клиентские лицензии (RDS на пользователя).</span><span class="sxs-lookup"><span data-stu-id="6fdd1-106">Provides a summary of the installed and issued Remote Desktop Services Per User client access licenses (RDS Per User CALs).</span></span>

## <a name="syntax"></a><span data-ttu-id="6fdd1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6fdd1-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportSummaryEntry
{
  string ProductVersion;
  uint32 ProductVersionID;
  string TSCALType;
  uint32 InstalledLicenses;
  uint32 IssuedLicenses;
  string TSCALAvailability;
};
```

## <a name="members"></a><span data-ttu-id="6fdd1-108">Члены</span><span class="sxs-lookup"><span data-stu-id="6fdd1-108">Members</span></span>

<span data-ttu-id="6fdd1-109">Класс **Win32 \_ тслиценсерепортсуммарентри** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6fdd1-109">The **Win32\_TSLicenseReportSummaryEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="6fdd1-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="6fdd1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6fdd1-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="6fdd1-111">Properties</span></span>

<span data-ttu-id="6fdd1-112">Класс **Win32 \_ тслиценсерепортсуммарентри** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-112">The **Win32\_TSLicenseReportSummaryEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6fdd1-113">**инсталледлиценсес**</span><span class="sxs-lookup"><span data-stu-id="6fdd1-113">**InstalledLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fdd1-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fdd1-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fdd1-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6fdd1-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fdd1-116">Число установленных клиентских лицензий служб удаленных рабочих столов "на пользователя".</span><span class="sxs-lookup"><span data-stu-id="6fdd1-116">Number of RDS Per User CALs that are installed.</span></span>

</dd> <dt>

<span data-ttu-id="6fdd1-117">**иссуедлиценсес**</span><span class="sxs-lookup"><span data-stu-id="6fdd1-117">**IssuedLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fdd1-118">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fdd1-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fdd1-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6fdd1-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fdd1-120">Число выданных клиентских лицензий RDS "на пользователя".</span><span class="sxs-lookup"><span data-stu-id="6fdd1-120">Number of RDS Per User CALs that are issued.</span></span>

</dd> <dt>

<span data-ttu-id="6fdd1-121">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="6fdd1-121">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fdd1-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6fdd1-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fdd1-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6fdd1-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fdd1-124">Версия службы удаленных рабочих столов, для которой была выдана клиентская лицензия RDS "на пользователя".</span><span class="sxs-lookup"><span data-stu-id="6fdd1-124">Version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span>

<dt>

<span data-ttu-id="6fdd1-125">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="6fdd1-125">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="6fdd1-126">С этой лицензией поддерживаются только серверы под Windows Server 2012, Windows Server 2008 R2 или Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-126">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="6fdd1-127">Windows Server 7</span><span class="sxs-lookup"><span data-stu-id="6fdd1-127">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="6fdd1-128">С этой лицензией поддерживаются только серверы, работающие под Windows Server 2008 R2 или Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-128">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="6fdd1-129">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="6fdd1-129">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="6fdd1-130">С этой лицензией поддерживаются только серверы под под Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-130">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6fdd1-131">**продуктверсионид**</span><span class="sxs-lookup"><span data-stu-id="6fdd1-131">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fdd1-132">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fdd1-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fdd1-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6fdd1-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fdd1-134">Идентификатор версии продукта для службы удаленных рабочих столов пакета лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-134">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="6fdd1-135">4</span><span class="sxs-lookup"><span data-stu-id="6fdd1-135">4</span></span>
</dt> <dd>

<span data-ttu-id="6fdd1-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6fdd1-136">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="6fdd1-137">3</span><span class="sxs-lookup"><span data-stu-id="6fdd1-137">3</span></span>
</dt> <dd>

<span data-ttu-id="6fdd1-138">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6fdd1-138">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="6fdd1-139">2</span><span class="sxs-lookup"><span data-stu-id="6fdd1-139">2</span></span>
</dt> <dd>

<span data-ttu-id="6fdd1-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6fdd1-140">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="6fdd1-141">1</span><span class="sxs-lookup"><span data-stu-id="6fdd1-141">1</span></span>
</dt> <dd>

<span data-ttu-id="6fdd1-142">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-142">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="6fdd1-143">0</span><span class="sxs-lookup"><span data-stu-id="6fdd1-143">0</span></span>
</dt> <dd>

<span data-ttu-id="6fdd1-144">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-144">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6fdd1-145">**тскалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="6fdd1-145">**TSCALAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fdd1-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6fdd1-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fdd1-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6fdd1-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fdd1-148">Доступность клиентских лицензий RDS "на пользователя".</span><span class="sxs-lookup"><span data-stu-id="6fdd1-148">The availability of the RDS Per User CALs.</span></span> <span data-ttu-id="6fdd1-149">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-149">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="6fdd1-150">Имеющ</span><span class="sxs-lookup"><span data-stu-id="6fdd1-150">"Available"</span></span>
</dt> <dd>

<span data-ttu-id="6fdd1-151">Доступны клиентские лицензии RDS "на пользователя".</span><span class="sxs-lookup"><span data-stu-id="6fdd1-151">The RDS Per User CALs are available.</span></span>

</dd> <dt>

<span data-ttu-id="6fdd1-152">Ограничены</span><span class="sxs-lookup"><span data-stu-id="6fdd1-152">"Limited"</span></span>
</dt> <dd>

<span data-ttu-id="6fdd1-153">Доступность клиентских лицензий служб удаленных рабочих столов "на пользователя" ограничена.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-153">The availability of the RDS Per User CALs is limited.</span></span>

</dd> <dt>

<span data-ttu-id="6fdd1-154">"None"</span><span class="sxs-lookup"><span data-stu-id="6fdd1-154">"None"</span></span>
</dt> <dd>

<span data-ttu-id="6fdd1-155">Клиентские лицензии RDS "на пользователя" недоступны.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-155">The RDS Per User CALs are not available.</span></span>

</dd> <dt>

<span data-ttu-id="6fdd1-156">"Not Tracking"</span><span class="sxs-lookup"><span data-stu-id="6fdd1-156">"Not Tracking"</span></span>
</dt> <dd>

<span data-ttu-id="6fdd1-157">Доступность клиентских лицензий служб удаленных рабочих столов "на пользователя" не отслеживается.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-157">The availability of the RDS Per User CALs is not being tracked.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6fdd1-158">**тскалтипе**</span><span class="sxs-lookup"><span data-stu-id="6fdd1-158">**TSCALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fdd1-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6fdd1-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fdd1-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6fdd1-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fdd1-161">Тип клиентских лицензий служб удаленных рабочих столов "на пользователя".</span><span class="sxs-lookup"><span data-stu-id="6fdd1-161">The type of RDS Per User CALs.</span></span> <span data-ttu-id="6fdd1-162">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-162">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="6fdd1-163">"На устройство"</span><span class="sxs-lookup"><span data-stu-id="6fdd1-163">"Per Device"</span></span>
</dt> <dd>

<span data-ttu-id="6fdd1-164">Для каждого устройства выдаются клиентские лицензии RDS "на пользователя".</span><span class="sxs-lookup"><span data-stu-id="6fdd1-164">The RDS Per User CALs are issued per device.</span></span>

</dd> <dt>

<span data-ttu-id="6fdd1-165">"На пользователя"</span><span class="sxs-lookup"><span data-stu-id="6fdd1-165">"Per User"</span></span>
</dt> <dd>

<span data-ttu-id="6fdd1-166">Клиентские лицензии RDS "на пользователя" выдаются для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-166">The RDS Per User CALs are issued per user.</span></span>

</dd> <dt>

<span data-ttu-id="6fdd1-167">Неизвестный</span><span class="sxs-lookup"><span data-stu-id="6fdd1-167">"Unknown"</span></span>
</dt> <dd>

<span data-ttu-id="6fdd1-168">Тип клиентских лицензий служб удаленных рабочих столов "на пользователя" неизвестен.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-168">The type of RDS Per User CALs is unknown.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6fdd1-169">Требования</span><span class="sxs-lookup"><span data-stu-id="6fdd1-169">Requirements</span></span>



| <span data-ttu-id="6fdd1-170">Требование</span><span class="sxs-lookup"><span data-stu-id="6fdd1-170">Requirement</span></span> | <span data-ttu-id="6fdd1-171">Значение</span><span class="sxs-lookup"><span data-stu-id="6fdd1-171">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fdd1-172">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6fdd1-172">Minimum supported client</span></span><br/> | <span data-ttu-id="6fdd1-173">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6fdd1-173">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="6fdd1-174">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6fdd1-174">Minimum supported server</span></span><br/> | <span data-ttu-id="6fdd1-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6fdd1-175">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="6fdd1-176">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6fdd1-176">Namespace</span></span><br/>                | <span data-ttu-id="6fdd1-177">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="6fdd1-177">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="6fdd1-178">MOF</span><span class="sxs-lookup"><span data-stu-id="6fdd1-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6fdd1-179"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6fdd1-179"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6fdd1-180">DLL</span><span class="sxs-lookup"><span data-stu-id="6fdd1-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fdd1-181"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fdd1-181"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



 

 





