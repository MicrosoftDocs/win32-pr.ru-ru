---
description: Возвращает отпечаток корневого ключа хранилища для данного модуля открытой части корневого ключа хранилища TPM.
ms.assetid: 08CBEB19-ECF5-4E43-B4A4-0F35987173E1
title: 'Метод Win32_Tpm:: Жетсркадсумбпринт'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetSrkADThumbprint
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 81e1ec53596a3d5ce469d412e9bd7ca17e1ad8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662283"
---
# <a name="win32_tpmgetsrkadthumbprint-method"></a><span data-ttu-id="4a7a5-103">\_Метод Win32 TPM:: жетсркадсумбпринт</span><span class="sxs-lookup"><span data-stu-id="4a7a5-103">Win32\_Tpm::GetSrkADThumbprint method</span></span>

<span data-ttu-id="4a7a5-104">Возвращает отпечаток корневого ключа хранилища для данного модуля открытой части корневого ключа хранилища TPM.</span><span class="sxs-lookup"><span data-stu-id="4a7a5-104">Gets the Storage root key thumbprint for a given modulus of the public portion of the TPM Storage Root Key.</span></span> <span data-ttu-id="4a7a5-105">Отпечаток используется для индексации корневых ключей хранилища на Active Directory сервере, если Active Directoryная резервная копия сведений о авторизации владельца доверенного платформенного модуля включена через параметр групповая политика.</span><span class="sxs-lookup"><span data-stu-id="4a7a5-105">The thumbprint is used to index the Storage Root Keys on the Active Directory server if the Active Directory backup of TPM owner authorization information is enabled through Group Policy setting.</span></span>

> [!Note]  
> <span data-ttu-id="4a7a5-106">Начиная с Windows 10 версии 1607, Авторизация владельца доверенного платформенного модуля никогда не зарезервирована на Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4a7a5-106">Beginning with Windows 10, version 1607, the TPM owner authorization is never backed up to Active Directory.</span></span>

 

<span data-ttu-id="4a7a5-107">Этот метод доступен только локальным администраторам.</span><span class="sxs-lookup"><span data-stu-id="4a7a5-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a7a5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a7a5-108">Syntax</span></span>


```C++
uint32 GetSrkADThumbprint(
  [in]  uint8 SrkPublicKeyModulus,
  [out] uint8 SrkADThumbprint
);
```



## <a name="parameters"></a><span data-ttu-id="4a7a5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a7a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a7a5-110">*Сркпубликкэймодулус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4a7a5-110">*SrkPublicKeyModulus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a7a5-111">Модуль открытой части корневого ключа хранилища TPM.</span><span class="sxs-lookup"><span data-stu-id="4a7a5-111">The modulus of the public portion of the TPM Storage Root Key.</span></span> <span data-ttu-id="4a7a5-112">Его также можно получить с помощью метода [**жетсркпубликкэймодулус**](win32-tpm-getsrkpublickeymodulus.md) класса [ \_ TPM Win32](win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="4a7a5-112">It can also be obtained using the [**GetSrkPublicKeyModulus**](win32-tpm-getsrkpublickeymodulus.md) method of the [Win32\_TPM](win32-tpm.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="4a7a5-113">*Сркадсумбпринт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4a7a5-113">*SrkADThumbprint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a7a5-114">Возвращает 20-байтовый массив, содержащий отпечаток корневого ключа хранилища для данного модуля.</span><span class="sxs-lookup"><span data-stu-id="4a7a5-114">Returns a 20-byte array containing the storage root key thumbprint for the given modulus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a7a5-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a7a5-115">Return value</span></span>

<span data-ttu-id="4a7a5-116">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к [базовым службам TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="4a7a5-116">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="4a7a5-117">Ниже приведены общие коды возврата.</span><span class="sxs-lookup"><span data-stu-id="4a7a5-117">Common return codes are listed below.</span></span>



| <span data-ttu-id="4a7a5-118">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="4a7a5-118">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="4a7a5-119">Описание</span><span class="sxs-lookup"><span data-stu-id="4a7a5-119">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="4a7a5-120"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="4a7a5-120"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="4a7a5-121">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="4a7a5-121">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4a7a5-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a7a5-122">Remarks</span></span>

<span data-ttu-id="4a7a5-123">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="4a7a5-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4a7a5-124">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4a7a5-124">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="4a7a5-125">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="4a7a5-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4a7a5-126">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="4a7a5-126">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4a7a5-127">Требования</span><span class="sxs-lookup"><span data-stu-id="4a7a5-127">Requirements</span></span>



| <span data-ttu-id="4a7a5-128">Требование</span><span class="sxs-lookup"><span data-stu-id="4a7a5-128">Requirement</span></span> | <span data-ttu-id="4a7a5-129">Значение</span><span class="sxs-lookup"><span data-stu-id="4a7a5-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a7a5-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a7a5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4a7a5-131">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4a7a5-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4a7a5-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a7a5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4a7a5-133">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4a7a5-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4a7a5-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4a7a5-134">Namespace</span></span><br/>                | <span data-ttu-id="4a7a5-135">\\\\.\\ корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="4a7a5-135">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="4a7a5-136">MOF</span><span class="sxs-lookup"><span data-stu-id="4a7a5-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a7a5-137"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4a7a5-137"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a7a5-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4a7a5-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a7a5-139"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="4a7a5-139"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a7a5-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a7a5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a7a5-141">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="4a7a5-141">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
