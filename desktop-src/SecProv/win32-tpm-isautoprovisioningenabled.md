---
description: Указывает, включен ли параметр автоматической подготовки доверенного платформенного модуля.
ms.assetid: C908673C-8BDB-4541-85C6-65FED1EBB535
title: 'Метод Win32_Tpm:: Исаутопровисионинженаблед'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsAutoProvisioningEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: cb269247292646464c6126a2588a50d77b19db9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911564"
---
# <a name="win32_tpmisautoprovisioningenabled-method"></a><span data-ttu-id="5d88a-103">\_Метод Win32 TPM:: исаутопровисионинженаблед</span><span class="sxs-lookup"><span data-stu-id="5d88a-103">Win32\_Tpm::IsAutoProvisioningEnabled method</span></span>

<span data-ttu-id="5d88a-104">Указывает, включен ли параметр автоматической подготовки доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="5d88a-104">Indicates if auto provisioning of the TPM is enabled.</span></span> <span data-ttu-id="5d88a-105">По умолчанию автоматическая подготовка включена для Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="5d88a-105">By default, auto provisioning is enabled for Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="5d88a-106">Этот метод доступен только локальным администраторам.</span><span class="sxs-lookup"><span data-stu-id="5d88a-106">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d88a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d88a-107">Syntax</span></span>


```C++
uint32 IsAutoProvisioningEnabled(
  [out] BOOL IsAutoProvisioningEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="5d88a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d88a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d88a-109">*Исаутопровисионинженаблед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5d88a-109">*IsAutoProvisioningEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d88a-110">Задайте **значение true** , если включена автоматическая подготовка TPM.</span><span class="sxs-lookup"><span data-stu-id="5d88a-110">Set to **TRUE** if the TPM auto provisioning is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d88a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d88a-111">Return value</span></span>

<span data-ttu-id="5d88a-112">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к [базовым службам TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="5d88a-112">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="5d88a-113">Ниже приведены общие коды возврата.</span><span class="sxs-lookup"><span data-stu-id="5d88a-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="5d88a-114">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="5d88a-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="5d88a-115">Описание</span><span class="sxs-lookup"><span data-stu-id="5d88a-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="5d88a-116"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5d88a-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="5d88a-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="5d88a-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5d88a-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d88a-118">Remarks</span></span>

<span data-ttu-id="5d88a-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="5d88a-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5d88a-120">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="5d88a-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5d88a-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="5d88a-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5d88a-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5d88a-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d88a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5d88a-123">Requirements</span></span>



| <span data-ttu-id="5d88a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5d88a-124">Requirement</span></span> | <span data-ttu-id="5d88a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5d88a-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d88a-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5d88a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5d88a-127">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5d88a-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5d88a-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5d88a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5d88a-129">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5d88a-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5d88a-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5d88a-130">Namespace</span></span><br/>                | <span data-ttu-id="5d88a-131">\\\\.\\ корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="5d88a-131">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="5d88a-132">MOF</span><span class="sxs-lookup"><span data-stu-id="5d88a-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d88a-133"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d88a-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d88a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5d88a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d88a-135"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="5d88a-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d88a-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d88a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d88a-137">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="5d88a-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
