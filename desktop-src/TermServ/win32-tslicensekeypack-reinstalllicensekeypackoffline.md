---
title: Метод Реинсталллиценсекэйпаккоффлине класса Win32_TSLicenseKeyPack
description: Переустанавливает пакет лицензионного ключа службы удаленных рабочих столов, который использует идентификатор лицензии, полученный через Интернет или по телефону.
ms.assetid: CFDB4C3B-C7C1-4670-BC87-92727057A500
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Реинсталллиценсекэйпаккоффлине
- Службы удаленных рабочих столов метода Реинсталллиценсекэйпаккоффлине, класс Win32_TSLicenseKeyPack
- Класс Win32_TSLicenseKeyPack службы удаленных рабочих столов, метод Реинсталллиценсекэйпаккоффлине
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e805521ea750c018ab2e7965e7fbfba05a92d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891533"
---
# <a name="reinstalllicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="7f7b5-106">Метод Реинсталллиценсекэйпаккоффлине \_ класса Win32 тслиценсекэйпакк</span><span class="sxs-lookup"><span data-stu-id="7f7b5-106">ReinstallLicenseKeyPackOffline method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="7f7b5-107">Переустанавливает пакет лицензионного ключа службы удаленных рабочих столов, который использует идентификатор лицензии, полученный через Интернет или по телефону.</span><span class="sxs-lookup"><span data-stu-id="7f7b5-107">Reinstalls a Remote Desktop Services license key pack that uses the license identifier that was received over the Internet or the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f7b5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f7b5-108">Syntax</span></span>


```mof
uint32 ReinstallLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="7f7b5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f7b5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f7b5-110">*слиценсекэйпаккид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7f7b5-110">*sLicenseKeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f7b5-111">Содержит 35-символьный код лицензии.</span><span class="sxs-lookup"><span data-stu-id="7f7b5-111">Contains the 35-character license code.</span></span> <span data-ttu-id="7f7b5-112">В качестве входных данных должна быть указана только строка, состоящая из 35 символов.</span><span class="sxs-lookup"><span data-stu-id="7f7b5-112">Only the 35-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="7f7b5-113">Переносы не добавляются.</span><span class="sxs-lookup"><span data-stu-id="7f7b5-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="7f7b5-114">*Кэйпаккид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7f7b5-114">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f7b5-115">Получает идентификатор пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="7f7b5-115">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f7b5-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f7b5-116">Return value</span></span>

<span data-ttu-id="7f7b5-117">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="7f7b5-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="7f7b5-118">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="7f7b5-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="7f7b5-119">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7f7b5-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f7b5-120">Требования</span><span class="sxs-lookup"><span data-stu-id="7f7b5-120">Requirements</span></span>



| <span data-ttu-id="7f7b5-121">Требование</span><span class="sxs-lookup"><span data-stu-id="7f7b5-121">Requirement</span></span> | <span data-ttu-id="7f7b5-122">Значение</span><span class="sxs-lookup"><span data-stu-id="7f7b5-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f7b5-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f7b5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7f7b5-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7f7b5-124">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="7f7b5-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f7b5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7f7b5-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f7b5-126">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="7f7b5-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7f7b5-127">Namespace</span></span><br/>                | <span data-ttu-id="7f7b5-128">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="7f7b5-128">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="7f7b5-129">MOF</span><span class="sxs-lookup"><span data-stu-id="7f7b5-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f7b5-130"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f7b5-130"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f7b5-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7f7b5-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f7b5-132"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f7b5-132"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f7b5-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f7b5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f7b5-134">**\_Тслиценсекэйпакк Win32**</span><span class="sxs-lookup"><span data-stu-id="7f7b5-134">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





