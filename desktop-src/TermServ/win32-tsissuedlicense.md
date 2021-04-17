---
title: Класс Win32_TSIssuedLicense
description: Описывает экземпляры клиентских лицензий службы удаленных рабочих столов для каждого устройства (RDS \ 160; CAL "на устройство"), выпущенных на сервере лицензий удаленный рабочий стол.
ms.assetid: 15825dc5-9ada-4c11-ac77-beb681e9b33c
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSIssuedLicense службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSIssuedLicense, описание
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense
- Win32_TSIssuedLicense.LicenseId
- Win32_TSIssuedLicense.KeyPackId
- Win32_TSIssuedLicense.sIssuedToUser
- Win32_TSIssuedLicense.sIssuedToComputer
- Win32_TSIssuedLicense.LicenseStatus
- Win32_TSIssuedLicense.IssueDate
- Win32_TSIssuedLicense.ExpirationDate
- Win32_TSIssuedLicense.sHardwareId
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c3d08a68ddcc15a912de4c674403928211a297e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681902"
---
# <a name="win32_tsissuedlicense-class"></a><span data-ttu-id="42cc4-105">\_Класс Win32 тсиссуедлиценсе</span><span class="sxs-lookup"><span data-stu-id="42cc4-105">Win32\_TSIssuedLicense class</span></span>

<span data-ttu-id="42cc4-106">Описывает экземпляры лицензий на клиентский доступ службы удаленных рабочих столов на устройство (клиентские лицензии на устройства), выданные с сервера лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="42cc4-106">Describes instances of Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) that are issued from a Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="42cc4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42cc4-107">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSIssuedLicense
{
  uint32   LicenseId;
  uint32   KeyPackId;
  string   sIssuedToUser;
  string   sIssuedToComputer;
  uint32   LicenseStatus;
  DATETIME IssueDate;
  DATETIME ExpirationDate;
  string   sHardwareId;
};
```

## <a name="members"></a><span data-ttu-id="42cc4-108">Члены</span><span class="sxs-lookup"><span data-stu-id="42cc4-108">Members</span></span>

<span data-ttu-id="42cc4-109">Класс **Win32 \_ тсиссуедлиценсе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="42cc4-109">The **Win32\_TSIssuedLicense** class has these types of members:</span></span>

-   [<span data-ttu-id="42cc4-110">Методы</span><span class="sxs-lookup"><span data-stu-id="42cc4-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="42cc4-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="42cc4-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="42cc4-112">Методы</span><span class="sxs-lookup"><span data-stu-id="42cc4-112">Methods</span></span>

<span data-ttu-id="42cc4-113">Класс **Win32 \_ тсиссуедлиценсе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="42cc4-113">The **Win32\_TSIssuedLicense** class has these methods.</span></span>



| <span data-ttu-id="42cc4-114">Метод</span><span class="sxs-lookup"><span data-stu-id="42cc4-114">Method</span></span>                                         | <span data-ttu-id="42cc4-115">Описание</span><span class="sxs-lookup"><span data-stu-id="42cc4-115">Description</span></span>                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42cc4-116">**REVOKE**</span><span class="sxs-lookup"><span data-stu-id="42cc4-116">**Revoke**</span></span>](revoke-win32-tsissuedlicense.md) | <span data-ttu-id="42cc4-117">Отменяет клиентские лицензии RDS "на устройство", представленные объектом **Win32 \_ тсиссуедлиценсе** .</span><span class="sxs-lookup"><span data-stu-id="42cc4-117">Revokes the RDS Per Device CALs that are represented by the **Win32\_TSIssuedLicense** object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="42cc4-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="42cc4-118">Properties</span></span>

<span data-ttu-id="42cc4-119">Класс **Win32 \_ тсиссуедлиценсе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="42cc4-119">The **Win32\_TSIssuedLicense** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="42cc4-120">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="42cc4-120">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42cc4-121">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="42cc4-121">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="42cc4-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="42cc4-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42cc4-123">Указывает дату истечения срока действия лицензии.</span><span class="sxs-lookup"><span data-stu-id="42cc4-123">Identifies the date that the license will expire.</span></span>

</dd> <dt>

<span data-ttu-id="42cc4-124">**иссуедате**</span><span class="sxs-lookup"><span data-stu-id="42cc4-124">**IssueDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42cc4-125">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="42cc4-125">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="42cc4-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="42cc4-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42cc4-127">Указывает дату выдачи лицензии.</span><span class="sxs-lookup"><span data-stu-id="42cc4-127">Identifies the date that the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="42cc4-128">**кэйпаккид**</span><span class="sxs-lookup"><span data-stu-id="42cc4-128">**KeyPackId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42cc4-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42cc4-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42cc4-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="42cc4-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42cc4-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="42cc4-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="42cc4-132">Идентифицирует службы удаленных рабочих столов пакет лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="42cc4-132">Identifies the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="42cc4-133">**лиценсеид**</span><span class="sxs-lookup"><span data-stu-id="42cc4-133">**LicenseId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42cc4-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42cc4-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42cc4-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="42cc4-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42cc4-136">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="42cc4-136">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="42cc4-137">Уникальный идентификатор для этой лицензии.</span><span class="sxs-lookup"><span data-stu-id="42cc4-137">Unique identifier for this license.</span></span>

</dd> <dt>

<span data-ttu-id="42cc4-138">**LicenseStatus**</span><span class="sxs-lookup"><span data-stu-id="42cc4-138">**LicenseStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42cc4-139">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42cc4-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42cc4-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="42cc4-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42cc4-141">Состояние лицензии.</span><span class="sxs-lookup"><span data-stu-id="42cc4-141">Status of the license.</span></span>

<dt>

<span data-ttu-id="42cc4-142">0</span><span class="sxs-lookup"><span data-stu-id="42cc4-142">0</span></span>
</dt> <dd>

<span data-ttu-id="42cc4-143">Состояние лицензии неизвестно.</span><span class="sxs-lookup"><span data-stu-id="42cc4-143">The license status is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="42cc4-144">1</span><span class="sxs-lookup"><span data-stu-id="42cc4-144">1</span></span>
</dt> <dd>

<span data-ttu-id="42cc4-145">Лицензия является временной лицензией.</span><span class="sxs-lookup"><span data-stu-id="42cc4-145">The license is a temporary license.</span></span>

</dd> <dt>

<span data-ttu-id="42cc4-146">2</span><span class="sxs-lookup"><span data-stu-id="42cc4-146">2</span></span>
</dt> <dd>

<span data-ttu-id="42cc4-147">Лицензия активна.</span><span class="sxs-lookup"><span data-stu-id="42cc4-147">The license is active.</span></span>

</dd> <dt>

<span data-ttu-id="42cc4-148">3</span><span class="sxs-lookup"><span data-stu-id="42cc4-148">3</span></span>
</dt> <dd>

<span data-ttu-id="42cc4-149">Лицензия является лицензией на обновление.</span><span class="sxs-lookup"><span data-stu-id="42cc4-149">The license is an upgrade license.</span></span>

</dd> <dt>

<span data-ttu-id="42cc4-150">4</span><span class="sxs-lookup"><span data-stu-id="42cc4-150">4</span></span>
</dt> <dd>

<span data-ttu-id="42cc4-151">Лицензия была отозвана.</span><span class="sxs-lookup"><span data-stu-id="42cc4-151">The license has been revoked.</span></span>

</dd> <dt>

<span data-ttu-id="42cc4-152">5</span><span class="sxs-lookup"><span data-stu-id="42cc4-152">5</span></span>
</dt> <dd>

<span data-ttu-id="42cc4-153">Состояние лицензии — ожидание.</span><span class="sxs-lookup"><span data-stu-id="42cc4-153">The license status is pending.</span></span>

</dd> <dt>

<span data-ttu-id="42cc4-154">6</span><span class="sxs-lookup"><span data-stu-id="42cc4-154">6</span></span>
</dt> <dd>

<span data-ttu-id="42cc4-155">Лицензия является параллельной лицензией.</span><span class="sxs-lookup"><span data-stu-id="42cc4-155">The license is a concurrent license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="42cc4-156">**шардвареид**</span><span class="sxs-lookup"><span data-stu-id="42cc4-156">**sHardwareId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42cc4-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="42cc4-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42cc4-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="42cc4-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42cc4-159">Идентификатор оборудования, для которого была выдана лицензия.</span><span class="sxs-lookup"><span data-stu-id="42cc4-159">Hardware identifier for which the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="42cc4-160">**сиссуедтокомпутер**</span><span class="sxs-lookup"><span data-stu-id="42cc4-160">**sIssuedToComputer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42cc4-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="42cc4-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42cc4-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="42cc4-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42cc4-163">Имя компьютера, для которого была выдана лицензия.</span><span class="sxs-lookup"><span data-stu-id="42cc4-163">Computer name for which the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="42cc4-164">**сиссуедтаусер**</span><span class="sxs-lookup"><span data-stu-id="42cc4-164">**sIssuedToUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42cc4-165">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="42cc4-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42cc4-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="42cc4-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42cc4-167">Имя пользователя, для которого была выдана лицензия.</span><span class="sxs-lookup"><span data-stu-id="42cc4-167">User name for which the license was issued.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42cc4-168">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42cc4-168">Remarks</span></span>

<span data-ttu-id="42cc4-169">Для использования этого класса необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="42cc4-169">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="42cc4-170">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="42cc4-170">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="42cc4-171">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="42cc4-171">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="42cc4-172">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="42cc4-172">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="42cc4-173">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="42cc4-173">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="42cc4-174">Требования</span><span class="sxs-lookup"><span data-stu-id="42cc4-174">Requirements</span></span>



| <span data-ttu-id="42cc4-175">Требование</span><span class="sxs-lookup"><span data-stu-id="42cc4-175">Requirement</span></span> | <span data-ttu-id="42cc4-176">Значение</span><span class="sxs-lookup"><span data-stu-id="42cc4-176">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="42cc4-177">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42cc4-177">Minimum supported client</span></span><br/> | <span data-ttu-id="42cc4-178">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="42cc4-178">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="42cc4-179">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42cc4-179">Minimum supported server</span></span><br/> | <span data-ttu-id="42cc4-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42cc4-180">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="42cc4-181">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="42cc4-181">Namespace</span></span><br/>                | <span data-ttu-id="42cc4-182">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="42cc4-182">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="42cc4-183">MOF</span><span class="sxs-lookup"><span data-stu-id="42cc4-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42cc4-184"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42cc4-184"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="42cc4-185">DLL</span><span class="sxs-lookup"><span data-stu-id="42cc4-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42cc4-186"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42cc4-186"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42cc4-187">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42cc4-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42cc4-188">**\_Тслиценсекэйпакк Win32**</span><span class="sxs-lookup"><span data-stu-id="42cc4-188">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="42cc4-189">**\_Тслиценсерепорт Win32**</span><span class="sxs-lookup"><span data-stu-id="42cc4-189">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="42cc4-190">**\_Тслиценсерепортентри Win32**</span><span class="sxs-lookup"><span data-stu-id="42cc4-190">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> <dt>

[<span data-ttu-id="42cc4-191">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="42cc4-191">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

