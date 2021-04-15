---
title: Метод Конвертлиценсес класса Win32_TSLicenseKeyPack
description: Преобразует лицензии в текущем ключевом пакете.
ms.assetid: 38600144-8fa2-4f9a-b7a4-7fafc304e7cb
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Конвертлиценсес
- Службы удаленных рабочих столов метода Конвертлиценсес, класс Win32_TSLicenseKeyPack
- Класс Win32_TSLicenseKeyPack службы удаленных рабочих столов, метод Конвертлиценсес
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ConvertLicenses
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f37b1d9804c5f14f89a7ff6b48f5f8fcbdc60b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414956"
---
# <a name="convertlicenses-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="dfd28-106">Метод Конвертлиценсес \_ класса Win32 тслиценсекэйпакк</span><span class="sxs-lookup"><span data-stu-id="dfd28-106">ConvertLicenses method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="dfd28-107">Преобразует лицензии в текущем ключевом пакете.</span><span class="sxs-lookup"><span data-stu-id="dfd28-107">Converts the licenses in the current key pack.</span></span> <span data-ttu-id="dfd28-108">Если лицензия является лицензией для каждого пользователя, она преобразуется в лицензию для каждого устройства.</span><span class="sxs-lookup"><span data-stu-id="dfd28-108">If the license is a per-user license, it is converted to a per-device license.</span></span> <span data-ttu-id="dfd28-109">Если лицензия является лицензией для каждого устройства, она преобразуется в лицензию для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="dfd28-109">If the license is a per-device license, it is converted to a per-user license.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfd28-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfd28-110">Syntax</span></span>


```mof
uint32 ConvertLicenses(
  [in]  uint32 Count,
  [out] uint32 KeypackID
);
```



## <a name="parameters"></a><span data-ttu-id="dfd28-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="dfd28-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfd28-112">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dfd28-112">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd28-113">Число лицензий для преобразования.</span><span class="sxs-lookup"><span data-stu-id="dfd28-113">The number of licenses to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="dfd28-114">*Кэйпаккид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dfd28-114">*KeypackID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd28-115">Идентификатор результирующего пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="dfd28-115">The identifier of the resultant key pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfd28-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dfd28-116">Return value</span></span>

<span data-ttu-id="dfd28-117">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="dfd28-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="dfd28-118">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="dfd28-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="dfd28-119">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="dfd28-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dfd28-120">Требования</span><span class="sxs-lookup"><span data-stu-id="dfd28-120">Requirements</span></span>



| <span data-ttu-id="dfd28-121">Требование</span><span class="sxs-lookup"><span data-stu-id="dfd28-121">Requirement</span></span> | <span data-ttu-id="dfd28-122">Значение</span><span class="sxs-lookup"><span data-stu-id="dfd28-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfd28-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dfd28-123">Minimum supported client</span></span><br/> | <span data-ttu-id="dfd28-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dfd28-124">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="dfd28-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dfd28-125">Minimum supported server</span></span><br/> | <span data-ttu-id="dfd28-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dfd28-126">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="dfd28-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dfd28-127">Namespace</span></span><br/>                | <span data-ttu-id="dfd28-128">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="dfd28-128">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="dfd28-129">MOF</span><span class="sxs-lookup"><span data-stu-id="dfd28-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dfd28-130"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dfd28-130"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="dfd28-131">DLL</span><span class="sxs-lookup"><span data-stu-id="dfd28-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfd28-132"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfd28-132"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfd28-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfd28-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfd28-134">**\_Тслиценсекэйпакк Win32**</span><span class="sxs-lookup"><span data-stu-id="dfd28-134">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





