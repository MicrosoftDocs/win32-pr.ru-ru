---
title: Метод Реинсталлопенпурчаселиценсекэйпакк класса Win32_TSLicenseKeyPack
description: Переустанавливает открытый лицензионный пакет службы удаленных рабочих столов лицензионных ключей.
ms.assetid: 3E70711E-284A-466E-A733-1219F5E0B741
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Реинсталлопенпурчаселиценсекэйпакк
- Службы удаленных рабочих столов метода Реинсталлопенпурчаселиценсекэйпакк, класс Win32_TSLicenseKeyPack
- Класс Win32_TSLicenseKeyPack службы удаленных рабочих столов, метод Реинсталлопенпурчаселиценсекэйпакк
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1eae765b74feed98760ef30c2b89a1090c4200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803604"
---
# <a name="reinstallopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="f8f04-106">Метод Реинсталлопенпурчаселиценсекэйпакк \_ класса Win32 тслиценсекэйпакк</span><span class="sxs-lookup"><span data-stu-id="f8f04-106">ReinstallOpenPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="f8f04-107">Переустанавливает открытый лицензионный пакет службы удаленных рабочих столов лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="f8f04-107">Reinstalls an Open License Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8f04-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8f04-108">Syntax</span></span>


```mof
uint32 ReinstallOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="f8f04-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8f04-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8f04-110">*слиценсенумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8f04-110">*sLicenseNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8f04-111">8-символьная числовая строка, предоставленная вместе с пакетом лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="f8f04-111">8-character numeric string that is provided with the license key pack.</span></span> <span data-ttu-id="f8f04-112">Параметр *слиценсенумбер* не может содержать дефисы.</span><span class="sxs-lookup"><span data-stu-id="f8f04-112">The *sLicenseNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="f8f04-113">*саусоризатионнумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8f04-113">*sAuthorizationNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8f04-114">Строка, состоящая из 15 символов и имеющая ключ лицензии.</span><span class="sxs-lookup"><span data-stu-id="f8f04-114">15-character alphanumeric string that is provided with the license key.</span></span> <span data-ttu-id="f8f04-115">Параметр *саусоризатионнумбер* не может содержать дефисы.</span><span class="sxs-lookup"><span data-stu-id="f8f04-115">The *sAuthorizationNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="f8f04-116">*ProductVersion* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8f04-116">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8f04-117">Номер версии продукта.</span><span class="sxs-lookup"><span data-stu-id="f8f04-117">Product version.</span></span>

<dt>

<span data-ttu-id="f8f04-118">0</span><span class="sxs-lookup"><span data-stu-id="f8f04-118">0</span></span>
</dt> <dd>

<span data-ttu-id="f8f04-119">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f8f04-119">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f8f04-120">1</span><span class="sxs-lookup"><span data-stu-id="f8f04-120">1</span></span>
</dt> <dd>

<span data-ttu-id="f8f04-121">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f8f04-121">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f8f04-122">2</span><span class="sxs-lookup"><span data-stu-id="f8f04-122">2</span></span>
</dt> <dd>

<span data-ttu-id="f8f04-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8f04-123">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f8f04-124">*Продукттипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8f04-124">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8f04-125">Тип продукта.</span><span class="sxs-lookup"><span data-stu-id="f8f04-125">Product type.</span></span>

<dt>

<span data-ttu-id="f8f04-126">0</span><span class="sxs-lookup"><span data-stu-id="f8f04-126">0</span></span>
</dt> <dd>

<span data-ttu-id="f8f04-127">Тип продукта пакета лицензионных ключей службы удаленных рабочих столов для каждого устройства.</span><span class="sxs-lookup"><span data-stu-id="f8f04-127">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="f8f04-128">Таким образом, каждому устройству, которое подключается к серверу узла сеансов удаленных рабочих столов, должна быть назначена лицензия.</span><span class="sxs-lookup"><span data-stu-id="f8f04-128">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="f8f04-129">1</span><span class="sxs-lookup"><span data-stu-id="f8f04-129">1</span></span>
</dt> <dd>

<span data-ttu-id="f8f04-130">Тип продукта пакета лицензионных ключей службы удаленных рабочих столов для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="f8f04-130">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="f8f04-131">Поэтому у каждого пользователя, подключающегося к серверу узла сеансов удаленных рабочих столов, должна быть лицензия.</span><span class="sxs-lookup"><span data-stu-id="f8f04-131">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="f8f04-132">2</span><span class="sxs-lookup"><span data-stu-id="f8f04-132">2</span></span>
</dt> <dd>

<span data-ttu-id="f8f04-133">Недопустимый тип продукта.</span><span class="sxs-lookup"><span data-stu-id="f8f04-133">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f8f04-134">*Лиценсекаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8f04-134">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8f04-135">Число устанавливаемых лицензий.</span><span class="sxs-lookup"><span data-stu-id="f8f04-135">The number of licenses to install.</span></span>

</dd> <dt>

<span data-ttu-id="f8f04-136">*Кэйпаккид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f8f04-136">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8f04-137">Получает идентификатор пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="f8f04-137">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8f04-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8f04-138">Return value</span></span>

<span data-ttu-id="f8f04-139">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="f8f04-139">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f8f04-140">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="f8f04-140">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f8f04-141">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f8f04-141">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8f04-142">Требования</span><span class="sxs-lookup"><span data-stu-id="f8f04-142">Requirements</span></span>



| <span data-ttu-id="f8f04-143">Требование</span><span class="sxs-lookup"><span data-stu-id="f8f04-143">Requirement</span></span> | <span data-ttu-id="f8f04-144">Значение</span><span class="sxs-lookup"><span data-stu-id="f8f04-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8f04-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8f04-145">Minimum supported client</span></span><br/> | <span data-ttu-id="f8f04-146">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f8f04-146">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f8f04-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8f04-147">Minimum supported server</span></span><br/> | <span data-ttu-id="f8f04-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8f04-148">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f8f04-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f8f04-149">Namespace</span></span><br/>                | <span data-ttu-id="f8f04-150">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f8f04-150">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="f8f04-151">MOF</span><span class="sxs-lookup"><span data-stu-id="f8f04-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8f04-152"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8f04-152"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8f04-153">DLL</span><span class="sxs-lookup"><span data-stu-id="f8f04-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8f04-154"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8f04-154"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8f04-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8f04-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8f04-156">**\_Тслиценсекэйпакк Win32**</span><span class="sxs-lookup"><span data-stu-id="f8f04-156">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





