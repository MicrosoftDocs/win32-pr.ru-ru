---
description: Импортирует сведения авторизации владельца для доверенного платформенного модуля, который уже принадлежит реестру операционной системы.
ms.assetid: 9611D363-6F10-48B9-B417-97133E975257
title: 'Метод Win32_Tpm:: Импортовнераус'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ImportOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: c74d99ab5cf101aa424dcf1921da774f53e21de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991015"
---
# <a name="win32_tpmimportownerauth-method"></a><span data-ttu-id="dcb48-103">\_Метод Win32 TPM:: импортовнераус</span><span class="sxs-lookup"><span data-stu-id="dcb48-103">Win32\_Tpm::ImportOwnerAuth method</span></span>

<span data-ttu-id="dcb48-104">Импортирует сведения авторизации владельца для доверенного платформенного модуля, который уже принадлежит реестру операционной системы.</span><span class="sxs-lookup"><span data-stu-id="dcb48-104">Imports the owner authorization information for a TPM that is already owned into the operating system registry.</span></span> <span data-ttu-id="dcb48-105">Эта операция сначала проверит, правильно ли указаны сведения авторизации владельца.</span><span class="sxs-lookup"><span data-stu-id="dcb48-105">This operation will first validate if the supplied owner authorization information is correct.</span></span> <span data-ttu-id="dcb48-106">Если это верно, метод импортирует эти сведения в реестр.</span><span class="sxs-lookup"><span data-stu-id="dcb48-106">If correct, the method imports this information to the registry.</span></span>

<span data-ttu-id="dcb48-107">Этот метод доступен только локальным администраторам.</span><span class="sxs-lookup"><span data-stu-id="dcb48-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcb48-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dcb48-108">Syntax</span></span>


```C++
uint32 ImportOwnerAuth(
  [in] STRING OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="dcb48-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="dcb48-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcb48-110">*Овнераус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dcb48-110">*OwnerAuth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcb48-111">Допустимые сведения авторизации владельца для TPM.</span><span class="sxs-lookup"><span data-stu-id="dcb48-111">The valid owner authorization information for the TPM.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcb48-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dcb48-112">Return value</span></span>

<span data-ttu-id="dcb48-113">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к [базовым службам TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="dcb48-113">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="dcb48-114">Ниже приведены общие коды возврата.</span><span class="sxs-lookup"><span data-stu-id="dcb48-114">Common return codes are listed below.</span></span>



| <span data-ttu-id="dcb48-115">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="dcb48-115">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="dcb48-116">Описание</span><span class="sxs-lookup"><span data-stu-id="dcb48-116">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="dcb48-117"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="dcb48-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="dcb48-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="dcb48-118">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dcb48-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dcb48-119">Remarks</span></span>

<span data-ttu-id="dcb48-120">Этот метод особенно полезен в сценариях, где доверенный платформенный модуль находится в состоянии "готов к снижению функциональности", и требует, чтобы импорт авторизации владельца был полностью готов или в сценариях с двойной загрузкой, где одна из операционных систем владеет доверенным платформенным модулем, а сведения авторизации владельца для TPM недоступны в другой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="dcb48-120">This method is particularly useful in the scenarios where the TPM is in a "ready with reduced functionality state " and requires the importing of the owner authorization to be fully ready or in a dual-boot scenarios where one of the operating systems has owned the TPM and the owner authorization information for TPM is not available in the other operating system.</span></span>

<span data-ttu-id="dcb48-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="dcb48-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="dcb48-122">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="dcb48-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="dcb48-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="dcb48-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="dcb48-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="dcb48-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dcb48-125">Требования</span><span class="sxs-lookup"><span data-stu-id="dcb48-125">Requirements</span></span>



| <span data-ttu-id="dcb48-126">Требование</span><span class="sxs-lookup"><span data-stu-id="dcb48-126">Requirement</span></span> | <span data-ttu-id="dcb48-127">Значение</span><span class="sxs-lookup"><span data-stu-id="dcb48-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcb48-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dcb48-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dcb48-129">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dcb48-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dcb48-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dcb48-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dcb48-131">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dcb48-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="dcb48-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dcb48-132">Namespace</span></span><br/>                | <span data-ttu-id="dcb48-133">\\\\.\\ корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="dcb48-133">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="dcb48-134">MOF</span><span class="sxs-lookup"><span data-stu-id="dcb48-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dcb48-135"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dcb48-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="dcb48-136">DLL</span><span class="sxs-lookup"><span data-stu-id="dcb48-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcb48-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="dcb48-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcb48-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dcb48-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcb48-139">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="dcb48-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
