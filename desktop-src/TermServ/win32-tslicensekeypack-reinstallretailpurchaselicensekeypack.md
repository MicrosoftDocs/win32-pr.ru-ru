---
title: Метод Реинсталлретаилпурчаселиценсекэйпакк класса Win32_TSLicenseKeyPack
description: Переустанавливает пакет лицензионных ключей службы удаленных рабочих столов, приобретенный по розничному каналу.
ms.assetid: 19528726-8DEB-4D03-BFA6-647C8A612FA2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Реинсталлретаилпурчаселиценсекэйпакк
- Службы удаленных рабочих столов метода Реинсталлретаилпурчаселиценсекэйпакк, класс Win32_TSLicenseKeyPack
- Класс Win32_TSLicenseKeyPack службы удаленных рабочих столов, метод Реинсталлретаилпурчаселиценсекэйпакк
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4caa8635eaf28ad823add500883832a7fe885b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071215"
---
# <a name="reinstallretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="f3e2e-106">Метод Реинсталлретаилпурчаселиценсекэйпакк \_ класса Win32 тслиценсекэйпакк</span><span class="sxs-lookup"><span data-stu-id="f3e2e-106">ReinstallRetailPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="f3e2e-107">Переустанавливает пакет лицензионных ключей службы удаленных рабочих столов, приобретенный по розничному каналу.</span><span class="sxs-lookup"><span data-stu-id="f3e2e-107">Reinstalls a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3e2e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3e2e-108">Syntax</span></span>


```mof
uint32 ReinstallRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="f3e2e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3e2e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3e2e-110">*слиценсекоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f3e2e-110">*sLicenseCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e2e-111">Содержит 25-символьный код лицензии.</span><span class="sxs-lookup"><span data-stu-id="f3e2e-111">Contains the 25-character license code.</span></span> <span data-ttu-id="f3e2e-112">В качестве входных данных должно быть задано только 25-символьная строка символов.</span><span class="sxs-lookup"><span data-stu-id="f3e2e-112">Only the 25-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="f3e2e-113">Переносы не добавляются.</span><span class="sxs-lookup"><span data-stu-id="f3e2e-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="f3e2e-114">*Кэйпаккид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f3e2e-114">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e2e-115">Получает идентификатор пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="f3e2e-115">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3e2e-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3e2e-116">Return value</span></span>

<span data-ttu-id="f3e2e-117">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="f3e2e-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f3e2e-118">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="f3e2e-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f3e2e-119">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f3e2e-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3e2e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="f3e2e-120">Requirements</span></span>



| <span data-ttu-id="f3e2e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="f3e2e-121">Requirement</span></span> | <span data-ttu-id="f3e2e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="f3e2e-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3e2e-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f3e2e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f3e2e-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f3e2e-124">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f3e2e-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f3e2e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f3e2e-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3e2e-126">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f3e2e-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f3e2e-127">Namespace</span></span><br/>                | <span data-ttu-id="f3e2e-128">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f3e2e-128">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="f3e2e-129">MOF</span><span class="sxs-lookup"><span data-stu-id="f3e2e-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3e2e-130"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3e2e-130"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3e2e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f3e2e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3e2e-132"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3e2e-132"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3e2e-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3e2e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3e2e-134">**\_Тслиценсекэйпакк Win32**</span><span class="sxs-lookup"><span data-stu-id="f3e2e-134">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





