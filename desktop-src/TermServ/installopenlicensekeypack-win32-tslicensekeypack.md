---
title: Метод Инсталлопенлиценсекэйпакк класса Win32_TSLicenseKeyPack
description: Устанавливает лицензию Open License службы удаленных рабочих столов лицензионный пакет.
ms.assetid: be50e25c-cda3-408b-934b-51ce343f3271
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Инсталлопенлиценсекэйпакк
- Службы удаленных рабочих столов метода Инсталлопенлиценсекэйпакк, класс Win32_TSLicenseKeyPack
- Класс Win32_TSLicenseKeyPack службы удаленных рабочих столов, метод Инсталлопенлиценсекэйпакк
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallOpenLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7335f25d3118c14f8cd0d27f72fd6a8d4cf1e0ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489837"
---
# <a name="installopenlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="ac5fa-106">Метод Инсталлопенлиценсекэйпакк \_ класса Win32 тслиценсекэйпакк</span><span class="sxs-lookup"><span data-stu-id="ac5fa-106">InstallOpenLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="ac5fa-107">Устанавливает лицензию Open License службы удаленных рабочих столов лицензионный пакет.</span><span class="sxs-lookup"><span data-stu-id="ac5fa-107">Installs an Open License Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac5fa-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac5fa-108">Syntax</span></span>


```mof
uint32 InstallOpenLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a><span data-ttu-id="ac5fa-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac5fa-109">Parameters</span></span>

<span data-ttu-id="ac5fa-110">*слиценсенумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac5fa-110">*sLicenseNumber* \[in\]</span></span>

<span data-ttu-id="ac5fa-111">8-символьная числовая строка, предоставленная вместе с пакетом лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="ac5fa-111">8-character numeric string that is provided with the license key pack.</span></span> <span data-ttu-id="ac5fa-112">Параметр *слиценсенумбер* не может содержать дефисы.</span><span class="sxs-lookup"><span data-stu-id="ac5fa-112">The *sLicenseNumber* parameter cannot contain hyphens.</span></span>

<span data-ttu-id="ac5fa-113">*саусоризатионнумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac5fa-113">*sAuthorizationNumber* \[in\]</span></span>

<span data-ttu-id="ac5fa-114">Строка, состоящая из 15 символов и имеющая ключ лицензии.</span><span class="sxs-lookup"><span data-stu-id="ac5fa-114">15-character alphanumeric string that is provided with the license key.</span></span> <span data-ttu-id="ac5fa-115">Параметр *саусоризатионнумбер* не может содержать дефисы.</span><span class="sxs-lookup"><span data-stu-id="ac5fa-115">The *sAuthorizationNumber* parameter cannot contain hyphens.</span></span>

<span data-ttu-id="ac5fa-116">*ProductVersion* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac5fa-116">*ProductVersion* \[in\]</span></span>

<span data-ttu-id="ac5fa-117">Номер версии продукта.</span><span class="sxs-lookup"><span data-stu-id="ac5fa-117">Product version.</span></span>

| <span data-ttu-id="ac5fa-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ac5fa-118">Value</span></span> | <span data-ttu-id="ac5fa-119">Описание</span><span class="sxs-lookup"><span data-stu-id="ac5fa-119">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="ac5fa-120">0</span><span class="sxs-lookup"><span data-stu-id="ac5fa-120">0</span></span> | <span data-ttu-id="ac5fa-121">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ac5fa-121">Not supported</span></span> |
| <span data-ttu-id="ac5fa-122">1</span><span class="sxs-lookup"><span data-stu-id="ac5fa-122">1</span></span> | <span data-ttu-id="ac5fa-123">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ac5fa-123">Not supported</span></span> |
| <span data-ttu-id="ac5fa-124">2</span><span class="sxs-lookup"><span data-stu-id="ac5fa-124">2</span></span> | <span data-ttu-id="ac5fa-125">Windows Server 2008/Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ac5fa-125">Windows Server 2008/Windows Server 2008 R2</span></span> |
| <span data-ttu-id="ac5fa-126">4</span><span class="sxs-lookup"><span data-stu-id="ac5fa-126">4</span></span> | <span data-ttu-id="ac5fa-127">Windows Server 2012/Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ac5fa-127">Windows Server 2012/Windows Server 2012 R2</span></span> |
| <span data-ttu-id="ac5fa-128">5</span><span class="sxs-lookup"><span data-stu-id="ac5fa-128">5</span></span> | <span data-ttu-id="ac5fa-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ac5fa-129">Windows Server 2016</span></span> |
| <span data-ttu-id="ac5fa-130">6</span><span class="sxs-lookup"><span data-stu-id="ac5fa-130">6</span></span> | <span data-ttu-id="ac5fa-131">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="ac5fa-131">Windows Server 2019</span></span> |

<span data-ttu-id="ac5fa-132">*Продукттипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac5fa-132">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac5fa-133">Тип продукта.</span><span class="sxs-lookup"><span data-stu-id="ac5fa-133">Product type.</span></span>

| <span data-ttu-id="ac5fa-134">Значение</span><span class="sxs-lookup"><span data-stu-id="ac5fa-134">Value</span></span> | <span data-ttu-id="ac5fa-135">Описание</span><span class="sxs-lookup"><span data-stu-id="ac5fa-135">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="ac5fa-136">0</span><span class="sxs-lookup"><span data-stu-id="ac5fa-136">0</span></span> | <span data-ttu-id="ac5fa-137">Тип продукта пакета лицензионных ключей службы удаленных рабочих столов для каждого устройства.</span><span class="sxs-lookup"><span data-stu-id="ac5fa-137">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="ac5fa-138">Таким образом, каждому устройству, которое подключается к серверу узла сеансов удаленных рабочих столов, должна быть назначена лицензия.</span><span class="sxs-lookup"><span data-stu-id="ac5fa-138">Therefore, each device that connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="ac5fa-139">1</span><span class="sxs-lookup"><span data-stu-id="ac5fa-139">1</span></span> | <span data-ttu-id="ac5fa-140">Тип продукта пакета лицензионных ключей службы удаленных рабочих столов для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="ac5fa-140">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="ac5fa-141">Поэтому у каждого пользователя, подключающегося к серверу узла сеансов удаленных рабочих столов, должна быть лицензия.</span><span class="sxs-lookup"><span data-stu-id="ac5fa-141">Therefore, each user who connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="ac5fa-142">2</span><span class="sxs-lookup"><span data-stu-id="ac5fa-142">2</span></span> | <span data-ttu-id="ac5fa-143">Недопустимый тип продукта.</span><span class="sxs-lookup"><span data-stu-id="ac5fa-143">This product type is not valid.</span></span> |

<span data-ttu-id="ac5fa-144">*Лиценсекаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac5fa-144">*LicenseCount* \[in\]</span></span>

<span data-ttu-id="ac5fa-145">Число устанавливаемых лицензий.</span><span class="sxs-lookup"><span data-stu-id="ac5fa-145">The number of licenses to install.</span></span>

<span data-ttu-id="ac5fa-146">*Кэйпаккид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ac5fa-146">*KeyPackId* \[out\]</span></span>

<span data-ttu-id="ac5fa-147">Получает идентификатор пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="ac5fa-147">Receives the key pack identifier.</span></span>

## <a name="return-value"></a><span data-ttu-id="ac5fa-148">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac5fa-148">Return value</span></span>

<span data-ttu-id="ac5fa-149">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="ac5fa-149">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ac5fa-150">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="ac5fa-150">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ac5fa-151">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ac5fa-151">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ac5fa-152">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac5fa-152">Remarks</span></span>

<span data-ttu-id="ac5fa-153">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="ac5fa-153">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ac5fa-154">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="ac5fa-154">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ac5fa-155">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="ac5fa-155">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ac5fa-156">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="ac5fa-156">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ac5fa-157">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ac5fa-157">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac5fa-158">Требования</span><span class="sxs-lookup"><span data-stu-id="ac5fa-158">Requirements</span></span>



| <span data-ttu-id="ac5fa-159">Требование</span><span class="sxs-lookup"><span data-stu-id="ac5fa-159">Requirement</span></span> | <span data-ttu-id="ac5fa-160">Значение</span><span class="sxs-lookup"><span data-stu-id="ac5fa-160">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac5fa-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac5fa-161">Minimum supported client</span></span><br/> | <span data-ttu-id="ac5fa-162">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ac5fa-162">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="ac5fa-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac5fa-163">Minimum supported server</span></span><br/> | <span data-ttu-id="ac5fa-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac5fa-164">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ac5fa-165">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ac5fa-165">Namespace</span></span><br/>                | <span data-ttu-id="ac5fa-166">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="ac5fa-166">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="ac5fa-167">MOF</span><span class="sxs-lookup"><span data-stu-id="ac5fa-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac5fa-168"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac5fa-168"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac5fa-169">DLL</span><span class="sxs-lookup"><span data-stu-id="ac5fa-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac5fa-170"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac5fa-170"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac5fa-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac5fa-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac5fa-172">**\_Тслиценсекэйпакк Win32**</span><span class="sxs-lookup"><span data-stu-id="ac5fa-172">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

