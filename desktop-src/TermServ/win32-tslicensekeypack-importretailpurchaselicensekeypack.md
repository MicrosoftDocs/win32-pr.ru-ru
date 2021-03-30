---
title: Метод Импортретаилпурчаселиценсекэйпакк класса Win32_TSLicenseKeyPack
description: Импорт с другого сервера лицензий удаленный рабочий стол, службы удаленных рабочих столов пакета лицензионных ключей, приобретенного по розничному каналу.
ms.assetid: B45C3263-216E-4284-89A1-BE2ADE3A8E84
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Импортретаилпурчаселиценсекэйпакк
- Службы удаленных рабочих столов метода Импортретаилпурчаселиценсекэйпакк, класс Win32_TSLicenseKeyPack
- Класс Win32_TSLicenseKeyPack службы удаленных рабочих столов, метод Импортретаилпурчаселиценсекэйпакк
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2699d1f96827f9ace0f111a4c95adb64d5f8467e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802476"
---
# <a name="importretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="f6bbb-106">Метод Импортретаилпурчаселиценсекэйпакк \_ класса Win32 тслиценсекэйпакк</span><span class="sxs-lookup"><span data-stu-id="f6bbb-106">ImportRetailPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="f6bbb-107">Импорт с другого сервера лицензий удаленный рабочий стол, службы удаленных рабочих столов пакета лицензионных ключей, приобретенного по розничному каналу.</span><span class="sxs-lookup"><span data-stu-id="f6bbb-107">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6bbb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6bbb-108">Syntax</span></span>


```mof
uint32 ImportRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="f6bbb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6bbb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6bbb-110">*слиценсекоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6bbb-110">*sLicenseCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6bbb-111">Содержит 25-символьный код лицензии.</span><span class="sxs-lookup"><span data-stu-id="f6bbb-111">Contains the 25-character license code.</span></span> <span data-ttu-id="f6bbb-112">В качестве входных данных должно быть задано только 25-символьная строка символов.</span><span class="sxs-lookup"><span data-stu-id="f6bbb-112">Only the 25-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="f6bbb-113">Переносы не добавляются.</span><span class="sxs-lookup"><span data-stu-id="f6bbb-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="f6bbb-114">*ссаурцелснаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6bbb-114">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6bbb-115">Имя исходного удаленный рабочий стол сервера лицензирования.</span><span class="sxs-lookup"><span data-stu-id="f6bbb-115">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="f6bbb-116">Это либо полное различающееся имя, либо IP-адрес сервера.</span><span class="sxs-lookup"><span data-stu-id="f6bbb-116">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="f6bbb-117">*ссаурцелспродуктид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6bbb-117">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6bbb-118">Идентификатор сервера лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="f6bbb-118">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="f6bbb-119">— Это буквенно-цифровая строка, состоящая из 35 символов, которая не может содержать дефисы.</span><span class="sxs-lookup"><span data-stu-id="f6bbb-119">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="f6bbb-120">*Кэйпаккид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f6bbb-120">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6bbb-121">Получает идентификатор пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="f6bbb-121">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6bbb-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6bbb-122">Return value</span></span>

<span data-ttu-id="f6bbb-123">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="f6bbb-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f6bbb-124">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="f6bbb-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f6bbb-125">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f6bbb-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6bbb-126">Требования</span><span class="sxs-lookup"><span data-stu-id="f6bbb-126">Requirements</span></span>



| <span data-ttu-id="f6bbb-127">Требование</span><span class="sxs-lookup"><span data-stu-id="f6bbb-127">Requirement</span></span> | <span data-ttu-id="f6bbb-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f6bbb-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6bbb-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6bbb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f6bbb-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f6bbb-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f6bbb-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6bbb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f6bbb-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6bbb-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f6bbb-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f6bbb-133">Namespace</span></span><br/>                | <span data-ttu-id="f6bbb-134">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f6bbb-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="f6bbb-135">MOF</span><span class="sxs-lookup"><span data-stu-id="f6bbb-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6bbb-136"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6bbb-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6bbb-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f6bbb-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6bbb-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6bbb-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6bbb-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6bbb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6bbb-140">**\_Тслиценсекэйпакк Win32**</span><span class="sxs-lookup"><span data-stu-id="f6bbb-140">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





