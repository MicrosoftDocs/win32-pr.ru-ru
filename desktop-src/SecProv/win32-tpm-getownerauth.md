---
description: Возвращает сведения о авторизации владельца для доверенного платформенного модуля, если он доступен в реестре.
ms.assetid: 3E2C28C8-4154-4B1B-9C47-AEDFD5622979
title: 'Метод Win32_Tpm:: Жетовнераус'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: a441b07af31758212152b657ccb033d8abdeebbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540914"
---
# <a name="win32_tpmgetownerauth-method"></a><span data-ttu-id="8bf70-103">\_Метод Win32 TPM:: жетовнераус</span><span class="sxs-lookup"><span data-stu-id="8bf70-103">Win32\_Tpm::GetOwnerAuth method</span></span>

<span data-ttu-id="8bf70-104">Возвращает сведения о авторизации владельца для доверенного платформенного модуля, если он доступен в реестре.</span><span class="sxs-lookup"><span data-stu-id="8bf70-104">Gets the owner authorization information for a TPM if one is available in the registry.</span></span> <span data-ttu-id="8bf70-105">Если TPM владеет или подготовлен в Windows 8 с параметрами по умолчанию, данные авторизации владельца доверенного платформенного модуля хранятся в реестре и доступны для использования этим методом.</span><span class="sxs-lookup"><span data-stu-id="8bf70-105">If a TPM is owned or provisioned in Windows 8 with the default settings, the TPM owner authorization information is stored in the registry and is available for use by this method.</span></span>

<span data-ttu-id="8bf70-106">Этот метод доступен только локальным администраторам.</span><span class="sxs-lookup"><span data-stu-id="8bf70-106">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bf70-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8bf70-107">Syntax</span></span>


```C++
uint32 GetOwnerAuth(
  [out] STRING OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="8bf70-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8bf70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bf70-109">*Овнераус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8bf70-109">*OwnerAuth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8bf70-110">Сведения о авторизации владельца для доверенного платформенного модуля, если он доступен в реестре.</span><span class="sxs-lookup"><span data-stu-id="8bf70-110">The owner authorization information for a TPM, if one is available in the registry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bf70-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8bf70-111">Return value</span></span>

<span data-ttu-id="8bf70-112">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к [базовым службам TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="8bf70-112">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="8bf70-113">Ниже приведены общие коды возврата.</span><span class="sxs-lookup"><span data-stu-id="8bf70-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="8bf70-114">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="8bf70-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="8bf70-115">Описание</span><span class="sxs-lookup"><span data-stu-id="8bf70-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="8bf70-116"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8bf70-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="8bf70-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="8bf70-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8bf70-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8bf70-118">Remarks</span></span>

<span data-ttu-id="8bf70-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="8bf70-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8bf70-120">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8bf70-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="8bf70-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="8bf70-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8bf70-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="8bf70-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8bf70-123">Требования</span><span class="sxs-lookup"><span data-stu-id="8bf70-123">Requirements</span></span>



| <span data-ttu-id="8bf70-124">Требование</span><span class="sxs-lookup"><span data-stu-id="8bf70-124">Requirement</span></span> | <span data-ttu-id="8bf70-125">Значение</span><span class="sxs-lookup"><span data-stu-id="8bf70-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf70-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8bf70-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8bf70-127">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8bf70-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8bf70-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8bf70-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8bf70-129">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8bf70-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8bf70-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8bf70-130">Namespace</span></span><br/>                | <span data-ttu-id="8bf70-131">\\\\.\\ корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="8bf70-131">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="8bf70-132">MOF</span><span class="sxs-lookup"><span data-stu-id="8bf70-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8bf70-133"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8bf70-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="8bf70-134">DLL</span><span class="sxs-lookup"><span data-stu-id="8bf70-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bf70-135"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="8bf70-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bf70-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8bf70-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bf70-137">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="8bf70-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
