---
title: Класс Win32_TSLicenseReport
description: Предоставляет экземпляры клиентской лицензии службы удаленных рабочих столов на пользователя (RDS \ 160; Отчеты об использовании CAL "на пользователя", созданные на сервере лицензий удаленный рабочий стол, а также методы создания, выборки и удаления отчетов по лицензиям.
ms.assetid: 8d67f158-cda3-4cf4-a766-09d08c21c49e
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSLicenseReport службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSLicenseReport, описание
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport
- Win32_TSLicenseReport.FileName
- Win32_TSLicenseReport.LicenseUsageCount
- Win32_TSLicenseReport.InstalledLicenses
- Win32_TSLicenseReport.GenerationDateTime
- Win32_TSLicenseReport.ScopeType
- Win32_TSLicenseReport.ScopeValue
- Win32_TSLicenseReport.Version
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de997056222c1b525253f320f6fe191f017614f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891529"
---
# <a name="win32_tslicensereport-class"></a><span data-ttu-id="ca005-105">\_Класс Win32 тслиценсерепорт</span><span class="sxs-lookup"><span data-stu-id="ca005-105">Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="ca005-106">Содержит экземпляры службы удаленных рабочих столов клиентских лицензий (RDS на пользователя), созданных на сервере лицензирования удаленный рабочий стол, а также методы создания, получения и удаления отчетов по лицензиям.</span><span class="sxs-lookup"><span data-stu-id="ca005-106">Provides instances of Remote Desktop Services Per User client access license (RDS Per User CAL) usage reports that are generated on the Remote Desktop license server, and methods for license report generation, fetch, and delete operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca005-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca005-107">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseReport
{
  string   FileName;
  uint32   LicenseUsageCount;
  uint32   InstalledLicenses;
  DATETIME GenerationDateTime;
  uint32   ScopeType;
  string   ScopeValue;
  uint32   Version;
};
```

## <a name="members"></a><span data-ttu-id="ca005-108">Члены</span><span class="sxs-lookup"><span data-stu-id="ca005-108">Members</span></span>

<span data-ttu-id="ca005-109">Класс **Win32 \_ тслиценсерепорт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ca005-109">The **Win32\_TSLicenseReport** class has these types of members:</span></span>

-   [<span data-ttu-id="ca005-110">Методы</span><span class="sxs-lookup"><span data-stu-id="ca005-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ca005-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="ca005-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ca005-112">Методы</span><span class="sxs-lookup"><span data-stu-id="ca005-112">Methods</span></span>

<span data-ttu-id="ca005-113">Класс **Win32 \_ тслиценсерепорт** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ca005-113">The **Win32\_TSLicenseReport** class has these methods.</span></span>



| <span data-ttu-id="ca005-114">Метод</span><span class="sxs-lookup"><span data-stu-id="ca005-114">Method</span></span>                                                                                                         | <span data-ttu-id="ca005-115">Описание</span><span class="sxs-lookup"><span data-stu-id="ca005-115">Description</span></span>                                                                                                                                                                                     |
|:---------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca005-116">**DeleteReport**</span><span class="sxs-lookup"><span data-stu-id="ca005-116">**DeleteReport**</span></span>](deletereport-win32-tslicensereport.md)                                                     | <span data-ttu-id="ca005-117">Удаляет объект отчета на сервере лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="ca005-117">Deletes a report object on the Remote Desktop license server.</span></span> <span data-ttu-id="ca005-118">Это не статический метод.</span><span class="sxs-lookup"><span data-stu-id="ca005-118">This is not a static method.</span></span><br/>                                                                                           |
| [<span data-ttu-id="ca005-119">**фетчрепортентриес**</span><span class="sxs-lookup"><span data-stu-id="ca005-119">**FetchReportEntries**</span></span>](fetchreportentries-win32-tslicensereport.md)                                         | <span data-ttu-id="ca005-120">Извлекает записи в объекте отчета.</span><span class="sxs-lookup"><span data-stu-id="ca005-120">Retrieves entries in the report object.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="ca005-121">**фетчрепортфаиледперусерентриес**</span><span class="sxs-lookup"><span data-stu-id="ca005-121">**FetchReportFailedPerUserEntries**</span></span>](fetchreportfailedperuserentries-win32-tslicensereport.md)               | <span data-ttu-id="ca005-122">Получает сведения о неудачных службы удаленных рабочих столов клиентских лицензиях на клиентские лицензии (RDS на пользователя) из отчета.</span><span class="sxs-lookup"><span data-stu-id="ca005-122">Retrieves details of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span><br/>                                                             |
| [<span data-ttu-id="ca005-123">**фетчрепортфаиледперусерсуммарентриес**</span><span class="sxs-lookup"><span data-stu-id="ca005-123">**FetchReportFailedPerUserSummaryEntries**</span></span>](fetchreportfailedperusersummaryentries-win32-tslicensereport.md) | <span data-ttu-id="ca005-124">Получение сводных данных о неудачных службы удаленных рабочих столов клиентских лицензиях на клиентские лицензии (RDS на пользователя) из отчета.</span><span class="sxs-lookup"><span data-stu-id="ca005-124">Retrieves summary information of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span><br/>                                                 |
| [<span data-ttu-id="ca005-125">**фетчрепортпердевицеентриес**</span><span class="sxs-lookup"><span data-stu-id="ca005-125">**FetchReportPerDeviceEntries**</span></span>](fetchreportperdeviceentries-win32-tslicensereport.md)                       | <span data-ttu-id="ca005-126">Получение сведений о выданных лицензиях на клиентский доступ службы удаленных рабочих столов для каждого устройства (клиентские лицензии служб удаленных рабочих столов на устройство) из отчета.</span><span class="sxs-lookup"><span data-stu-id="ca005-126">Retrieves information of issued Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) from the report.</span></span><br/>                                                     |
| [<span data-ttu-id="ca005-127">**фетчрепортсуммарентриес**</span><span class="sxs-lookup"><span data-stu-id="ca005-127">**FetchReportSummaryEntries**</span></span>](win32-tslicensereport-fetchreportsummaryentries.md)                           | <span data-ttu-id="ca005-128">Извлекает сводки лицензий из объекта отчета.</span><span class="sxs-lookup"><span data-stu-id="ca005-128">Retrieves license summaries from the report object.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="ca005-129">**Создание отчета.**</span><span class="sxs-lookup"><span data-stu-id="ca005-129">**GenerateReport**</span></span>](generatereport-win32-tslicensereport.md)                                                 | <span data-ttu-id="ca005-130">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ca005-130">This method is not supported.</span></span><br/> <span data-ttu-id="ca005-131">**Windows server 2008 R2 и Windows server 2008:** Формирует текущий отчет об использовании лицензий на пользователя на сервере лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="ca005-131">**Windows Server 2008 R2 and Windows Server 2008:** Generates a current per user license usage report on the Remote Desktop license server.</span></span><br/> |
| [<span data-ttu-id="ca005-132">**женератерепортекс**</span><span class="sxs-lookup"><span data-stu-id="ca005-132">**GenerateReportEx**</span></span>](generatereportex-win32-tslicensereport.md)                                             | <span data-ttu-id="ca005-133">Формирует текущий отчет об использовании лицензий на пользователя на сервере лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="ca005-133">Generates a current per user license usage report on the Remote Desktop license server.</span></span><br/>                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="ca005-134">Свойства</span><span class="sxs-lookup"><span data-stu-id="ca005-134">Properties</span></span>

<span data-ttu-id="ca005-135">Класс **Win32 \_ тслиценсерепорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ca005-135">The **Win32\_TSLicenseReport** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ca005-136">**FileName**</span><span class="sxs-lookup"><span data-stu-id="ca005-136">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca005-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca005-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca005-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca005-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca005-139">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ca005-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ca005-140">Имя отчета.</span><span class="sxs-lookup"><span data-stu-id="ca005-140">The report name.</span></span>

</dd> <dt>

<span data-ttu-id="ca005-141">**женератиондатетиме**</span><span class="sxs-lookup"><span data-stu-id="ca005-141">**GenerationDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca005-142">Тип данных: **[DateTime](/windows/desktop/WmiSdk/datetime)**</span><span class="sxs-lookup"><span data-stu-id="ca005-142">Data type: **[DATETIME](/windows/desktop/WmiSdk/datetime)**</span></span>
</dt> <dt>

<span data-ttu-id="ca005-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca005-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca005-144">Дата и время создания отчета лицензирования удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="ca005-144">RD Licensing report generation date and time.</span></span>

</dd> <dt>

<span data-ttu-id="ca005-145">**инсталледлиценсес**</span><span class="sxs-lookup"><span data-stu-id="ca005-145">**InstalledLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca005-146">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca005-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca005-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca005-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca005-148">Квалификаторы: не [ **рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ca005-148">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ca005-149">Данное свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ca005-149">This property is not supported.</span></span>

<span data-ttu-id="ca005-150">**Windows server 2008 R2 и Windows server 2008:** Число установленных клиентских лицензий служб удаленных рабочих столов "на пользователя".</span><span class="sxs-lookup"><span data-stu-id="ca005-150">**Windows Server 2008 R2 and Windows Server 2008:** Number of RDS Per User CALs that are installed.</span></span>

</dd> <dt>

<span data-ttu-id="ca005-151">**лиценсеусажекаунт**</span><span class="sxs-lookup"><span data-stu-id="ca005-151">**LicenseUsageCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca005-152">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca005-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca005-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca005-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca005-154">Квалификаторы: не [ **рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ca005-154">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ca005-155">Данное свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ca005-155">This property is not supported.</span></span>

<span data-ttu-id="ca005-156">**Windows server 2008 R2 и Windows server 2008:** Количество клиентских лицензий служб удаленных рабочих столов "на пользователя", которые в настоящее время используются.</span><span class="sxs-lookup"><span data-stu-id="ca005-156">**Windows Server 2008 R2 and Windows Server 2008:** Number of RDS Per User CALs that are currently in use.</span></span>

</dd> <dt>

<span data-ttu-id="ca005-157">**ScopeType**</span><span class="sxs-lookup"><span data-stu-id="ca005-157">**ScopeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca005-158">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca005-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca005-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca005-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca005-160">Квалификаторы: не [ **рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ca005-160">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ca005-161">Данное свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ca005-161">This property is not supported.</span></span>

<span data-ttu-id="ca005-162">**Windows server 2008 R2 и Windows server 2008:** Тип области отчета лицензирования удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="ca005-162">**Windows Server 2008 R2 and Windows Server 2008:** RD Licensing report scope type.</span></span>

</dd> <dt>

<span data-ttu-id="ca005-163">**скопевалуе**</span><span class="sxs-lookup"><span data-stu-id="ca005-163">**ScopeValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca005-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca005-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca005-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca005-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca005-166">Квалификаторы: не [ **рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ca005-166">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ca005-167">Данное свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ca005-167">This property is not supported.</span></span>

<span data-ttu-id="ca005-168">**Windows server 2008 R2 и Windows server 2008:** Значение области отчета лицензирования удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="ca005-168">**Windows Server 2008 R2 and Windows Server 2008:** RD Licensing report scope value.</span></span>

</dd> <dt>

<span data-ttu-id="ca005-169">**Version**</span><span class="sxs-lookup"><span data-stu-id="ca005-169">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca005-170">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca005-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca005-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca005-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca005-172">Версия отчета лицензирования удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="ca005-172">RD Licensing report version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca005-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca005-173">Remarks</span></span>

<span data-ttu-id="ca005-174">Отчеты, созданные с помощью WMI, отображаются в диспетчере лицензирования удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="ca005-174">Reports that are generated by using WMI are displayed in RD Licensing Manager.</span></span> <span data-ttu-id="ca005-175">Отчеты, удаленные с помощью WMI, также удаляются из диспетчера лицензирования удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="ca005-175">Reports that are deleted by using WMI are also deleted from RD Licensing Manager.</span></span>

<span data-ttu-id="ca005-176">Для использования этого класса необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="ca005-176">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="ca005-177">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="ca005-177">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ca005-178">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="ca005-178">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ca005-179">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="ca005-179">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ca005-180">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ca005-180">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca005-181">Требования</span><span class="sxs-lookup"><span data-stu-id="ca005-181">Requirements</span></span>



| <span data-ttu-id="ca005-182">Требование</span><span class="sxs-lookup"><span data-stu-id="ca005-182">Requirement</span></span> | <span data-ttu-id="ca005-183">Значение</span><span class="sxs-lookup"><span data-stu-id="ca005-183">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca005-184">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca005-184">Minimum supported client</span></span><br/> | <span data-ttu-id="ca005-185">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ca005-185">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="ca005-186">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca005-186">Minimum supported server</span></span><br/> | <span data-ttu-id="ca005-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca005-187">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ca005-188">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ca005-188">Namespace</span></span><br/>                | <span data-ttu-id="ca005-189">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="ca005-189">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="ca005-190">MOF</span><span class="sxs-lookup"><span data-stu-id="ca005-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca005-191"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca005-191"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca005-192">DLL</span><span class="sxs-lookup"><span data-stu-id="ca005-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca005-193"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca005-193"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca005-194">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca005-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca005-195">**\_Тсиссуедлиценсе Win32**</span><span class="sxs-lookup"><span data-stu-id="ca005-195">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="ca005-196">**\_Тслиценсекэйпакк Win32**</span><span class="sxs-lookup"><span data-stu-id="ca005-196">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="ca005-197">**\_Тслиценсерепортентри Win32**</span><span class="sxs-lookup"><span data-stu-id="ca005-197">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> <dt>

[<span data-ttu-id="ca005-198">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="ca005-198">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

