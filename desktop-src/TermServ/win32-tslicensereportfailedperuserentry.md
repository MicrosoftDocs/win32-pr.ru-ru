---
title: Класс Win32_TSLicenseReportFailedPerUserEntry
description: Содержит сведения о неудачном службы удаленных рабочих столов клиентской лицензии на пользователя (RDS \ 160; CAL на пользователя).
ms.assetid: 27d155a4-938e-4bca-8d15-03c44740e506
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSLicenseReportFailedPerUserEntry службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSLicenseReportFailedPerUserEntry, описание
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserEntry
- Win32_TSLicenseReportFailedPerUserEntry.User
- Win32_TSLicenseReportFailedPerUserEntry.TriedIssuanceOn
- Win32_TSLicenseReportFailedPerUserEntry.CALType
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersion
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18098ce0510a39f6083edcf688a18c10a3e20278
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414825"
---
# <a name="win32_tslicensereportfailedperuserentry-class"></a><span data-ttu-id="006d7-105">\_Класс Win32 тслиценсерепортфаиледперусерентри</span><span class="sxs-lookup"><span data-stu-id="006d7-105">Win32\_TSLicenseReportFailedPerUserEntry class</span></span>

<span data-ttu-id="006d7-106">Содержит сведения о неудачном службы удаленных рабочих столов клиентской лицензии на пользователя (RDS на пользователя CAL).</span><span class="sxs-lookup"><span data-stu-id="006d7-106">Provides details about the failed Remote Desktop Services Per User client access license (RDS Per User CAL).</span></span>

<span data-ttu-id="006d7-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="006d7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="006d7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="006d7-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserEntry
{
  string   User;
  DATETIME TriedIssuanceOn;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a><span data-ttu-id="006d7-109">Члены</span><span class="sxs-lookup"><span data-stu-id="006d7-109">Members</span></span>

<span data-ttu-id="006d7-110">Класс **Win32 \_ тслиценсерепортфаиледперусерентри** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="006d7-110">The **Win32\_TSLicenseReportFailedPerUserEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="006d7-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="006d7-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="006d7-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="006d7-112">Properties</span></span>

<span data-ttu-id="006d7-113">Класс **Win32 \_ тслиценсерепортфаиледперусерентри** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="006d7-113">The **Win32\_TSLicenseReportFailedPerUserEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="006d7-114">**калтипе**</span><span class="sxs-lookup"><span data-stu-id="006d7-114">**CALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="006d7-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="006d7-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="006d7-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="006d7-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="006d7-117">Указывает тип выданной лицензии CAL.</span><span class="sxs-lookup"><span data-stu-id="006d7-117">Specifies the type of CAL issued.</span></span> <span data-ttu-id="006d7-118">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="006d7-118">This will be one of the following values.</span></span>

<span data-ttu-id="006d7-119">"Встроенная клиентская лицензия служб терминалов" на устройство "</span><span class="sxs-lookup"><span data-stu-id="006d7-119">"Built-in TS Per Device CAL"</span></span>

<span data-ttu-id="006d7-120">"Клиентская лицензия" TS per Device "</span><span class="sxs-lookup"><span data-stu-id="006d7-120">"TS Per Device CAL"</span></span>

<span data-ttu-id="006d7-121">"Клиентская лицензия TS подключателя к Интернету"</span><span class="sxs-lookup"><span data-stu-id="006d7-121">"TS Internet Connector CAL"</span></span>

<span data-ttu-id="006d7-122">"TS CAL на пользователя"</span><span class="sxs-lookup"><span data-stu-id="006d7-122">"TS Per User CAL"</span></span>

<span data-ttu-id="006d7-123">"TS или RDS per Device CAL"</span><span class="sxs-lookup"><span data-stu-id="006d7-123">"TS or RDS Per Device CAL"</span></span>

<span data-ttu-id="006d7-124">Клиентские лицензии TS или RDS на пользователя</span><span class="sxs-lookup"><span data-stu-id="006d7-124">"TS or RDS Per User CAL"</span></span>

<span data-ttu-id="006d7-125">Лицензия "Стандартный набор VDI Standard Suite для подписки устройств"</span><span class="sxs-lookup"><span data-stu-id="006d7-125">"VDI Standard Suite Per Device subscription license"</span></span>

<span data-ttu-id="006d7-126">Лицензия "VDI Premium Suite с подпиской на устройство"</span><span class="sxs-lookup"><span data-stu-id="006d7-126">"VDI Premium Suite Per Device subscription license"</span></span>

<span data-ttu-id="006d7-127">"RDS per Device CAL"</span><span class="sxs-lookup"><span data-stu-id="006d7-127">"RDS Per Device CAL"</span></span>

<span data-ttu-id="006d7-128">"RDS на пользователя CAL"</span><span class="sxs-lookup"><span data-stu-id="006d7-128">"RDS Per User CAL"</span></span>

</dd> <dt>

<span data-ttu-id="006d7-129">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="006d7-129">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="006d7-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="006d7-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="006d7-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="006d7-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="006d7-132">Версия службы удаленных рабочих столов, для которой была выдана клиентская лицензия RDS на пользователя.</span><span class="sxs-lookup"><span data-stu-id="006d7-132">The version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span> <span data-ttu-id="006d7-133">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="006d7-133">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="006d7-134">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="006d7-134">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="006d7-135">С этой лицензией поддерживаются только серверы под Windows Server 2012, Windows Server 2008 R2 или Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="006d7-135">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="006d7-136">Windows Server 7</span><span class="sxs-lookup"><span data-stu-id="006d7-136">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="006d7-137">С этой лицензией поддерживаются только серверы, работающие под Windows Server 2008 R2 или Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="006d7-137">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="006d7-138">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="006d7-138">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="006d7-139">С этой лицензией поддерживаются только серверы под под Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="006d7-139">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="006d7-140">**продуктверсионид**</span><span class="sxs-lookup"><span data-stu-id="006d7-140">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="006d7-141">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="006d7-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="006d7-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="006d7-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="006d7-143">Идентификатор версии продукта для службы удаленных рабочих столов пакета лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="006d7-143">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="006d7-144">4</span><span class="sxs-lookup"><span data-stu-id="006d7-144">4</span></span>
</dt> <dd>

<span data-ttu-id="006d7-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="006d7-145">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="006d7-146">3</span><span class="sxs-lookup"><span data-stu-id="006d7-146">3</span></span>
</dt> <dd>

<span data-ttu-id="006d7-147">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="006d7-147">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="006d7-148">2</span><span class="sxs-lookup"><span data-stu-id="006d7-148">2</span></span>
</dt> <dd>

<span data-ttu-id="006d7-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="006d7-149">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="006d7-150">1</span><span class="sxs-lookup"><span data-stu-id="006d7-150">1</span></span>
</dt> <dd>

<span data-ttu-id="006d7-151">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="006d7-151">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="006d7-152">0</span><span class="sxs-lookup"><span data-stu-id="006d7-152">0</span></span>
</dt> <dd>

<span data-ttu-id="006d7-153">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="006d7-153">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="006d7-154">**триедиссуанцеон**</span><span class="sxs-lookup"><span data-stu-id="006d7-154">**TriedIssuanceOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="006d7-155">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="006d7-155">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="006d7-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="006d7-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="006d7-157">Дата попыток выдачи лицензии.</span><span class="sxs-lookup"><span data-stu-id="006d7-157">The date on which license issuance was attempted.</span></span>

</dd> <dt>

<span data-ttu-id="006d7-158">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="006d7-158">**User**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="006d7-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="006d7-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="006d7-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="006d7-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="006d7-161">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="006d7-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="006d7-162">Имя пользователя, которому предпринималась попытка выдачи лицензии.</span><span class="sxs-lookup"><span data-stu-id="006d7-162">The name of the user to whom the license issuance was attempted.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="006d7-163">Требования</span><span class="sxs-lookup"><span data-stu-id="006d7-163">Requirements</span></span>



| <span data-ttu-id="006d7-164">Требование</span><span class="sxs-lookup"><span data-stu-id="006d7-164">Requirement</span></span> | <span data-ttu-id="006d7-165">Значение</span><span class="sxs-lookup"><span data-stu-id="006d7-165">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="006d7-166">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="006d7-166">Minimum supported client</span></span><br/> | <span data-ttu-id="006d7-167">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="006d7-167">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="006d7-168">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="006d7-168">Minimum supported server</span></span><br/> | <span data-ttu-id="006d7-169">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="006d7-169">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="006d7-170">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="006d7-170">Namespace</span></span><br/>                | <span data-ttu-id="006d7-171">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="006d7-171">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="006d7-172">MOF</span><span class="sxs-lookup"><span data-stu-id="006d7-172">MOF</span></span><br/>                      | <dl> <span data-ttu-id="006d7-173"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="006d7-173"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="006d7-174">DLL</span><span class="sxs-lookup"><span data-stu-id="006d7-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="006d7-175"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="006d7-175"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="006d7-176">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="006d7-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="006d7-177">**фетчрепортфаиледперусерентриес**</span><span class="sxs-lookup"><span data-stu-id="006d7-177">**FetchReportFailedPerUserEntries**</span></span>](fetchreportfailedperuserentries-win32-tslicensereport.md)
</dt> </dl>

 

