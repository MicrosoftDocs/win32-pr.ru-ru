---
title: Метод Ремовелиценсесвисидкаунт класса Win32_TSLicenseKeyPack
description: Удаляет указанное число лицензий службы удаленных рабочих столов из указанного пакета ключей.
ms.assetid: 36228659-7BE7-490A-A00C-A99FA66BFEB8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ремовелиценсесвисидкаунт
- Службы удаленных рабочих столов метода Ремовелиценсесвисидкаунт, класс Win32_TSLicenseKeyPack
- Класс Win32_TSLicenseKeyPack службы удаленных рабочих столов, метод Ремовелиценсесвисидкаунт
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.RemoveLicensesWithIdCount
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b2de1d1e0bfeed538e400436f8a88cd25ac563
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071214"
---
# <a name="removelicenseswithidcount-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="431db-106">Метод Ремовелиценсесвисидкаунт \_ класса Win32 тслиценсекэйпакк</span><span class="sxs-lookup"><span data-stu-id="431db-106">RemoveLicensesWithIdCount method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="431db-107">Удаляет указанное число лицензий службы удаленных рабочих столов из указанного пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="431db-107">Removes the specified number of Remote Desktop Services licenses from the specified key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="431db-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="431db-108">Syntax</span></span>


```mof
uint32 RemoveLicensesWithIdCount(
  [in] uint32 KeyPackId,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a><span data-ttu-id="431db-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="431db-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="431db-110">*Кэйпаккид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="431db-110">*KeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="431db-111">Идентификатор пакета ключей, содержащего удаляемые лицензии.</span><span class="sxs-lookup"><span data-stu-id="431db-111">The identifier of the key pack that contains the licenses to remove.</span></span>

</dd> <dt>

<span data-ttu-id="431db-112">*Лиценсекаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="431db-112">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="431db-113">Число удаляемых лицензий.</span><span class="sxs-lookup"><span data-stu-id="431db-113">The number of licenses to uninstall.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="431db-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="431db-114">Return value</span></span>

<span data-ttu-id="431db-115">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="431db-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="431db-116">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="431db-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="431db-117">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="431db-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="431db-118">Требования</span><span class="sxs-lookup"><span data-stu-id="431db-118">Requirements</span></span>



| <span data-ttu-id="431db-119">Требование</span><span class="sxs-lookup"><span data-stu-id="431db-119">Requirement</span></span> | <span data-ttu-id="431db-120">Значение</span><span class="sxs-lookup"><span data-stu-id="431db-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="431db-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="431db-121">Minimum supported client</span></span><br/> | <span data-ttu-id="431db-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="431db-122">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="431db-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="431db-123">Minimum supported server</span></span><br/> | <span data-ttu-id="431db-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="431db-124">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="431db-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="431db-125">Namespace</span></span><br/>                | <span data-ttu-id="431db-126">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="431db-126">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="431db-127">MOF</span><span class="sxs-lookup"><span data-stu-id="431db-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="431db-128"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="431db-128"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="431db-129">DLL</span><span class="sxs-lookup"><span data-stu-id="431db-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="431db-130"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="431db-130"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="431db-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="431db-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="431db-132">**\_Тслиценсекэйпакк Win32**</span><span class="sxs-lookup"><span data-stu-id="431db-132">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





