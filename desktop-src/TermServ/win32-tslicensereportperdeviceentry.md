---
title: Класс Win32_TSLicenseReportPerDeviceEntry
description: Содержит сведения о неудачном службы удаленных рабочих столов клиентской лицензии на устройство (RDS \ 160; CAL на устройство).
ms.assetid: b26f2518-439c-4562-9492-a0cfa60c457a
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSLicenseReportPerDeviceEntry службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSLicenseReportPerDeviceEntry, описание
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportPerDeviceEntry
- Win32_TSLicenseReportPerDeviceEntry.sIssuedToComputer
- Win32_TSLicenseReportPerDeviceEntry.sHardwareId
- Win32_TSLicenseReportPerDeviceEntry.ExpirationDate
- Win32_TSLicenseReportPerDeviceEntry.CALType
- Win32_TSLicenseReportPerDeviceEntry.ProductVersion
- Win32_TSLicenseReportPerDeviceEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a120d477ff03675f160d94f1506f59cdf1462fa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489354"
---
# <a name="win32_tslicensereportperdeviceentry-class"></a><span data-ttu-id="cdf67-105">\_Класс Win32 тслиценсерепортпердевицеентри</span><span class="sxs-lookup"><span data-stu-id="cdf67-105">Win32\_TSLicenseReportPerDeviceEntry class</span></span>

<span data-ttu-id="cdf67-106">Содержит сведения о неудачном службы удаленных рабочих столов клиентской лицензии для каждого устройства (клиентская лицензия RDS на устройство).</span><span class="sxs-lookup"><span data-stu-id="cdf67-106">Provides details about the failed Remote Desktop Services Per Device client access license (RDS Per Device CAL).</span></span>

<span data-ttu-id="cdf67-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="cdf67-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdf67-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cdf67-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportPerDeviceEntry
{
  string   sIssuedToComputer;
  string   sHardwareId;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a><span data-ttu-id="cdf67-109">Члены</span><span class="sxs-lookup"><span data-stu-id="cdf67-109">Members</span></span>

<span data-ttu-id="cdf67-110">Класс **Win32 \_ тслиценсерепортпердевицеентри** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cdf67-110">The **Win32\_TSLicenseReportPerDeviceEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="cdf67-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="cdf67-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cdf67-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="cdf67-112">Properties</span></span>

<span data-ttu-id="cdf67-113">Класс **Win32 \_ тслиценсерепортпердевицеентри** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cdf67-113">The **Win32\_TSLicenseReportPerDeviceEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cdf67-114">**калтипе**</span><span class="sxs-lookup"><span data-stu-id="cdf67-114">**CALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf67-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cdf67-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdf67-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cdf67-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdf67-117">Указывает тип выданной лицензии CAL.</span><span class="sxs-lookup"><span data-stu-id="cdf67-117">Specifies the type of CAL issued.</span></span> <span data-ttu-id="cdf67-118">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="cdf67-118">This will be one of the following values.</span></span>

<span data-ttu-id="cdf67-119">"Встроенная клиентская лицензия служб терминалов" на устройство "</span><span class="sxs-lookup"><span data-stu-id="cdf67-119">"Built-in TS Per Device CAL"</span></span>

<span data-ttu-id="cdf67-120">"Клиентская лицензия" TS per Device "</span><span class="sxs-lookup"><span data-stu-id="cdf67-120">"TS Per Device CAL"</span></span>

<span data-ttu-id="cdf67-121">"Клиентская лицензия TS подключателя к Интернету"</span><span class="sxs-lookup"><span data-stu-id="cdf67-121">"TS Internet Connector CAL"</span></span>

<span data-ttu-id="cdf67-122">"TS CAL на пользователя"</span><span class="sxs-lookup"><span data-stu-id="cdf67-122">"TS Per User CAL"</span></span>

<span data-ttu-id="cdf67-123">"TS или RDS per Device CAL"</span><span class="sxs-lookup"><span data-stu-id="cdf67-123">"TS or RDS Per Device CAL"</span></span>

<span data-ttu-id="cdf67-124">Клиентские лицензии TS или RDS на пользователя</span><span class="sxs-lookup"><span data-stu-id="cdf67-124">"TS or RDS Per User CAL"</span></span>

<span data-ttu-id="cdf67-125">Лицензия "Стандартный набор VDI Standard Suite для подписки устройств"</span><span class="sxs-lookup"><span data-stu-id="cdf67-125">"VDI Standard Suite Per Device subscription license"</span></span>

<span data-ttu-id="cdf67-126">Лицензия "VDI Premium Suite с подпиской на устройство"</span><span class="sxs-lookup"><span data-stu-id="cdf67-126">"VDI Premium Suite Per Device subscription license"</span></span>

<span data-ttu-id="cdf67-127">"RDS per Device CAL"</span><span class="sxs-lookup"><span data-stu-id="cdf67-127">"RDS Per Device CAL"</span></span>

<span data-ttu-id="cdf67-128">"RDS на пользователя CAL"</span><span class="sxs-lookup"><span data-stu-id="cdf67-128">"RDS Per User CAL"</span></span>

</dd> <dt>

<span data-ttu-id="cdf67-129">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="cdf67-129">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf67-130">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cdf67-130">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="cdf67-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cdf67-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdf67-132">Дата окончания срока действия лицензии.</span><span class="sxs-lookup"><span data-stu-id="cdf67-132">The expiration date of the license.</span></span>

</dd> <dt>

<span data-ttu-id="cdf67-133">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="cdf67-133">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf67-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cdf67-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdf67-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cdf67-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdf67-136">Версия службы удаленных рабочих столов, для которой была выдана клиентская лицензия RDS на пользователя.</span><span class="sxs-lookup"><span data-stu-id="cdf67-136">The version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span> <span data-ttu-id="cdf67-137">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="cdf67-137">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="cdf67-138">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="cdf67-138">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="cdf67-139">С этой лицензией поддерживаются только серверы под Windows Server 2012, Windows Server 2008 R2 или Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="cdf67-139">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="cdf67-140">Windows Server 7</span><span class="sxs-lookup"><span data-stu-id="cdf67-140">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="cdf67-141">С этой лицензией поддерживаются только серверы, работающие под Windows Server 2008 R2 или Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="cdf67-141">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="cdf67-142">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="cdf67-142">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="cdf67-143">С этой лицензией поддерживаются только серверы под под Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="cdf67-143">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cdf67-144">**продуктверсионид**</span><span class="sxs-lookup"><span data-stu-id="cdf67-144">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf67-145">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cdf67-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cdf67-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cdf67-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdf67-147">Идентификатор версии продукта для службы удаленных рабочих столов пакета лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="cdf67-147">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="cdf67-148">4</span><span class="sxs-lookup"><span data-stu-id="cdf67-148">4</span></span>
</dt> <dd>

<span data-ttu-id="cdf67-149">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cdf67-149">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="cdf67-150">3</span><span class="sxs-lookup"><span data-stu-id="cdf67-150">3</span></span>
</dt> <dd>

<span data-ttu-id="cdf67-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cdf67-151">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="cdf67-152">2</span><span class="sxs-lookup"><span data-stu-id="cdf67-152">2</span></span>
</dt> <dd>

<span data-ttu-id="cdf67-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cdf67-153">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="cdf67-154">1</span><span class="sxs-lookup"><span data-stu-id="cdf67-154">1</span></span>
</dt> <dd>

<span data-ttu-id="cdf67-155">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cdf67-155">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="cdf67-156">0</span><span class="sxs-lookup"><span data-stu-id="cdf67-156">0</span></span>
</dt> <dd>

<span data-ttu-id="cdf67-157">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cdf67-157">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cdf67-158">**шардвареид**</span><span class="sxs-lookup"><span data-stu-id="cdf67-158">**sHardwareId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf67-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cdf67-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdf67-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cdf67-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdf67-161">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cdf67-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cdf67-162">Идентификатор оборудования компьютера.</span><span class="sxs-lookup"><span data-stu-id="cdf67-162">The hardware identifier of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="cdf67-163">**сиссуедтокомпутер**</span><span class="sxs-lookup"><span data-stu-id="cdf67-163">**sIssuedToComputer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf67-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cdf67-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdf67-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cdf67-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdf67-166">Имя компьютера, для которого предпринималась попытка выдачи лицензии.</span><span class="sxs-lookup"><span data-stu-id="cdf67-166">The name of the computer that the license issuance was attempted for.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cdf67-167">Требования</span><span class="sxs-lookup"><span data-stu-id="cdf67-167">Requirements</span></span>



| <span data-ttu-id="cdf67-168">Требование</span><span class="sxs-lookup"><span data-stu-id="cdf67-168">Requirement</span></span> | <span data-ttu-id="cdf67-169">Значение</span><span class="sxs-lookup"><span data-stu-id="cdf67-169">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdf67-170">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cdf67-170">Minimum supported client</span></span><br/> | <span data-ttu-id="cdf67-171">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cdf67-171">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="cdf67-172">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cdf67-172">Minimum supported server</span></span><br/> | <span data-ttu-id="cdf67-173">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cdf67-173">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="cdf67-174">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cdf67-174">Namespace</span></span><br/>                | <span data-ttu-id="cdf67-175">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="cdf67-175">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="cdf67-176">MOF</span><span class="sxs-lookup"><span data-stu-id="cdf67-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cdf67-177"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cdf67-177"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cdf67-178">DLL</span><span class="sxs-lookup"><span data-stu-id="cdf67-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdf67-179"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdf67-179"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdf67-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cdf67-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdf67-181">**фетчрепортпердевицеентриес**</span><span class="sxs-lookup"><span data-stu-id="cdf67-181">**FetchReportPerDeviceEntries**</span></span>](fetchreportperdeviceentries-win32-tslicensereport.md)
</dt> </dl>

 

