---
description: Включает автоматическую подготовку доверенного платформенного модуля, если она в настоящее время отключена.
ms.assetid: 70F56A4C-F936-4CB6-83F6-F3B691F43B98
title: 'Метод Win32_Tpm:: Енаблеаутопровисионинг'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.EnableAutoProvisioning
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5288be5c9822b7e76b0cb25b60ee68dacc36d5e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343065"
---
# <a name="win32_tpmenableautoprovisioning-method"></a><span data-ttu-id="ffbda-103">\_Метод Win32 TPM:: енаблеаутопровисионинг</span><span class="sxs-lookup"><span data-stu-id="ffbda-103">Win32\_Tpm::EnableAutoProvisioning method</span></span>

<span data-ttu-id="ffbda-104">Включает автоматическую подготовку доверенного платформенного модуля, если она в настоящее время отключена.</span><span class="sxs-lookup"><span data-stu-id="ffbda-104">Enables auto provisioning of the TPM if it is currently disabled.</span></span> <span data-ttu-id="ffbda-105">Операция не действует, если автоматическая подготовка уже включена.</span><span class="sxs-lookup"><span data-stu-id="ffbda-105">The operation has no effect if auto provisioning is already enabled.</span></span> <span data-ttu-id="ffbda-106">По умолчанию автоматическая подготовка включена для Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ffbda-106">By default, auto provisioning is enabled for Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="ffbda-107">Этот метод доступен только локальным администраторам.</span><span class="sxs-lookup"><span data-stu-id="ffbda-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffbda-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ffbda-108">Syntax</span></span>


```C++
uint32 EnableAutoProvisioning();
```



## <a name="parameters"></a><span data-ttu-id="ffbda-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ffbda-109">Parameters</span></span>

<span data-ttu-id="ffbda-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="ffbda-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ffbda-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ffbda-111">Return value</span></span>

<span data-ttu-id="ffbda-112">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к [базовым службам TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="ffbda-112">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="ffbda-113">Ниже приведены общие коды возврата.</span><span class="sxs-lookup"><span data-stu-id="ffbda-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="ffbda-114">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="ffbda-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="ffbda-115">Описание</span><span class="sxs-lookup"><span data-stu-id="ffbda-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="ffbda-116"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ffbda-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="ffbda-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="ffbda-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ffbda-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ffbda-118">Remarks</span></span>

<span data-ttu-id="ffbda-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="ffbda-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ffbda-120">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="ffbda-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="ffbda-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="ffbda-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ffbda-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="ffbda-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ffbda-123">Требования</span><span class="sxs-lookup"><span data-stu-id="ffbda-123">Requirements</span></span>



| <span data-ttu-id="ffbda-124">Требование</span><span class="sxs-lookup"><span data-stu-id="ffbda-124">Requirement</span></span> | <span data-ttu-id="ffbda-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ffbda-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffbda-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ffbda-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ffbda-127">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ffbda-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ffbda-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ffbda-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ffbda-129">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ffbda-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ffbda-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ffbda-130">Namespace</span></span><br/>                | <span data-ttu-id="ffbda-131">\\\\.\\ корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="ffbda-131">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="ffbda-132">MOF</span><span class="sxs-lookup"><span data-stu-id="ffbda-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffbda-133"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffbda-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffbda-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ffbda-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffbda-135"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="ffbda-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffbda-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ffbda-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffbda-137">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="ffbda-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
