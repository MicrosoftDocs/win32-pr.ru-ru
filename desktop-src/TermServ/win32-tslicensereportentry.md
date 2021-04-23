---
title: Класс Win32_TSLicenseReportEntry
description: Содержит сведения о выданной службы удаленных рабочих столов клиентской лицензии для каждого пользователя (RDS \ 160; CAL на пользователя).
ms.assetid: 75fa7f39-af5b-45a0-ba2b-5c667edfec16
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSLicenseReportEntry службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSLicenseReportEntry, описание
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportEntry
- Win32_TSLicenseReportEntry.User
- Win32_TSLicenseReportEntry.ExpirationDate
- Win32_TSLicenseReportEntry.CALType
- Win32_TSLicenseReportEntry.ProductVersion
- Win32_TSLicenseReportEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44fa97a91561a9d4cf3fd571c773288796754858
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414828"
---
# <a name="win32_tslicensereportentry-class"></a><span data-ttu-id="e3338-105">\_Класс Win32 тслиценсерепортентри</span><span class="sxs-lookup"><span data-stu-id="e3338-105">Win32\_TSLicenseReportEntry class</span></span>

<span data-ttu-id="e3338-106">Содержит сведения о выданной службы удаленных рабочих столов клиентской лицензии для каждого пользователя (клиентские лицензии служб удаленных рабочих столов на пользователя).</span><span class="sxs-lookup"><span data-stu-id="e3338-106">Provides details of the issued Remote Desktop Services Per User client access license (RDS Per User CAL).</span></span>

## <a name="syntax"></a><span data-ttu-id="e3338-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3338-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportEntry
{
  string   User;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a><span data-ttu-id="e3338-108">Члены</span><span class="sxs-lookup"><span data-stu-id="e3338-108">Members</span></span>

<span data-ttu-id="e3338-109">Класс **Win32 \_ тслиценсерепортентри** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e3338-109">The **Win32\_TSLicenseReportEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="e3338-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="e3338-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e3338-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="e3338-111">Properties</span></span>

<span data-ttu-id="e3338-112">Класс **Win32 \_ тслиценсерепортентри** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e3338-112">The **Win32\_TSLicenseReportEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e3338-113">**калтипе**</span><span class="sxs-lookup"><span data-stu-id="e3338-113">**CALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3338-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e3338-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3338-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3338-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3338-116">Указывает тип выданной лицензии CAL.</span><span class="sxs-lookup"><span data-stu-id="e3338-116">Specifies the type of CAL issued.</span></span> <span data-ttu-id="e3338-117">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e3338-117">This will be one of the following values.</span></span>

<span data-ttu-id="e3338-118">**Windows server 2008 R2 и Windows server 2008:** Это свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e3338-118">**Windows Server 2008 R2 and Windows Server 2008:** This property is not supported.</span></span>

<span data-ttu-id="e3338-119">"Встроенная клиентская лицензия служб терминалов" на устройство "</span><span class="sxs-lookup"><span data-stu-id="e3338-119">"Built-in TS Per Device CAL"</span></span>

<span data-ttu-id="e3338-120">"Клиентская лицензия" TS per Device "</span><span class="sxs-lookup"><span data-stu-id="e3338-120">"TS Per Device CAL"</span></span>

<span data-ttu-id="e3338-121">"Клиентская лицензия TS подключателя к Интернету"</span><span class="sxs-lookup"><span data-stu-id="e3338-121">"TS Internet Connector CAL"</span></span>

<span data-ttu-id="e3338-122">"TS CAL на пользователя"</span><span class="sxs-lookup"><span data-stu-id="e3338-122">"TS Per User CAL"</span></span>

<span data-ttu-id="e3338-123">"TS или RDS per Device CAL"</span><span class="sxs-lookup"><span data-stu-id="e3338-123">"TS or RDS Per Device CAL"</span></span>

<span data-ttu-id="e3338-124">Клиентские лицензии TS или RDS на пользователя</span><span class="sxs-lookup"><span data-stu-id="e3338-124">"TS or RDS Per User CAL"</span></span>

<span data-ttu-id="e3338-125">Лицензия "Стандартный набор VDI Standard Suite для подписки устройств"</span><span class="sxs-lookup"><span data-stu-id="e3338-125">"VDI Standard Suite Per Device subscription license"</span></span>

<span data-ttu-id="e3338-126">Лицензия "VDI Premium Suite с подпиской на устройство"</span><span class="sxs-lookup"><span data-stu-id="e3338-126">"VDI Premium Suite Per Device subscription license"</span></span>

<span data-ttu-id="e3338-127">"RDS per Device CAL"</span><span class="sxs-lookup"><span data-stu-id="e3338-127">"RDS Per Device CAL"</span></span>

<span data-ttu-id="e3338-128">"RDS на пользователя CAL"</span><span class="sxs-lookup"><span data-stu-id="e3338-128">"RDS Per User CAL"</span></span>

</dd> <dt>

<span data-ttu-id="e3338-129">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="e3338-129">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3338-130">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e3338-130">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="e3338-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3338-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3338-132">Дата окончания срока действия лицензии, выданной пользователю.</span><span class="sxs-lookup"><span data-stu-id="e3338-132">Expiration date of the license that was issued to the user.</span></span>

</dd> <dt>

<span data-ttu-id="e3338-133">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="e3338-133">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3338-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e3338-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3338-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3338-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3338-136">Версия службы удаленных рабочих столов, для которой была выдана клиентская лицензия RDS "на пользователя".</span><span class="sxs-lookup"><span data-stu-id="e3338-136">Version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span>

<dt>

<span data-ttu-id="e3338-137">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="e3338-137">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="e3338-138">С этой лицензией поддерживаются только серверы под Windows Server 2012, Windows Server 2008 R2 или Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e3338-138">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="e3338-139">Windows Server 7</span><span class="sxs-lookup"><span data-stu-id="e3338-139">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="e3338-140">С этой лицензией поддерживаются только серверы, работающие под Windows Server 2008 R2 или Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e3338-140">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="e3338-141">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="e3338-141">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="e3338-142">С этой лицензией поддерживаются только серверы под под Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e3338-142">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e3338-143">**продуктверсионид**</span><span class="sxs-lookup"><span data-stu-id="e3338-143">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3338-144">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e3338-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e3338-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3338-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3338-146">Идентификатор версии продукта для службы удаленных рабочих столов пакета лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="e3338-146">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="e3338-147">4</span><span class="sxs-lookup"><span data-stu-id="e3338-147">4</span></span>
</dt> <dd>

<span data-ttu-id="e3338-148">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e3338-148">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="e3338-149">3</span><span class="sxs-lookup"><span data-stu-id="e3338-149">3</span></span>
</dt> <dd>

<span data-ttu-id="e3338-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e3338-150">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="e3338-151">2</span><span class="sxs-lookup"><span data-stu-id="e3338-151">2</span></span>
</dt> <dd>

<span data-ttu-id="e3338-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3338-152">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="e3338-153">1</span><span class="sxs-lookup"><span data-stu-id="e3338-153">1</span></span>
</dt> <dd>

<span data-ttu-id="e3338-154">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e3338-154">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="e3338-155">0</span><span class="sxs-lookup"><span data-stu-id="e3338-155">0</span></span>
</dt> <dd>

<span data-ttu-id="e3338-156">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e3338-156">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e3338-157">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="e3338-157">**User**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3338-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e3338-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3338-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3338-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3338-160">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e3338-160">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e3338-161">Имя пользователя, которому была выдана лицензия.</span><span class="sxs-lookup"><span data-stu-id="e3338-161">Name of the user to whom the license was issued.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3338-162">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3338-162">Remarks</span></span>

<span data-ttu-id="e3338-163">Для использования этого класса необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="e3338-163">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="e3338-164">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="e3338-164">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e3338-165">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="e3338-165">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e3338-166">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="e3338-166">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e3338-167">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e3338-167">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3338-168">Требования</span><span class="sxs-lookup"><span data-stu-id="e3338-168">Requirements</span></span>



| <span data-ttu-id="e3338-169">Требование</span><span class="sxs-lookup"><span data-stu-id="e3338-169">Requirement</span></span> | <span data-ttu-id="e3338-170">Значение</span><span class="sxs-lookup"><span data-stu-id="e3338-170">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3338-171">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3338-171">Minimum supported client</span></span><br/> | <span data-ttu-id="e3338-172">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e3338-172">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="e3338-173">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3338-173">Minimum supported server</span></span><br/> | <span data-ttu-id="e3338-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3338-174">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="e3338-175">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e3338-175">Namespace</span></span><br/>                | <span data-ttu-id="e3338-176">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="e3338-176">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="e3338-177">MOF</span><span class="sxs-lookup"><span data-stu-id="e3338-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3338-178"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3338-178"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3338-179">DLL</span><span class="sxs-lookup"><span data-stu-id="e3338-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3338-180"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3338-180"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3338-181">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3338-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3338-182">**фетчрепортентриес**</span><span class="sxs-lookup"><span data-stu-id="e3338-182">**FetchReportEntries**</span></span>](fetchreportentries-win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="e3338-183">**\_Тсиссуедлиценсе Win32**</span><span class="sxs-lookup"><span data-stu-id="e3338-183">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="e3338-184">**\_Тслиценсекэйпакк Win32**</span><span class="sxs-lookup"><span data-stu-id="e3338-184">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="e3338-185">**\_Тслиценсерепорт Win32**</span><span class="sxs-lookup"><span data-stu-id="e3338-185">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="e3338-186">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="e3338-186">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

