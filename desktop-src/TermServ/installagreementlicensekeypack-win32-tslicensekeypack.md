---
title: Метод Инсталлагриментлиценсекэйпакк класса Win32_TSLicenseKeyPack
description: Устанавливает службы удаленных рабочих столов пакет лицензионных ключей, приобретенный по лицензионному соглашению, и автоматически подключается через Интернет для проверки лицензии на пакет ключей.
ms.assetid: 70a0aac3-2709-47ba-bf6a-549393c4c115
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Инсталлагриментлиценсекэйпакк
- Службы удаленных рабочих столов метода Инсталлагриментлиценсекэйпакк, класс Win32_TSLicenseKeyPack
- Класс Win32_TSLicenseKeyPack службы удаленных рабочих столов, метод Инсталлагриментлиценсекэйпакк
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb891469feae169c1267c12c04af6d21415c309
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682080"
---
# <a name="installagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="e788c-106">Метод Инсталлагриментлиценсекэйпакк \_ класса Win32 тслиценсекэйпакк</span><span class="sxs-lookup"><span data-stu-id="e788c-106">InstallAgreementLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="e788c-107">Устанавливает службы удаленных рабочих столов пакет лицензионных ключей, приобретенный по лицензионному соглашению, и автоматически подключается через Интернет для проверки лицензии на пакет ключей.</span><span class="sxs-lookup"><span data-stu-id="e788c-107">Installs a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span>

## <a name="syntax"></a><span data-ttu-id="e788c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e788c-108">Syntax</span></span>


```mof
uint32 InstallAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a><span data-ttu-id="e788c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e788c-109">Parameters</span></span>

<span data-ttu-id="e788c-110">*AgreementType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e788c-110">*AgreementType* \[in\]</span></span>

<span data-ttu-id="e788c-111">Тип соглашения.</span><span class="sxs-lookup"><span data-stu-id="e788c-111">Agreement type.</span></span>

| <span data-ttu-id="e788c-112">Значение</span><span class="sxs-lookup"><span data-stu-id="e788c-112">Value</span></span> | <span data-ttu-id="e788c-113">Описание</span><span class="sxs-lookup"><span data-stu-id="e788c-113">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="e788c-114">0</span><span class="sxs-lookup"><span data-stu-id="e788c-114">0</span></span> | <span data-ttu-id="e788c-115">Пакет лицензионных ключей относится к выбранному соглашению о корпоративном лицензировании (для клиентов с 250 или более компьютеров).</span><span class="sxs-lookup"><span data-stu-id="e788c-115">The license key pack is from a Select volume license agreement (for customers with 250 or more computers).</span></span> <span data-ttu-id="e788c-116">Параметр *сагриментнумбер* — номер регистрации (семь цифр), найденный в подписанном соглашении.</span><span class="sxs-lookup"><span data-stu-id="e788c-116">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="e788c-117">1</span><span class="sxs-lookup"><span data-stu-id="e788c-117">1</span></span> | <span data-ttu-id="e788c-118">Пакет лицензионных ключей относится к корпоративному соглашению корпоративного лицензирования для клиентов с 250 или более компьютеров.</span><span class="sxs-lookup"><span data-stu-id="e788c-118">The license key pack is from an Enterprise volume license agreement for customers with 250 or more computers.</span></span> <span data-ttu-id="e788c-119">Параметр *сагриментнумбер* — номер регистрации (семь цифр), найденный в подписанном соглашении.</span><span class="sxs-lookup"><span data-stu-id="e788c-119">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="e788c-120">2</span><span class="sxs-lookup"><span data-stu-id="e788c-120">2</span></span> | <span data-ttu-id="e788c-121">Пакет лицензионных ключей относится к соглашению о корпоративном лицензировании для образовательных учреждений.</span><span class="sxs-lookup"><span data-stu-id="e788c-121">The license key pack is from a Campus volume license agreement for a higher education institution.</span></span> <span data-ttu-id="e788c-122">Параметр *сагриментнумбер* — номер регистрации (семь цифр), найденный в подписанном соглашении.</span><span class="sxs-lookup"><span data-stu-id="e788c-122">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="e788c-123">3</span><span class="sxs-lookup"><span data-stu-id="e788c-123">3</span></span> | <span data-ttu-id="e788c-124">Пакет лицензионных ключей входит в состав учебного соглашения корпоративного лицензирования для основного и дополнительного учреждений.</span><span class="sxs-lookup"><span data-stu-id="e788c-124">The license key pack is from a School volume license agreement for primary and secondary institutions.</span></span> <span data-ttu-id="e788c-125">Параметр *сагриментнумбер* — номер регистрации (семь цифр), найденный в подписанном соглашении.</span><span class="sxs-lookup"><span data-stu-id="e788c-125">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="e788c-126">4</span><span class="sxs-lookup"><span data-stu-id="e788c-126">4</span></span> | <span data-ttu-id="e788c-127">Пакет лицензионных ключей предоставляется лицензионным соглашением поставщика услуг для поставщиков услуг по ежемесячному лицензированию программного обеспечения Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="e788c-127">The license key pack is from a Service Provider license agreement for service providers to license Microsoft software on a monthly basis.</span></span> <span data-ttu-id="e788c-128">Параметр *сагриментнумбер* — номер регистрации (семь цифр), найденный в подписанном соглашении.</span><span class="sxs-lookup"><span data-stu-id="e788c-128">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="e788c-129">5</span><span class="sxs-lookup"><span data-stu-id="e788c-129">5</span></span> | <span data-ttu-id="e788c-130">Пакет лицензионных ключей относится к другому лицензионному соглашению, такому как открытая стоимость, открытая лицензия на несколько лет и открытая лицензия на подписку.</span><span class="sxs-lookup"><span data-stu-id="e788c-130">The license key pack is from another license agreement, such as Open Value, Multi-Year Open License, and Open Subscription License.</span></span> <span data-ttu-id="e788c-131">Параметр *сагриментнумбер* — это номер соглашения, предоставленный в сведениях о программе.</span><span class="sxs-lookup"><span data-stu-id="e788c-131">The *sAgreementNumber* parameter is the agreement number provided with your program information.</span></span> |

<span data-ttu-id="e788c-132">*сагриментнумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e788c-132">*sAgreementNumber* \[in\]</span></span>

<span data-ttu-id="e788c-133">Номер соглашения или номер регистрации.</span><span class="sxs-lookup"><span data-stu-id="e788c-133">Agreement number or enrollment number.</span></span> <span data-ttu-id="e788c-134">Параметр *сагриментнумбер* — это семь цифр числовая строка без дефисов.</span><span class="sxs-lookup"><span data-stu-id="e788c-134">The *sAgreementNumber* parameter is a seven digit numeric string without hyphens.</span></span>

<span data-ttu-id="e788c-135">*ProductVersion* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e788c-135">*ProductVersion* \[in\]</span></span>

<span data-ttu-id="e788c-136">Номер версии продукта.</span><span class="sxs-lookup"><span data-stu-id="e788c-136">Product version.</span></span>

| <span data-ttu-id="e788c-137">Значение</span><span class="sxs-lookup"><span data-stu-id="e788c-137">Value</span></span> | <span data-ttu-id="e788c-138">Описание</span><span class="sxs-lookup"><span data-stu-id="e788c-138">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="e788c-139">0</span><span class="sxs-lookup"><span data-stu-id="e788c-139">0</span></span> | <span data-ttu-id="e788c-140">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e788c-140">Not supported</span></span> |
| <span data-ttu-id="e788c-141">1</span><span class="sxs-lookup"><span data-stu-id="e788c-141">1</span></span> | <span data-ttu-id="e788c-142">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e788c-142">Not supported</span></span> |
| <span data-ttu-id="e788c-143">2</span><span class="sxs-lookup"><span data-stu-id="e788c-143">2</span></span> | <span data-ttu-id="e788c-144">Windows Server 2008/Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e788c-144">Windows Server 2008/Windows Server 2008 R2</span></span> |
| <span data-ttu-id="e788c-145">4</span><span class="sxs-lookup"><span data-stu-id="e788c-145">4</span></span> | <span data-ttu-id="e788c-146">Windows Server 2012/Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e788c-146">Windows Server 2012/Windows Server 2012 R2</span></span> |
| <span data-ttu-id="e788c-147">5</span><span class="sxs-lookup"><span data-stu-id="e788c-147">5</span></span> | <span data-ttu-id="e788c-148">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e788c-148">Windows Server 2016</span></span> |
| <span data-ttu-id="e788c-149">6</span><span class="sxs-lookup"><span data-stu-id="e788c-149">6</span></span> | <span data-ttu-id="e788c-150">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="e788c-150">Windows Server 2019</span></span> |

<span data-ttu-id="e788c-151">*Продукттипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e788c-151">*ProductType* \[in\]</span></span>

<span data-ttu-id="e788c-152">Тип продукта.</span><span class="sxs-lookup"><span data-stu-id="e788c-152">Product type.</span></span>

| <span data-ttu-id="e788c-153">Значение</span><span class="sxs-lookup"><span data-stu-id="e788c-153">Value</span></span> | <span data-ttu-id="e788c-154">Описание</span><span class="sxs-lookup"><span data-stu-id="e788c-154">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="e788c-155">0</span><span class="sxs-lookup"><span data-stu-id="e788c-155">0</span></span> | <span data-ttu-id="e788c-156">Тип продукта пакета лицензионных ключей службы удаленных рабочих столов для каждого устройства.</span><span class="sxs-lookup"><span data-stu-id="e788c-156">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="e788c-157">Таким образом, каждому устройству, которое подключается к серверу узла сеансов удаленных рабочих столов, должна быть назначена лицензия.</span><span class="sxs-lookup"><span data-stu-id="e788c-157">Therefore, each device that connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="e788c-158">1</span><span class="sxs-lookup"><span data-stu-id="e788c-158">1</span></span> | <span data-ttu-id="e788c-159">Тип продукта пакета лицензионных ключей службы удаленных рабочих столов для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="e788c-159">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="e788c-160">Поэтому у каждого пользователя, подключающегося к серверу узла сеансов удаленных рабочих столов, должна быть лицензия.</span><span class="sxs-lookup"><span data-stu-id="e788c-160">Therefore, each user who connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="e788c-161">2</span><span class="sxs-lookup"><span data-stu-id="e788c-161">2</span></span> | <span data-ttu-id="e788c-162">Недопустимый тип продукта.</span><span class="sxs-lookup"><span data-stu-id="e788c-162">This product type is not valid.</span></span> |

<span data-ttu-id="e788c-163">*Лиценсекаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e788c-163">*LicenseCount* \[in\]</span></span>

<span data-ttu-id="e788c-164">Число устанавливаемых лицензий.</span><span class="sxs-lookup"><span data-stu-id="e788c-164">Number of licenses to install.</span></span>

<span data-ttu-id="e788c-165">*Кэйпаккид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e788c-165">*KeyPackId* \[out\]</span></span>

<span data-ttu-id="e788c-166">Получает идентификатор пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="e788c-166">Receives the key pack identifier.</span></span>

## <a name="return-value"></a><span data-ttu-id="e788c-167">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e788c-167">Return value</span></span>

<span data-ttu-id="e788c-168">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="e788c-168">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e788c-169">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="e788c-169">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e788c-170">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e788c-170">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e788c-171">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e788c-171">Remarks</span></span>

<span data-ttu-id="e788c-172">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="e788c-172">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e788c-173">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="e788c-173">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e788c-174">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="e788c-174">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e788c-175">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="e788c-175">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e788c-176">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e788c-176">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e788c-177">Требования</span><span class="sxs-lookup"><span data-stu-id="e788c-177">Requirements</span></span>

| <span data-ttu-id="e788c-178">Требование</span><span class="sxs-lookup"><span data-stu-id="e788c-178">Requirement</span></span> | <span data-ttu-id="e788c-179">Значение</span><span class="sxs-lookup"><span data-stu-id="e788c-179">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e788c-180">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e788c-180">Minimum supported client</span></span><br/> | <span data-ttu-id="e788c-181">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e788c-181">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="e788c-182">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e788c-182">Minimum supported server</span></span><br/> | <span data-ttu-id="e788c-183">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e788c-183">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="e788c-184">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e788c-184">Namespace</span></span><br/>                | <span data-ttu-id="e788c-185">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="e788c-185">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="e788c-186">MOF</span><span class="sxs-lookup"><span data-stu-id="e788c-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e788c-187"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e788c-187"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e788c-188">DLL</span><span class="sxs-lookup"><span data-stu-id="e788c-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e788c-189"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e788c-189"><dt>TlsWmiProv.dll</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="e788c-190">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e788c-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e788c-191">**\_Тслиценсекэйпакк Win32**</span><span class="sxs-lookup"><span data-stu-id="e788c-191">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

