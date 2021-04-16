---
title: Метод Импортлиценсекэйпаккоффлине класса Win32_TSLicenseKeyPack
description: Импорт с другого сервера лицензий удаленный рабочий стол, службы удаленных рабочих столов пакета лицензионных ключей, который использует идентификатор лицензии, полученный через Интернет или по телефону.
ms.assetid: 69D65917-8B82-4C24-AFFA-BBE529D3883C
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Импортлиценсекэйпаккоффлине
- Службы удаленных рабочих столов метода Импортлиценсекэйпаккоффлине, класс Win32_TSLicenseKeyPack
- Класс Win32_TSLicenseKeyPack службы удаленных рабочих столов, метод Импортлиценсекэйпаккоффлине
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de474cce6eb91cdc605588f7f4a63d97f985769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534256"
---
# <a name="importlicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="84041-106">Метод Импортлиценсекэйпаккоффлине \_ класса Win32 тслиценсекэйпакк</span><span class="sxs-lookup"><span data-stu-id="84041-106">ImportLicenseKeyPackOffline method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="84041-107">Импорт с другого сервера лицензий удаленный рабочий стол, службы удаленных рабочих столов пакета лицензионных ключей, который использует идентификатор лицензии, полученный через Интернет или по телефону.</span><span class="sxs-lookup"><span data-stu-id="84041-107">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that uses a license identifier that was received over the Internet or the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="84041-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84041-108">Syntax</span></span>


```mof
uint32 ImportLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="84041-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="84041-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84041-110">*слиценсекэйпаккид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84041-110">*sLicenseKeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84041-111">Содержит 35-символьный код лицензии.</span><span class="sxs-lookup"><span data-stu-id="84041-111">Contains the 35-character license code.</span></span> <span data-ttu-id="84041-112">В качестве входных данных должна быть указана только строка, состоящая из 35 символов.</span><span class="sxs-lookup"><span data-stu-id="84041-112">Only the 35-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="84041-113">Переносы не добавляются.</span><span class="sxs-lookup"><span data-stu-id="84041-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="84041-114">*ссаурцелснаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84041-114">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84041-115">Имя исходного удаленный рабочий стол сервера лицензирования.</span><span class="sxs-lookup"><span data-stu-id="84041-115">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="84041-116">Это либо полное различающееся имя, либо IP-адрес сервера.</span><span class="sxs-lookup"><span data-stu-id="84041-116">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="84041-117">*ссаурцелспродуктид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84041-117">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84041-118">Идентификатор сервера лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="84041-118">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="84041-119">— Это буквенно-цифровая строка, состоящая из 35 символов, которая не может содержать дефисы.</span><span class="sxs-lookup"><span data-stu-id="84041-119">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="84041-120">*Кэйпаккид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="84041-120">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84041-121">Получает идентификатор пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="84041-121">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84041-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84041-122">Return value</span></span>

<span data-ttu-id="84041-123">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="84041-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="84041-124">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="84041-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="84041-125">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="84041-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="84041-126">Требования</span><span class="sxs-lookup"><span data-stu-id="84041-126">Requirements</span></span>



| <span data-ttu-id="84041-127">Требование</span><span class="sxs-lookup"><span data-stu-id="84041-127">Requirement</span></span> | <span data-ttu-id="84041-128">Значение</span><span class="sxs-lookup"><span data-stu-id="84041-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="84041-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84041-129">Minimum supported client</span></span><br/> | <span data-ttu-id="84041-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="84041-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="84041-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84041-131">Minimum supported server</span></span><br/> | <span data-ttu-id="84041-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84041-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="84041-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="84041-133">Namespace</span></span><br/>                | <span data-ttu-id="84041-134">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="84041-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="84041-135">MOF</span><span class="sxs-lookup"><span data-stu-id="84041-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84041-136"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84041-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="84041-137">DLL</span><span class="sxs-lookup"><span data-stu-id="84041-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84041-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84041-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84041-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84041-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84041-140">**\_Тслиценсекэйпакк Win32**</span><span class="sxs-lookup"><span data-stu-id="84041-140">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





