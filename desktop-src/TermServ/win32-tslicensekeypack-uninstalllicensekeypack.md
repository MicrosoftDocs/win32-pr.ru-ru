---
title: Метод Унинсталллиценсекэйпакк класса Win32_TSLicenseKeyPack
description: Удаляет службы удаленных рабочих столов пакет лицензионных ключей.
ms.assetid: AF429AD7-C0DB-40AC-A4C6-591699FBF7E7
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Унинсталллиценсекэйпакк
- Службы удаленных рабочих столов метода Унинсталллиценсекэйпакк, класс Win32_TSLicenseKeyPack
- Класс Win32_TSLicenseKeyPack службы удаленных рабочих столов, метод Унинсталллиценсекэйпакк
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.UninstallLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64754ea9ef2a32676b36821cf20c4f6871396415
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414829"
---
# <a name="uninstalllicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="d2d23-106">Метод Унинсталллиценсекэйпакк \_ класса Win32 тслиценсекэйпакк</span><span class="sxs-lookup"><span data-stu-id="d2d23-106">UninstallLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="d2d23-107">Удаляет службы удаленных рабочих столов пакет лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="d2d23-107">Uninstalls a Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2d23-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2d23-108">Syntax</span></span>


```mof
uint32 UninstallLicenseKeyPack(
  [in] unit32 ProductVersion,
  [in] unit32 ProductType,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a><span data-ttu-id="d2d23-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2d23-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2d23-110">*ProductVersion* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d2d23-110">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2d23-111">Идентификатор версии продукта для службы удаленных рабочих столов пакета лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="d2d23-111">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="d2d23-112">0</span><span class="sxs-lookup"><span data-stu-id="d2d23-112">0</span></span>
</dt> <dd>

<span data-ttu-id="d2d23-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d2d23-113">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d2d23-114">1</span><span class="sxs-lookup"><span data-stu-id="d2d23-114">1</span></span>
</dt> <dd>

<span data-ttu-id="d2d23-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d2d23-115">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d2d23-116">2</span><span class="sxs-lookup"><span data-stu-id="d2d23-116">2</span></span>
</dt> <dd>

<span data-ttu-id="d2d23-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2d23-117">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d2d23-118">*Продукттипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d2d23-118">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2d23-119">Тип продукта службы удаленных рабочих столов пакета лицензионных ключей.</span><span class="sxs-lookup"><span data-stu-id="d2d23-119">Product type of the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="d2d23-120">0</span><span class="sxs-lookup"><span data-stu-id="d2d23-120">0</span></span>
</dt> <dd>

<span data-ttu-id="d2d23-121">Тип продукта пакета лицензионных ключей службы удаленных рабочих столов для каждого устройства.</span><span class="sxs-lookup"><span data-stu-id="d2d23-121">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="d2d23-122">Таким образом, каждому устройству, которое подключается к серверу узла сеансов удаленных рабочих столов, должна быть назначена лицензия.</span><span class="sxs-lookup"><span data-stu-id="d2d23-122">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="d2d23-123">1</span><span class="sxs-lookup"><span data-stu-id="d2d23-123">1</span></span>
</dt> <dd>

<span data-ttu-id="d2d23-124">Тип продукта пакета лицензионных ключей службы удаленных рабочих столов для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="d2d23-124">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="d2d23-125">Поэтому у каждого пользователя, подключающегося к серверу узла сеансов удаленных рабочих столов, должна быть лицензия.</span><span class="sxs-lookup"><span data-stu-id="d2d23-125">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="d2d23-126">2</span><span class="sxs-lookup"><span data-stu-id="d2d23-126">2</span></span>
</dt> <dd>

<span data-ttu-id="d2d23-127">Недопустимый тип продукта.</span><span class="sxs-lookup"><span data-stu-id="d2d23-127">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d2d23-128">*Лиценсекаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d2d23-128">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2d23-129">Число удаляемых лицензий.</span><span class="sxs-lookup"><span data-stu-id="d2d23-129">The number of licenses to uninstall.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2d23-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2d23-130">Return value</span></span>

<span data-ttu-id="d2d23-131">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="d2d23-131">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d2d23-132">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="d2d23-132">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d2d23-133">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d2d23-133">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2d23-134">Требования</span><span class="sxs-lookup"><span data-stu-id="d2d23-134">Requirements</span></span>



| <span data-ttu-id="d2d23-135">Требование</span><span class="sxs-lookup"><span data-stu-id="d2d23-135">Requirement</span></span> | <span data-ttu-id="d2d23-136">Значение</span><span class="sxs-lookup"><span data-stu-id="d2d23-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2d23-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d2d23-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d2d23-138">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d2d23-138">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="d2d23-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d2d23-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d2d23-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2d23-140">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="d2d23-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d2d23-141">Namespace</span></span><br/>                | <span data-ttu-id="d2d23-142">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="d2d23-142">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="d2d23-143">MOF</span><span class="sxs-lookup"><span data-stu-id="d2d23-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2d23-144"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2d23-144"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2d23-145">DLL</span><span class="sxs-lookup"><span data-stu-id="d2d23-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2d23-146"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2d23-146"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2d23-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2d23-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2d23-148">**\_Тслиценсекэйпакк Win32**</span><span class="sxs-lookup"><span data-stu-id="d2d23-148">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





