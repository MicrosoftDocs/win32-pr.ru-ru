---
title: Класс Win32_TSLicenseKeyPack
description: Предоставляет методы и свойства для просмотра и установки службы удаленных рабочих столов пакетов лицензионных ключей.
ms.assetid: 27450646-c51f-4911-bb42-410794e32003
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSLicenseKeyPack службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSLicenseKeyPack, описание
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack.KeyPackId
- Win32_TSLicenseKeyPack.Description
- Win32_TSLicenseKeyPack.KeyPackType
- Win32_TSLicenseKeyPack.ProductType
- Win32_TSLicenseKeyPack.ProductVersion
- Win32_TSLicenseKeyPack.ProductVersionID
- Win32_TSLicenseKeyPack.TotalLicenses
- Win32_TSLicenseKeyPack.IssuedLicenses
- Win32_TSLicenseKeyPack.AvailableLicenses
- Win32_TSLicenseKeyPack.ExpirationDate
- Win32_TSLicenseKeyPack.AccessRights
- Win32_TSLicenseKeyPack.TypeAndModel
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d78af398ebf7c137be5b31c9db427691a66a7a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533788"
---
# <a name="win32_tslicensekeypack-class"></a><span data-ttu-id="ed3d2-105">\_Класс Win32 тслиценсекэйпакк</span><span class="sxs-lookup"><span data-stu-id="ed3d2-105">Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="ed3d2-106">Предоставляет методы и свойства для просмотра и установки службы удаленных рабочих столов пакетов лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-106">Provides methods and properties for viewing and installing Remote Desktop Services license key packs.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed3d2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed3d2-107">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseKeyPack
{
  uint32   KeyPackId;
  string   Description;
  uint32   KeyPackType;
  uint32   ProductType;
  string   ProductVersion;
  uint32   ProductVersionID;
  uint32   TotalLicenses;
  uint32   IssuedLicenses;
  uint32   AvailableLicenses;
  DATETIME ExpirationDate;
  uint32   AccessRights;
  string   TypeAndModel;
};
```

## <a name="members"></a><span data-ttu-id="ed3d2-108">Члены</span><span class="sxs-lookup"><span data-stu-id="ed3d2-108">Members</span></span>

<span data-ttu-id="ed3d2-109">Класс **Win32 \_ тслиценсекэйпакк** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ed3d2-109">The **Win32\_TSLicenseKeyPack** class has these types of members:</span></span>

-   [<span data-ttu-id="ed3d2-110">Методы</span><span class="sxs-lookup"><span data-stu-id="ed3d2-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ed3d2-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="ed3d2-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ed3d2-112">Методы</span><span class="sxs-lookup"><span data-stu-id="ed3d2-112">Methods</span></span>

<span data-ttu-id="ed3d2-113">Класс **Win32 \_ тслиценсекэйпакк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-113">The **Win32\_TSLicenseKeyPack** class has these methods.</span></span>



| <span data-ttu-id="ed3d2-114">Метод</span><span class="sxs-lookup"><span data-stu-id="ed3d2-114">Method</span></span>                                                                                                        | <span data-ttu-id="ed3d2-115">Описание</span><span class="sxs-lookup"><span data-stu-id="ed3d2-115">Description</span></span>                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed3d2-116">**конвертлиценсес**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-116">**ConvertLicenses**</span></span>](convertlicenses-win32-tslicensekeypack.md)                                             | <span data-ttu-id="ed3d2-117">Преобразует лицензии в текущем ключевом пакете.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-117">Converts the licenses in the current key pack.</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="ed3d2-118">**импортагриментлиценсекэйпакк**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-118">**ImportAgreementLicenseKeyPack**</span></span>](win32-tslicensekeypack-importagreementlicensekeypack.md)                 | <span data-ttu-id="ed3d2-119">Импорт, с другого сервера лицензий удаленный рабочий стол, службы удаленных рабочих столов пакета лицензионных ключей, приобретенного по лицензионному соглашению, и автоматически подключается через Интернет для проверки лицензии на пакет ключей.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-119">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span><br/> |
| [<span data-ttu-id="ed3d2-120">**импортлиценсекэйпаккоффлине**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-120">**ImportLicenseKeyPackOffline**</span></span>](win32-tslicensekeypack-importlicensekeypackoffline.md)                     | <span data-ttu-id="ed3d2-121">Импорт с другого сервера лицензий удаленный рабочий стол, службы удаленных рабочих столов пакета лицензионных ключей, который использует идентификатор лицензии, полученный через Интернет или по телефону.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-121">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that uses a license identifier that was received over the Internet or the phone.</span></span><br/>                                               |
| [<span data-ttu-id="ed3d2-122">**импортопенпурчаселиценсекэйпакк**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-122">**ImportOpenPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-importopenpurchaselicensekeypack.md)           | <span data-ttu-id="ed3d2-123">Импорт, с другого сервера лицензий удаленный рабочий стол — Open License службы удаленных рабочих столов пакет лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-123">Imports, from another Remote Desktop license server, an Open License Remote Desktop Services license key pack.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="ed3d2-124">**импортретаилпурчаселиценсекэйпакк**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-124">**ImportRetailPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-importretailpurchaselicensekeypack.md)       | <span data-ttu-id="ed3d2-125">Импорт с другого сервера лицензий удаленный рабочий стол, службы удаленных рабочих столов пакета лицензионных ключей, приобретенного по розничному каналу.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-125">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span><br/>                                                                                   |
| [<span data-ttu-id="ed3d2-126">**инсталлагриментлиценсекэйпакк**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-126">**InstallAgreementLicenseKeyPack**</span></span>](installagreementlicensekeypack-win32-tslicensekeypack.md)               | <span data-ttu-id="ed3d2-127">Устанавливает службы удаленных рабочих столов пакет лицензионных ключей, приобретенный по лицензии на соглашение.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-127">Installs a Remote Desktop Services license key pack that was purchased through an agreement license.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="ed3d2-128">**инсталллиценсекэйпакк**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-128">**InstallLicenseKeyPack**</span></span>](installlicensekeypack-win32-tslicensekeypack.md)                                 | <span data-ttu-id="ed3d2-129">Устанавливает службы удаленных рабочих столов пакет лицензионных ключей, который использует идентификатор пакета лицензионных ключей, полученный через Интернет или по телефону.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-129">Installs a Remote Desktop Services license key pack that uses a license key pack ID that was received over the Internet or the phone.</span></span><br/>                                                                                          |
| [<span data-ttu-id="ed3d2-130">**инсталлопенлиценсекэйпакк**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-130">**InstallOpenLicenseKeyPack**</span></span>](installopenlicensekeypack-win32-tslicensekeypack.md)                         | <span data-ttu-id="ed3d2-131">Устанавливает службы удаленных рабочих столов пакет лицензионных ключей, приобретенный по открытому лицензионному соглашению.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-131">Installs a Remote Desktop Services license key pack that was purchased through an open license agreement.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="ed3d2-132">**инсталлретаилпурчаселиценсекэйпакк**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-132">**InstallRetailPurchaseLicenseKeyPack**</span></span>](installretailpurchaselicensekeypack-win32-tslicensekeypack.md)     | <span data-ttu-id="ed3d2-133">Устанавливает службы удаленных рабочих столов пакет лицензионных ключей, приобретенный в розничном магазине.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-133">Installs a Remote Desktop Services license key pack that was purchased through a retail store.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="ed3d2-134">**реинсталлагриментлиценсекэйпакк**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-134">**ReinstallAgreementLicenseKeyPack**</span></span>](win32-tslicensekeypack-reinstallagreementlicensekeypack.md)           | <span data-ttu-id="ed3d2-135">Переустанавливает пакет лицензионных ключей службы удаленных рабочих столов, приобретенный по лицензионному соглашению, и автоматически подключается через Интернет для проверки лицензии на пакет ключей.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-135">Reinstalls a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span><br/>                                           |
| [<span data-ttu-id="ed3d2-136">**реинсталллиценсекэйпаккоффлине**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-136">**ReinstallLicenseKeyPackOffline**</span></span>](win32-tslicensekeypack-reinstalllicensekeypackoffline.md)               | <span data-ttu-id="ed3d2-137">Переустанавливает пакет лицензионного ключа службы удаленных рабочих столов, который использует идентификатор лицензии, полученный через Интернет или по телефону.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-137">Reinstalls a Remote Desktop Services license key pack that uses the license identifier that was received over the Internet or the phone.</span></span><br/>                                                                                       |
| [<span data-ttu-id="ed3d2-138">**реинсталлопенпурчаселиценсекэйпакк**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-138">**ReinstallOpenPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-reinstallopenpurchaselicensekeypack.md)     | <span data-ttu-id="ed3d2-139">Переустанавливает открытый лицензионный пакет службы удаленных рабочих столов лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-139">Reinstalls an Open License Remote Desktop Services license key pack.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="ed3d2-140">**реинсталлретаилпурчаселиценсекэйпакк**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-140">**ReinstallRetailPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-reinstallretailpurchaselicensekeypack.md) | <span data-ttu-id="ed3d2-141">Переустанавливает пакет лицензионных ключей службы удаленных рабочих столов, приобретенный по розничному каналу.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-141">Reinstalls a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="ed3d2-142">**ремовелиценсесвисидкаунт**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-142">**RemoveLicensesWithIdCount**</span></span>](win32-tslicensekeypack-removelicenseswithidcount.md)                         | <span data-ttu-id="ed3d2-143">Удаляет указанное число лицензий службы удаленных рабочих столов из указанного пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-143">Removes the specified number of Remote Desktop Services licenses from the specified key pack.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="ed3d2-144">**унинсталллиценсекэйпакк**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-144">**UninstallLicenseKeyPack**</span></span>](win32-tslicensekeypack-uninstalllicensekeypack.md)                             | <span data-ttu-id="ed3d2-145">Удаляет службы удаленных рабочих столов пакет лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-145">Uninstalls a Remote Desktop Services license key pack.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="ed3d2-146">**унинсталллиценсекэйпакквисид**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-146">**UninstallLicenseKeyPackWithId**</span></span>](win32-tslicensekeypack-uninstalllicensekeypackwithid.md)                 | <span data-ttu-id="ed3d2-147">Удаляет службы удаленных рабочих столов пакет лицензионных ключей с указанным идентификатором пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-147">Uninstalls the Remote Desktop Services license key pack with the specified key pack identifier.</span></span><br/>                                                                                                                                |



 

### <a name="properties"></a><span data-ttu-id="ed3d2-148">Свойства</span><span class="sxs-lookup"><span data-stu-id="ed3d2-148">Properties</span></span>

<span data-ttu-id="ed3d2-149">Класс **Win32 \_ тслиценсекэйпакк** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-149">The **Win32\_TSLicenseKeyPack** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ed3d2-150">**AccessRights**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-150">**AccessRights**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3d2-151">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3d2-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed3d2-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed3d2-153">Квалификаторы: [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "3"), [**Битвалуес**](/windows/desktop/WmiSdk/standard-qualifiers) ("сеанс RD", "сеанс VDI", "Калиста", "Партнеры VDI")</span><span class="sxs-lookup"><span data-stu-id="ed3d2-153">Qualifiers: [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "3"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("RD Session", "VDI Session", "Calista", "VDI Partners")</span></span>
</dt> </dl>

<span data-ttu-id="ed3d2-154">Квалификатор для прав доступа к пакету лицензионных ключей служб терминалов</span><span class="sxs-lookup"><span data-stu-id="ed3d2-154">Qualifier for TS Licensing key pack access rights</span></span>

</dd> <dt>

<span data-ttu-id="ed3d2-155">**аваилаблелиценсес**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-155">**AvailableLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3d2-156">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3d2-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed3d2-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed3d2-158">Общее число доступных лицензий в службы удаленных рабочих столов пакете лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-158">Total number of available licenses in the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="ed3d2-159">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3d2-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed3d2-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed3d2-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed3d2-162">Описание пакета лицензионных ключей службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-162">Description of the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="ed3d2-163">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-163">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3d2-164">Тип данных: **[DateTime](/windows/desktop/WmiSdk/datetime)**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-164">Data type: **[DATETIME](/windows/desktop/WmiSdk/datetime)**</span></span>
</dt> <dt>

<span data-ttu-id="ed3d2-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed3d2-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed3d2-166">Дата истечения срока действия пакета лицензионных ключей службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-166">The expiration date of the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="ed3d2-167">**иссуедлиценсес**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-167">**IssuedLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3d2-168">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3d2-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed3d2-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed3d2-170">Общее число выданных лицензий в службы удаленных рабочих столов пакете лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-170">Total number of issued licenses in the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="ed3d2-171">**кэйпаккид**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-171">**KeyPackId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3d2-172">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3d2-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed3d2-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed3d2-174">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ed3d2-174">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ed3d2-175">Идентификатор пакета лицензионных ключей службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-175">Identifier for the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="ed3d2-176">**кэйпакктипе**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-176">**KeyPackType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3d2-177">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3d2-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed3d2-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed3d2-179">Тип пакета ключей для сервера лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-179">Type of key pack for the Remote Desktop license server.</span></span>

| <span data-ttu-id="ed3d2-180">Значение</span><span class="sxs-lookup"><span data-stu-id="ed3d2-180">Value</span></span> | <span data-ttu-id="ed3d2-181">Описание</span><span class="sxs-lookup"><span data-stu-id="ed3d2-181">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="ed3d2-182">0</span><span class="sxs-lookup"><span data-stu-id="ed3d2-182">0</span></span> | <span data-ttu-id="ed3d2-183">Неизвестный тип пакета лицензионных ключей службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-183">The Remote Desktop Services license key pack type is unknown.</span></span> |
| <span data-ttu-id="ed3d2-184">1</span><span class="sxs-lookup"><span data-stu-id="ed3d2-184">1</span></span> | <span data-ttu-id="ed3d2-185">Тип пакета лицензионных ключей службы удаленных рабочих столов является розничной покупкой.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-185">The Remote Desktop Services license key pack type is a retail purchase.</span></span> |
| <span data-ttu-id="ed3d2-186">2</span><span class="sxs-lookup"><span data-stu-id="ed3d2-186">2</span></span> | <span data-ttu-id="ed3d2-187">Службы удаленных рабочих столов тип пакета лицензионных ключей — это покупка тома.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-187">The Remote Desktop Services license key pack type is a volume purchase.</span></span> |
| <span data-ttu-id="ed3d2-188">3</span><span class="sxs-lookup"><span data-stu-id="ed3d2-188">3</span></span> | <span data-ttu-id="ed3d2-189">Службы удаленных рабочих столов тип пакета лицензионных ключей — это параллельная лицензия.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-189">The Remote Desktop Services license key pack type is a concurrent license.</span></span> |
| <span data-ttu-id="ed3d2-190">4</span><span class="sxs-lookup"><span data-stu-id="ed3d2-190">4</span></span> | <span data-ttu-id="ed3d2-191">Службы удаленных рабочих столов тип пакета лицензионных ключей является временным.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-191">The Remote Desktop Services license key pack type is temporary.</span></span> |
| <span data-ttu-id="ed3d2-192">5</span><span class="sxs-lookup"><span data-stu-id="ed3d2-192">5</span></span> | <span data-ttu-id="ed3d2-193">Службы удаленных рабочих столов тип пакета лицензионных ключей — открытая лицензия.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-193">The Remote Desktop Services license key pack type is an open license.</span></span> |
| <span data-ttu-id="ed3d2-194">6</span><span class="sxs-lookup"><span data-stu-id="ed3d2-194">6</span></span> | <span data-ttu-id="ed3d2-195">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-195">Not supported.</span></span> |

<span data-ttu-id="ed3d2-196">**продукттипе**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-196">**ProductType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3d2-197">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3d2-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed3d2-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed3d2-199">Тип продукта службы удаленных рабочих столов пакета лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-199">Product type of the Remote Desktop Services license key pack.</span></span>

| <span data-ttu-id="ed3d2-200">Значение</span><span class="sxs-lookup"><span data-stu-id="ed3d2-200">Value</span></span> | <span data-ttu-id="ed3d2-201">Описание</span><span class="sxs-lookup"><span data-stu-id="ed3d2-201">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="ed3d2-202">0</span><span class="sxs-lookup"><span data-stu-id="ed3d2-202">0</span></span> | <span data-ttu-id="ed3d2-203">Тип продукта пакета лицензионных ключей службы удаленных рабочих столов для каждого устройства.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-203">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="ed3d2-204">Таким образом, каждому устройству, которое подключается к серверу узла сеансов удаленных рабочих столов, должна быть назначена лицензия.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-204">Therefore, each device that connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="ed3d2-205">1</span><span class="sxs-lookup"><span data-stu-id="ed3d2-205">1</span></span> | <span data-ttu-id="ed3d2-206">Тип продукта пакета лицензионных ключей службы удаленных рабочих столов для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-206">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="ed3d2-207">Поэтому у каждого пользователя, подключающегося к серверу узла сеансов удаленных рабочих столов, должна быть лицензия.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-207">Therefore, each user who connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="ed3d2-208">2</span><span class="sxs-lookup"><span data-stu-id="ed3d2-208">2</span></span> | <span data-ttu-id="ed3d2-209">Недопустимый тип продукта.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-209">This product type is not valid.</span></span> |

<span data-ttu-id="ed3d2-210">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-210">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3d2-211">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed3d2-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed3d2-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed3d2-213">Версия продукта для службы удаленных рабочих столов пакета лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-213">Product version for the Remote Desktop Services license key pack.</span></span>

| <span data-ttu-id="ed3d2-214">Значение</span><span class="sxs-lookup"><span data-stu-id="ed3d2-214">Value</span></span> | <span data-ttu-id="ed3d2-215">Описание</span><span class="sxs-lookup"><span data-stu-id="ed3d2-215">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="ed3d2-216">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="ed3d2-216">"Windows Server 2012"</span></span> | <span data-ttu-id="ed3d2-217">С этой лицензией поддерживаются только серверы под Windows Server 2012, Windows Server 2008 R2 или Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-217">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span> |
| <span data-ttu-id="ed3d2-218">Windows Server 7</span><span class="sxs-lookup"><span data-stu-id="ed3d2-218">"Windows Server 7"</span></span> | <span data-ttu-id="ed3d2-219">С этой лицензией поддерживаются только серверы, работающие под Windows Server 2008 R2 или Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-219">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span> |
| <span data-ttu-id="ed3d2-220">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="ed3d2-220">"Windows Server 2008"</span></span> | <span data-ttu-id="ed3d2-221">Этот пакет ключей поддерживает только серверы под управлением Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-221">Only servers running Windows Server 2008 are supported by this key pack.</span></span> |

<span data-ttu-id="ed3d2-222">**продуктверсионид**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-222">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3d2-223">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3d2-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed3d2-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed3d2-225">Идентификатор версии продукта для службы удаленных рабочих столов пакета лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-225">Product version identifier for the Remote Desktop Services license key pack.</span></span>

| <span data-ttu-id="ed3d2-226">Значение</span><span class="sxs-lookup"><span data-stu-id="ed3d2-226">Value</span></span> | <span data-ttu-id="ed3d2-227">Описание</span><span class="sxs-lookup"><span data-stu-id="ed3d2-227">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="ed3d2-228">0</span><span class="sxs-lookup"><span data-stu-id="ed3d2-228">0</span></span> | <span data-ttu-id="ed3d2-229">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ed3d2-229">Not supported</span></span> |
| <span data-ttu-id="ed3d2-230">1</span><span class="sxs-lookup"><span data-stu-id="ed3d2-230">1</span></span> | <span data-ttu-id="ed3d2-231">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ed3d2-231">Not supported</span></span> |
| <span data-ttu-id="ed3d2-232">2</span><span class="sxs-lookup"><span data-stu-id="ed3d2-232">2</span></span> | <span data-ttu-id="ed3d2-233">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed3d2-233">Windows Server 2008</span></span> |
| <span data-ttu-id="ed3d2-234">3</span><span class="sxs-lookup"><span data-stu-id="ed3d2-234">3</span></span> | <span data-ttu-id="ed3d2-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ed3d2-235">Windows Server 2008 R2</span></span> |
| <span data-ttu-id="ed3d2-236">4</span><span class="sxs-lookup"><span data-stu-id="ed3d2-236">4</span></span> | <span data-ttu-id="ed3d2-237">Windows Server 2012/Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ed3d2-237">Windows Server 2012/Windows Server 2012 R2</span></span> |
| <span data-ttu-id="ed3d2-238">5</span><span class="sxs-lookup"><span data-stu-id="ed3d2-238">5</span></span> | <span data-ttu-id="ed3d2-239">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ed3d2-239">Windows Server 2016</span></span> |
| <span data-ttu-id="ed3d2-240">6</span><span class="sxs-lookup"><span data-stu-id="ed3d2-240">6</span></span> | <span data-ttu-id="ed3d2-241">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="ed3d2-241">Windows Server 2019</span></span> |

<span data-ttu-id="ed3d2-242">**тоталлиценсес**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-242">**TotalLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3d2-243">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3d2-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed3d2-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed3d2-245">Общее число лицензий в службы удаленных рабочих столов пакете лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-245">Total number of licenses in the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="ed3d2-246">**типеандмодел**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-246">**TypeAndModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3d2-247">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed3d2-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed3d2-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed3d2-249">Квалификатор для типа и модели пакета лицензионных ключей служб терминалов.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-249">Qualifier for TS Licensing key pack type and model.</span></span> <span data-ttu-id="ed3d2-250">Примеры: лицензия на подписку VDI на устройство, клиентская лицензия служб терминалов "на пользователя"</span><span class="sxs-lookup"><span data-stu-id="ed3d2-250">Examples: VDI Per Device subscription license, TS Per User CAL</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed3d2-251">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed3d2-251">Remarks</span></span>

<span data-ttu-id="ed3d2-252">Для использования этого класса необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-252">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="ed3d2-253">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="ed3d2-253">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ed3d2-254">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="ed3d2-254">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ed3d2-255">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-255">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ed3d2-256">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ed3d2-256">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed3d2-257">Требования</span><span class="sxs-lookup"><span data-stu-id="ed3d2-257">Requirements</span></span>



| <span data-ttu-id="ed3d2-258">Требование</span><span class="sxs-lookup"><span data-stu-id="ed3d2-258">Requirement</span></span> | <span data-ttu-id="ed3d2-259">Значение</span><span class="sxs-lookup"><span data-stu-id="ed3d2-259">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed3d2-260">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ed3d2-260">Minimum supported client</span></span><br/> | <span data-ttu-id="ed3d2-261">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ed3d2-261">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="ed3d2-262">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ed3d2-262">Minimum supported server</span></span><br/> | <span data-ttu-id="ed3d2-263">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed3d2-263">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ed3d2-264">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ed3d2-264">Namespace</span></span><br/>                | <span data-ttu-id="ed3d2-265">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="ed3d2-265">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="ed3d2-266">MOF</span><span class="sxs-lookup"><span data-stu-id="ed3d2-266">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed3d2-267"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed3d2-267"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed3d2-268">DLL</span><span class="sxs-lookup"><span data-stu-id="ed3d2-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed3d2-269"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed3d2-269"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed3d2-270">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed3d2-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed3d2-271">**\_Тсиссуедлиценсе Win32**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-271">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="ed3d2-272">**\_Тслиценсерепорт Win32**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-272">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="ed3d2-273">**\_Тслиценсерепортентри Win32**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-273">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> <dt>

[<span data-ttu-id="ed3d2-274">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="ed3d2-274">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

