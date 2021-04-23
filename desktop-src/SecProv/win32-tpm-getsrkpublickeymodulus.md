---
description: Возвращает модуль открытой части корневого ключа хранилища TPM.
ms.assetid: 266AE378-8BF2-4F6E-A055-E15D95E218DC
title: 'Метод Win32_Tpm:: Жетсркпубликкэймодулус'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetSrkPublicKeyModulus
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6d78abb695f2a9bc9de3887c8128395c2403b2b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663797"
---
# <a name="win32_tpmgetsrkpublickeymodulus-method"></a><span data-ttu-id="e5f2a-103">\_Метод Win32 TPM:: жетсркпубликкэймодулус</span><span class="sxs-lookup"><span data-stu-id="e5f2a-103">Win32\_Tpm::GetSrkPublicKeyModulus method</span></span>

<span data-ttu-id="e5f2a-104">Возвращает модуль открытой части корневого ключа хранилища TPM.</span><span class="sxs-lookup"><span data-stu-id="e5f2a-104">Gets the modulus of the public portion of the TPM Storage Root Key.</span></span>

<span data-ttu-id="e5f2a-105">Этот метод доступен только локальным администраторам.</span><span class="sxs-lookup"><span data-stu-id="e5f2a-105">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5f2a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5f2a-106">Syntax</span></span>


```C++
uint32 GetSrkPublicKeyModulus(
  [out] uint8 SrkPublicKeyModulus
);
```



## <a name="parameters"></a><span data-ttu-id="e5f2a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5f2a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5f2a-108">*Сркпубликкэймодулус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e5f2a-108">*SrkPublicKeyModulus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5f2a-109">Возвращает массив из 256 байт, содержащий модуль открытой части корневого ключа хранилища TPM</span><span class="sxs-lookup"><span data-stu-id="e5f2a-109">Returns a 256-byte array containing the modulus of the public portion of the TPM Storage Root Key</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5f2a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5f2a-110">Return value</span></span>

<span data-ttu-id="e5f2a-111">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к [базовым службам TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="e5f2a-111">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="e5f2a-112">Ниже приведены общие коды возврата.</span><span class="sxs-lookup"><span data-stu-id="e5f2a-112">Common return codes are listed below.</span></span>



| <span data-ttu-id="e5f2a-113">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="e5f2a-113">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="e5f2a-114">Описание</span><span class="sxs-lookup"><span data-stu-id="e5f2a-114">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="e5f2a-115"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="e5f2a-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="e5f2a-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="e5f2a-116">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e5f2a-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5f2a-117">Remarks</span></span>

<span data-ttu-id="e5f2a-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="e5f2a-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e5f2a-119">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e5f2a-119">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="e5f2a-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="e5f2a-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e5f2a-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="e5f2a-121">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5f2a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="e5f2a-122">Requirements</span></span>



| <span data-ttu-id="e5f2a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="e5f2a-123">Requirement</span></span> | <span data-ttu-id="e5f2a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e5f2a-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5f2a-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5f2a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e5f2a-126">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e5f2a-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e5f2a-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5f2a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e5f2a-128">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e5f2a-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e5f2a-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e5f2a-129">Namespace</span></span><br/>                | <span data-ttu-id="e5f2a-130">\\\\.\\ корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="e5f2a-130">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="e5f2a-131">MOF</span><span class="sxs-lookup"><span data-stu-id="e5f2a-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5f2a-132"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5f2a-132"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5f2a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e5f2a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5f2a-134"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="e5f2a-134"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5f2a-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5f2a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5f2a-136">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="e5f2a-136">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
