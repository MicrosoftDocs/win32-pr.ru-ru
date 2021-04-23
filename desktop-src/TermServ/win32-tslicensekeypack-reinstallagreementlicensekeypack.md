---
title: Метод Реинсталлагриментлиценсекэйпакк класса Win32_TSLicenseKeyPack
description: Переустанавливает пакет лицензионных ключей службы удаленных рабочих столов, приобретенный по лицензионному соглашению, и автоматически подключается через Интернет для проверки лицензии на пакет ключей.
ms.assetid: BC3C966B-E6CE-45E2-BC1D-2439B75D4C3C
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Реинсталлагриментлиценсекэйпакк
- Службы удаленных рабочих столов метода Реинсталлагриментлиценсекэйпакк, класс Win32_TSLicenseKeyPack
- Класс Win32_TSLicenseKeyPack службы удаленных рабочих столов, метод Реинсталлагриментлиценсекэйпакк
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821ff6dc538a670e03757253b616ff16489dc108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534253"
---
# <a name="reinstallagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="6ee1b-106">Метод Реинсталлагриментлиценсекэйпакк \_ класса Win32 тслиценсекэйпакк</span><span class="sxs-lookup"><span data-stu-id="6ee1b-106">ReinstallAgreementLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="6ee1b-107">Переустанавливает пакет лицензионных ключей службы удаленных рабочих столов, приобретенный по лицензионному соглашению, и автоматически подключается через Интернет для проверки лицензии на пакет ключей.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-107">Reinstalls a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ee1b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ee1b-108">Syntax</span></span>


```mof
uint32 ReinstallAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="6ee1b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ee1b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ee1b-110">*AgreementType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ee1b-110">*AgreementType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ee1b-111">Тип соглашения.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-111">Agreement type.</span></span>

<dt>

<span data-ttu-id="6ee1b-112">0</span><span class="sxs-lookup"><span data-stu-id="6ee1b-112">0</span></span>
</dt> <dd>

<span data-ttu-id="6ee1b-113">Пакет лицензионных ключей относится к выбранному соглашению о корпоративном лицензировании (для клиентов с 250 или более компьютеров).</span><span class="sxs-lookup"><span data-stu-id="6ee1b-113">The license key pack is from a Select volume license agreement (for customers with 250 or more computers).</span></span> <span data-ttu-id="6ee1b-114">Параметр *сагриментнумбер* — номер регистрации (семь цифр), найденный в подписанном соглашении.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-114">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="6ee1b-115">1</span><span class="sxs-lookup"><span data-stu-id="6ee1b-115">1</span></span>
</dt> <dd>

<span data-ttu-id="6ee1b-116">Пакет лицензионных ключей относится к корпоративному соглашению корпоративного лицензирования для клиентов с 250 или более компьютеров.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-116">The license key pack is from an Enterprise volume license agreement for customers with 250 or more computers.</span></span> <span data-ttu-id="6ee1b-117">Параметр *сагриментнумбер* — номер регистрации (семь цифр), найденный в подписанном соглашении.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-117">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="6ee1b-118">2</span><span class="sxs-lookup"><span data-stu-id="6ee1b-118">2</span></span>
</dt> <dd>

<span data-ttu-id="6ee1b-119">Пакет лицензионных ключей относится к соглашению о корпоративном лицензировании для образовательных учреждений.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-119">The license key pack is from a Campus volume license agreement for a higher education institution.</span></span> <span data-ttu-id="6ee1b-120">Параметр *сагриментнумбер* — номер регистрации (семь цифр), найденный в подписанном соглашении.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-120">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="6ee1b-121">3</span><span class="sxs-lookup"><span data-stu-id="6ee1b-121">3</span></span>
</dt> <dd>

<span data-ttu-id="6ee1b-122">Пакет лицензионных ключей входит в состав учебного соглашения корпоративного лицензирования для основного и дополнительного учреждений.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-122">The license key pack is from a School volume license agreement for primary and secondary institutions.</span></span> <span data-ttu-id="6ee1b-123">Параметр *сагриментнумбер* — номер регистрации (семь цифр), найденный в подписанном соглашении.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-123">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="6ee1b-124">4</span><span class="sxs-lookup"><span data-stu-id="6ee1b-124">4</span></span>
</dt> <dd>

<span data-ttu-id="6ee1b-125">Пакет лицензионных ключей предоставляется лицензионным соглашением поставщика услуг для поставщиков услуг по ежемесячному лицензированию программного обеспечения Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-125">The license key pack is from a Service Provider license agreement for service providers to license Microsoft software on a monthly basis.</span></span> <span data-ttu-id="6ee1b-126">Параметр *сагриментнумбер* — номер регистрации (семь цифр), найденный в подписанном соглашении.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-126">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="6ee1b-127">5</span><span class="sxs-lookup"><span data-stu-id="6ee1b-127">5</span></span>
</dt> <dd>

<span data-ttu-id="6ee1b-128">Пакет лицензионных ключей относится к другому лицензионному соглашению, такому как открытая стоимость, открытая лицензия на несколько лет и открытая лицензия на подписку.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-128">The license key pack is from another license agreement, such as Open Value, Multi-Year Open License, and Open Subscription License.</span></span> <span data-ttu-id="6ee1b-129">Параметр *сагриментнумбер* — это номер соглашения, предоставленный в сведениях о программе.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-129">The *sAgreementNumber* parameter is the agreement number provided with your program information.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6ee1b-130">*сагриментнумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ee1b-130">*sAgreementNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ee1b-131">Номер соглашения или номер регистрации.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-131">Agreement number or enrollment number.</span></span> <span data-ttu-id="6ee1b-132">Параметр *сагриментнумбер* — это семь цифр числовая строка без дефисов.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-132">The *sAgreementNumber* parameter is a seven digit numeric string without hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="6ee1b-133">*ProductVersion* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ee1b-133">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ee1b-134">Номер версии продукта.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-134">Product version.</span></span>

<dt>

<span data-ttu-id="6ee1b-135">0</span><span class="sxs-lookup"><span data-stu-id="6ee1b-135">0</span></span>
</dt> <dd>

<span data-ttu-id="6ee1b-136">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-136">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="6ee1b-137">1</span><span class="sxs-lookup"><span data-stu-id="6ee1b-137">1</span></span>
</dt> <dd>

<span data-ttu-id="6ee1b-138">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-138">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="6ee1b-139">2</span><span class="sxs-lookup"><span data-stu-id="6ee1b-139">2</span></span>
</dt> <dd>

<span data-ttu-id="6ee1b-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ee1b-140">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6ee1b-141">*Продукттипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ee1b-141">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ee1b-142">Тип продукта.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-142">Product type.</span></span>

<dt>

<span data-ttu-id="6ee1b-143">0</span><span class="sxs-lookup"><span data-stu-id="6ee1b-143">0</span></span>
</dt> <dd>

<span data-ttu-id="6ee1b-144">Тип продукта пакета лицензионных ключей службы удаленных рабочих столов для каждого устройства.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-144">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="6ee1b-145">Таким образом, каждому устройству, которое подключается к серверу узла сеансов удаленных рабочих столов, должна быть назначена лицензия.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-145">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="6ee1b-146">1</span><span class="sxs-lookup"><span data-stu-id="6ee1b-146">1</span></span>
</dt> <dd>

<span data-ttu-id="6ee1b-147">Тип продукта пакета лицензионных ключей службы удаленных рабочих столов для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-147">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="6ee1b-148">Поэтому у каждого пользователя, подключающегося к серверу узла сеансов удаленных рабочих столов, должна быть лицензия.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-148">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="6ee1b-149">2</span><span class="sxs-lookup"><span data-stu-id="6ee1b-149">2</span></span>
</dt> <dd>

<span data-ttu-id="6ee1b-150">Недопустимый тип продукта.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-150">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6ee1b-151">*Лиценсекаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ee1b-151">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ee1b-152">Число устанавливаемых лицензий.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-152">Number of licenses to install.</span></span>

</dd> <dt>

<span data-ttu-id="6ee1b-153">*Кэйпаккид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6ee1b-153">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ee1b-154">Получает идентификатор пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-154">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ee1b-155">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ee1b-155">Return value</span></span>

<span data-ttu-id="6ee1b-156">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-156">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6ee1b-157">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-157">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6ee1b-158">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6ee1b-158">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ee1b-159">Требования</span><span class="sxs-lookup"><span data-stu-id="6ee1b-159">Requirements</span></span>



| <span data-ttu-id="6ee1b-160">Требование</span><span class="sxs-lookup"><span data-stu-id="6ee1b-160">Requirement</span></span> | <span data-ttu-id="6ee1b-161">Значение</span><span class="sxs-lookup"><span data-stu-id="6ee1b-161">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee1b-162">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ee1b-162">Minimum supported client</span></span><br/> | <span data-ttu-id="6ee1b-163">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6ee1b-163">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="6ee1b-164">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ee1b-164">Minimum supported server</span></span><br/> | <span data-ttu-id="6ee1b-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ee1b-165">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="6ee1b-166">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6ee1b-166">Namespace</span></span><br/>                | <span data-ttu-id="6ee1b-167">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="6ee1b-167">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="6ee1b-168">MOF</span><span class="sxs-lookup"><span data-stu-id="6ee1b-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ee1b-169"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ee1b-169"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ee1b-170">DLL</span><span class="sxs-lookup"><span data-stu-id="6ee1b-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ee1b-171"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ee1b-171"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ee1b-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ee1b-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ee1b-173">**\_Тслиценсекэйпакк Win32**</span><span class="sxs-lookup"><span data-stu-id="6ee1b-173">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





