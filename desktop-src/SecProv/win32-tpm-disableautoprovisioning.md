---
description: Отключает автоматическую подготовку доверенного платформенного модуля, если в настоящее время он включен.
ms.assetid: 30CC2581-9C16-4A11-92F1-625992F2AF20
title: 'Win32_Tpm: метод:D Исаблеаутопровисионинг'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.DisableAutoProvisioning
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5387e744ec5f02bf448a997cfe1c8c83342903a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663798"
---
# <a name="win32_tpmdisableautoprovisioning-method"></a><span data-ttu-id="2cbfc-103">\_TPM Win32::D метод исаблеаутопровисионинг</span><span class="sxs-lookup"><span data-stu-id="2cbfc-103">Win32\_Tpm::DisableAutoProvisioning method</span></span>

<span data-ttu-id="2cbfc-104">Отключает автоматическую подготовку доверенного платформенного модуля, если в настоящее время он включен.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-104">Disables auto provisioning of the TPM if it is currently enabled.</span></span> <span data-ttu-id="2cbfc-105">Операция не действует, если автоматическая подготовка уже отключена.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-105">The operation has no effect if auto provisioning is already disabled.</span></span> <span data-ttu-id="2cbfc-106">По умолчанию автоматическая подготовка включена для Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-106">By default, auto provisioning is enabled for Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="2cbfc-107">Этот метод доступен только локальным администраторам.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cbfc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2cbfc-108">Syntax</span></span>


```C++
uint32 DisableAutoProvisioning(
  [in, optional] BOOL OnlyForNextBoot
);
```



## <a name="parameters"></a><span data-ttu-id="2cbfc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2cbfc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cbfc-110">*Онлифорнекстбут* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="2cbfc-110">*OnlyForNextBoot* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2cbfc-111">Если задано **значение true**, автоматическая подготовка отключена только для следующей загрузки.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-111">If set to **TRUE**, auto provisioning is disabled for only the next boot.</span></span> <span data-ttu-id="2cbfc-112">Если задано значение **false** или не указано, автоматическая подготовка будет отключена.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-112">If set to **FALSE** or not specified, auto provisioning is permanently disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cbfc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2cbfc-113">Return value</span></span>

<span data-ttu-id="2cbfc-114">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к [базовым службам TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="2cbfc-114">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="2cbfc-115">Ниже приведены общие коды возврата.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="2cbfc-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="2cbfc-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="2cbfc-117">Описание</span><span class="sxs-lookup"><span data-stu-id="2cbfc-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="2cbfc-118"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="2cbfc-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="2cbfc-119">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2cbfc-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2cbfc-120">Remarks</span></span>

<span data-ttu-id="2cbfc-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="2cbfc-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2cbfc-122">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="2cbfc-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2cbfc-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="2cbfc-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2cbfc-125">Требования</span><span class="sxs-lookup"><span data-stu-id="2cbfc-125">Requirements</span></span>



| <span data-ttu-id="2cbfc-126">Требование</span><span class="sxs-lookup"><span data-stu-id="2cbfc-126">Requirement</span></span> | <span data-ttu-id="2cbfc-127">Значение</span><span class="sxs-lookup"><span data-stu-id="2cbfc-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cbfc-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2cbfc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2cbfc-129">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2cbfc-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2cbfc-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2cbfc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2cbfc-131">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2cbfc-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2cbfc-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2cbfc-132">Namespace</span></span><br/>                | <span data-ttu-id="2cbfc-133">\\\\.\\ корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="2cbfc-133">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="2cbfc-134">MOF</span><span class="sxs-lookup"><span data-stu-id="2cbfc-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2cbfc-135"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2cbfc-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="2cbfc-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2cbfc-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cbfc-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="2cbfc-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cbfc-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2cbfc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cbfc-139">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="2cbfc-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
