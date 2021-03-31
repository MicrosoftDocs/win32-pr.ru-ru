---
title: Метод Импортагриментлиценсекэйпакк класса Win32_TSLicenseKeyPack
description: Импорт, с другого сервера лицензий удаленный рабочий стол, службы удаленных рабочих столов пакета лицензионных ключей, приобретенного по лицензионному соглашению, и автоматически подключается через Интернет для проверки лицензии на пакет ключей.
ms.assetid: 3C29E691-3734-4D39-A89F-F381F285DC9E
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Импортагриментлиценсекэйпакк
- Службы удаленных рабочих столов метода Импортагриментлиценсекэйпакк, класс Win32_TSLicenseKeyPack
- Класс Win32_TSLicenseKeyPack службы удаленных рабочих столов, метод Импортагриментлиценсекэйпакк
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff61d022f9cf195eb357817f7733f4ec49e2986f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137495"
---
# <a name="importagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="83318-106">Метод Импортагриментлиценсекэйпакк \_ класса Win32 тслиценсекэйпакк</span><span class="sxs-lookup"><span data-stu-id="83318-106">ImportAgreementLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="83318-107">Импорт, с другого сервера лицензий удаленный рабочий стол, службы удаленных рабочих столов пакета лицензионных ключей, приобретенного по лицензионному соглашению, и автоматически подключается через Интернет для проверки лицензии на пакет ключей.</span><span class="sxs-lookup"><span data-stu-id="83318-107">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span>

## <a name="syntax"></a><span data-ttu-id="83318-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83318-108">Syntax</span></span>


```mof
uint32 ImportAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="83318-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="83318-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83318-110">*AgreementType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83318-110">*AgreementType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83318-111">Тип соглашения.</span><span class="sxs-lookup"><span data-stu-id="83318-111">Agreement type.</span></span>

<dt>

<span data-ttu-id="83318-112">0</span><span class="sxs-lookup"><span data-stu-id="83318-112">0</span></span>
</dt> <dd>

<span data-ttu-id="83318-113">Пакет лицензионных ключей относится к выбранному соглашению о корпоративном лицензировании (для клиентов с 250 или более компьютеров).</span><span class="sxs-lookup"><span data-stu-id="83318-113">The license key pack is from a Select volume license agreement (for customers with 250 or more computers).</span></span> <span data-ttu-id="83318-114">Параметр *сагриментнумбер* — номер регистрации (семь цифр), найденный в подписанном соглашении.</span><span class="sxs-lookup"><span data-stu-id="83318-114">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="83318-115">1</span><span class="sxs-lookup"><span data-stu-id="83318-115">1</span></span>
</dt> <dd>

<span data-ttu-id="83318-116">Пакет лицензионных ключей относится к корпоративному соглашению корпоративного лицензирования для клиентов с 250 или более компьютеров.</span><span class="sxs-lookup"><span data-stu-id="83318-116">The license key pack is from an Enterprise volume license agreement for customers with 250 or more computers.</span></span> <span data-ttu-id="83318-117">Параметр *сагриментнумбер* — номер регистрации (семь цифр), найденный в подписанном соглашении.</span><span class="sxs-lookup"><span data-stu-id="83318-117">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="83318-118">2</span><span class="sxs-lookup"><span data-stu-id="83318-118">2</span></span>
</dt> <dd>

<span data-ttu-id="83318-119">Пакет лицензионных ключей относится к соглашению о корпоративном лицензировании для образовательных учреждений.</span><span class="sxs-lookup"><span data-stu-id="83318-119">The license key pack is from a Campus volume license agreement for a higher education institution.</span></span> <span data-ttu-id="83318-120">Параметр *сагриментнумбер* — номер регистрации (семь цифр), найденный в подписанном соглашении.</span><span class="sxs-lookup"><span data-stu-id="83318-120">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="83318-121">3</span><span class="sxs-lookup"><span data-stu-id="83318-121">3</span></span>
</dt> <dd>

<span data-ttu-id="83318-122">Пакет лицензионных ключей входит в состав учебного соглашения корпоративного лицензирования для основного и дополнительного учреждений.</span><span class="sxs-lookup"><span data-stu-id="83318-122">The license key pack is from a School volume license agreement for primary and secondary institutions.</span></span> <span data-ttu-id="83318-123">Параметр *сагриментнумбер* — номер регистрации (семь цифр), найденный в подписанном соглашении.</span><span class="sxs-lookup"><span data-stu-id="83318-123">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="83318-124">4</span><span class="sxs-lookup"><span data-stu-id="83318-124">4</span></span>
</dt> <dd>

<span data-ttu-id="83318-125">Пакет лицензионных ключей предоставляется лицензионным соглашением поставщика услуг для поставщиков услуг по ежемесячному лицензированию программного обеспечения Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="83318-125">The license key pack is from a Service Provider license agreement for service providers to license Microsoft software on a monthly basis.</span></span> <span data-ttu-id="83318-126">Параметр *сагриментнумбер* — номер регистрации (семь цифр), найденный в подписанном соглашении.</span><span class="sxs-lookup"><span data-stu-id="83318-126">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="83318-127">5</span><span class="sxs-lookup"><span data-stu-id="83318-127">5</span></span>
</dt> <dd>

<span data-ttu-id="83318-128">Пакет лицензионных ключей относится к другому лицензионному соглашению, такому как открытая стоимость, открытая лицензия на несколько лет и открытая лицензия на подписку.</span><span class="sxs-lookup"><span data-stu-id="83318-128">The license key pack is from another license agreement, such as Open Value, Multi-Year Open License, and Open Subscription License.</span></span> <span data-ttu-id="83318-129">Параметр *сагриментнумбер* — это номер соглашения, предоставленный в сведениях о программе.</span><span class="sxs-lookup"><span data-stu-id="83318-129">The *sAgreementNumber* parameter is the agreement number provided with your program information.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="83318-130">*сагриментнумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83318-130">*sAgreementNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83318-131">Номер соглашения или номер регистрации.</span><span class="sxs-lookup"><span data-stu-id="83318-131">Agreement number or enrollment number.</span></span> <span data-ttu-id="83318-132">Параметр *сагриментнумбер* — это семь цифр числовая строка без дефисов.</span><span class="sxs-lookup"><span data-stu-id="83318-132">The *sAgreementNumber* parameter is a seven digit numeric string without hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="83318-133">*ProductVersion* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83318-133">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83318-134">Номер версии продукта.</span><span class="sxs-lookup"><span data-stu-id="83318-134">Product version.</span></span>

<dt>

<span data-ttu-id="83318-135">0</span><span class="sxs-lookup"><span data-stu-id="83318-135">0</span></span>
</dt> <dd>

<span data-ttu-id="83318-136">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="83318-136">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="83318-137">1</span><span class="sxs-lookup"><span data-stu-id="83318-137">1</span></span>
</dt> <dd>

<span data-ttu-id="83318-138">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="83318-138">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="83318-139">2</span><span class="sxs-lookup"><span data-stu-id="83318-139">2</span></span>
</dt> <dd>

<span data-ttu-id="83318-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83318-140">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="83318-141">*Продукттипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83318-141">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83318-142">Тип продукта.</span><span class="sxs-lookup"><span data-stu-id="83318-142">Product type.</span></span>

<dt>

<span data-ttu-id="83318-143">0</span><span class="sxs-lookup"><span data-stu-id="83318-143">0</span></span>
</dt> <dd>

<span data-ttu-id="83318-144">Тип продукта пакета лицензионных ключей службы удаленных рабочих столов для каждого устройства.</span><span class="sxs-lookup"><span data-stu-id="83318-144">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="83318-145">Таким образом, каждому устройству, которое подключается к серверу узла сеансов удаленных рабочих столов, должна быть назначена лицензия.</span><span class="sxs-lookup"><span data-stu-id="83318-145">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="83318-146">1</span><span class="sxs-lookup"><span data-stu-id="83318-146">1</span></span>
</dt> <dd>

<span data-ttu-id="83318-147">Тип продукта пакета лицензионных ключей службы удаленных рабочих столов для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="83318-147">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="83318-148">Поэтому у каждого пользователя, подключающегося к серверу узла сеансов удаленных рабочих столов, должна быть лицензия.</span><span class="sxs-lookup"><span data-stu-id="83318-148">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="83318-149">2</span><span class="sxs-lookup"><span data-stu-id="83318-149">2</span></span>
</dt> <dd>

<span data-ttu-id="83318-150">Недопустимый тип продукта.</span><span class="sxs-lookup"><span data-stu-id="83318-150">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="83318-151">*Лиценсекаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83318-151">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83318-152">Число импортируемых лицензий.</span><span class="sxs-lookup"><span data-stu-id="83318-152">Number of licenses to import.</span></span>

</dd> <dt>

<span data-ttu-id="83318-153">*ссаурцелснаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83318-153">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83318-154">Имя исходного удаленный рабочий стол сервера лицензирования.</span><span class="sxs-lookup"><span data-stu-id="83318-154">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="83318-155">Это либо полное различающееся имя, либо IP-адрес сервера.</span><span class="sxs-lookup"><span data-stu-id="83318-155">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="83318-156">*ссаурцелспродуктид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83318-156">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83318-157">Идентификатор сервера лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="83318-157">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="83318-158">— Это буквенно-цифровая строка, состоящая из 35 символов, которая не может содержать дефисы.</span><span class="sxs-lookup"><span data-stu-id="83318-158">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="83318-159">*Кэйпаккид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="83318-159">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83318-160">Получает идентификатор пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="83318-160">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83318-161">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83318-161">Return value</span></span>

<span data-ttu-id="83318-162">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="83318-162">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="83318-163">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="83318-163">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="83318-164">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="83318-164">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83318-165">Требования</span><span class="sxs-lookup"><span data-stu-id="83318-165">Requirements</span></span>



| <span data-ttu-id="83318-166">Требование</span><span class="sxs-lookup"><span data-stu-id="83318-166">Requirement</span></span> | <span data-ttu-id="83318-167">Значение</span><span class="sxs-lookup"><span data-stu-id="83318-167">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="83318-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83318-168">Minimum supported client</span></span><br/> | <span data-ttu-id="83318-169">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="83318-169">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="83318-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83318-170">Minimum supported server</span></span><br/> | <span data-ttu-id="83318-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83318-171">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="83318-172">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="83318-172">Namespace</span></span><br/>                | <span data-ttu-id="83318-173">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="83318-173">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="83318-174">MOF</span><span class="sxs-lookup"><span data-stu-id="83318-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83318-175"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83318-175"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="83318-176">DLL</span><span class="sxs-lookup"><span data-stu-id="83318-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83318-177"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83318-177"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83318-178">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83318-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83318-179">**\_Тслиценсекэйпакк Win32**</span><span class="sxs-lookup"><span data-stu-id="83318-179">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





