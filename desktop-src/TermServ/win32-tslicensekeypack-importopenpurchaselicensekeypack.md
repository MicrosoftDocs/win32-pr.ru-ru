---
title: Метод Импортопенпурчаселиценсекэйпакк класса Win32_TSLicenseKeyPack
description: Импорт, с другого сервера лицензий удаленный рабочий стол — Open License службы удаленных рабочих столов пакет лицензионных ключей.
ms.assetid: FE1923FF-5292-4080-AB51-88B8A6B2322C
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Импортопенпурчаселиценсекэйпакк
- Службы удаленных рабочих столов метода Импортопенпурчаселиценсекэйпакк, класс Win32_TSLicenseKeyPack
- Класс Win32_TSLicenseKeyPack службы удаленных рабочих столов, метод Импортопенпурчаселиценсекэйпакк
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 944bb1ce63150caece2cbc247af24542fde2d4f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672859"
---
# <a name="importopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="4e966-106">Метод Импортопенпурчаселиценсекэйпакк \_ класса Win32 тслиценсекэйпакк</span><span class="sxs-lookup"><span data-stu-id="4e966-106">ImportOpenPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="4e966-107">Импорт, с другого сервера лицензий удаленный рабочий стол — Open License службы удаленных рабочих столов пакет лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="4e966-107">Imports, from another Remote Desktop license server, an Open License Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e966-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e966-108">Syntax</span></span>


```mof
uint32 ImportOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="4e966-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e966-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e966-110">*слиценсенумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4e966-110">*sLicenseNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e966-111">8-символьная числовая строка, предоставленная вместе с пакетом лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="4e966-111">8-character numeric string that is provided with the license key pack.</span></span> <span data-ttu-id="4e966-112">Параметр *слиценсенумбер* не может содержать дефисы.</span><span class="sxs-lookup"><span data-stu-id="4e966-112">The *sLicenseNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="4e966-113">*саусоризатионнумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4e966-113">*sAuthorizationNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e966-114">Строка, состоящая из 15 символов и имеющая ключ лицензии.</span><span class="sxs-lookup"><span data-stu-id="4e966-114">15-character alphanumeric string that is provided with the license key.</span></span> <span data-ttu-id="4e966-115">Параметр *саусоризатионнумбер* не может содержать дефисы.</span><span class="sxs-lookup"><span data-stu-id="4e966-115">The *sAuthorizationNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="4e966-116">*ProductVersion* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4e966-116">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e966-117">Номер версии продукта.</span><span class="sxs-lookup"><span data-stu-id="4e966-117">Product version.</span></span>

<dt>

<span data-ttu-id="4e966-118">0</span><span class="sxs-lookup"><span data-stu-id="4e966-118">0</span></span>
</dt> <dd>

<span data-ttu-id="4e966-119">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4e966-119">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4e966-120">1</span><span class="sxs-lookup"><span data-stu-id="4e966-120">1</span></span>
</dt> <dd>

<span data-ttu-id="4e966-121">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4e966-121">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4e966-122">2</span><span class="sxs-lookup"><span data-stu-id="4e966-122">2</span></span>
</dt> <dd>

<span data-ttu-id="4e966-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e966-123">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4e966-124">*Продукттипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4e966-124">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e966-125">Тип продукта.</span><span class="sxs-lookup"><span data-stu-id="4e966-125">Product type.</span></span>

<dt>

<span data-ttu-id="4e966-126">0</span><span class="sxs-lookup"><span data-stu-id="4e966-126">0</span></span>
</dt> <dd>

<span data-ttu-id="4e966-127">Тип продукта пакета лицензионных ключей службы удаленных рабочих столов для каждого устройства.</span><span class="sxs-lookup"><span data-stu-id="4e966-127">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="4e966-128">Таким образом, каждому устройству, которое подключается к серверу узла сеансов удаленных рабочих столов, должна быть назначена лицензия.</span><span class="sxs-lookup"><span data-stu-id="4e966-128">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="4e966-129">1</span><span class="sxs-lookup"><span data-stu-id="4e966-129">1</span></span>
</dt> <dd>

<span data-ttu-id="4e966-130">Тип продукта пакета лицензионных ключей службы удаленных рабочих столов для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="4e966-130">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="4e966-131">Поэтому у каждого пользователя, подключающегося к серверу узла сеансов удаленных рабочих столов, должна быть лицензия.</span><span class="sxs-lookup"><span data-stu-id="4e966-131">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="4e966-132">2</span><span class="sxs-lookup"><span data-stu-id="4e966-132">2</span></span>
</dt> <dd>

<span data-ttu-id="4e966-133">Недопустимый тип продукта.</span><span class="sxs-lookup"><span data-stu-id="4e966-133">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4e966-134">*Лиценсекаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4e966-134">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e966-135">Число импортируемых лицензий</span><span class="sxs-lookup"><span data-stu-id="4e966-135">The number of licenses to import</span></span>

</dd> <dt>

<span data-ttu-id="4e966-136">*ссаурцелснаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4e966-136">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e966-137">Имя исходного удаленный рабочий стол сервера лицензирования.</span><span class="sxs-lookup"><span data-stu-id="4e966-137">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="4e966-138">Это либо полное различающееся имя, либо IP-адрес сервера.</span><span class="sxs-lookup"><span data-stu-id="4e966-138">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="4e966-139">*ссаурцелспродуктид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4e966-139">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e966-140">Идентификатор сервера лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="4e966-140">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="4e966-141">— Это буквенно-цифровая строка, состоящая из 35 символов, которая не может содержать дефисы.</span><span class="sxs-lookup"><span data-stu-id="4e966-141">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="4e966-142">*Кэйпаккид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4e966-142">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e966-143">Получает идентификатор пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="4e966-143">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e966-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e966-144">Return value</span></span>

<span data-ttu-id="4e966-145">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="4e966-145">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="4e966-146">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="4e966-146">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="4e966-147">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4e966-147">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e966-148">Требования</span><span class="sxs-lookup"><span data-stu-id="4e966-148">Requirements</span></span>



| <span data-ttu-id="4e966-149">Требование</span><span class="sxs-lookup"><span data-stu-id="4e966-149">Requirement</span></span> | <span data-ttu-id="4e966-150">Значение</span><span class="sxs-lookup"><span data-stu-id="4e966-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e966-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e966-151">Minimum supported client</span></span><br/> | <span data-ttu-id="4e966-152">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4e966-152">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="4e966-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e966-153">Minimum supported server</span></span><br/> | <span data-ttu-id="4e966-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e966-154">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="4e966-155">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4e966-155">Namespace</span></span><br/>                | <span data-ttu-id="4e966-156">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="4e966-156">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="4e966-157">MOF</span><span class="sxs-lookup"><span data-stu-id="4e966-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e966-158"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e966-158"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e966-159">DLL</span><span class="sxs-lookup"><span data-stu-id="4e966-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e966-160"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e966-160"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e966-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e966-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e966-162">**\_Тслиценсекэйпакк Win32**</span><span class="sxs-lookup"><span data-stu-id="4e966-162">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





