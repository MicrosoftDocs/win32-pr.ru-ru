---
description: Сбрасывает значение авторизации корневого ключа хранилища (SRK), чтобы оно было совместимо с операционной системой.
ms.assetid: af008733-b43c-4017-9e79-bdd98f2e20b6
title: Метод Ресетсркаус класса Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetSrkAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 7d838ded7051511b6a8f9117327ee7cdb1a00d7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348912"
---
# <a name="resetsrkauth-method-of-the-win32_tpm-class"></a><span data-ttu-id="ebb75-103">Метод Ресетсркаус \_ класса TPM Win32</span><span class="sxs-lookup"><span data-stu-id="ebb75-103">ResetSrkAuth method of the Win32\_Tpm class</span></span>

<span data-ttu-id="ebb75-104">Метод **ресетсркаус** класса [**\_ TPM Win32**](win32-tpm.md) сбрасывает значение авторизации корневого ключа хранилища (SRK), чтобы оно было совместимо с операционной системой.</span><span class="sxs-lookup"><span data-stu-id="ebb75-104">The **ResetSrkAuth** method of the [**Win32\_Tpm**](win32-tpm.md) class resets the Storage Root Key (SRK) authorization value to be compatible with the operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebb75-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebb75-105">Syntax</span></span>


```mof
uint32 ResetSrkAuth(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="ebb75-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ebb75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebb75-107">*Овнераус* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="ebb75-107">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ebb75-108">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="ebb75-108">Type: **string**</span></span>

<span data-ttu-id="ebb75-109">Строка, идентифицирующая владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="ebb75-109">A string that identifies the TPM owner.</span></span> <span data-ttu-id="ebb75-110">Эта строка должна быть строкой в кодировке Base64, завершающейся нулем, которая содержит ровно 20 байт двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="ebb75-110">This string must be a base64-encoded null-terminated string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="ebb75-111">Используйте метод [**конверттувнераус**](converttoownerauth-win32-tpm.md) для преобразования парольной фразы в ожидаемый формат.</span><span class="sxs-lookup"><span data-stu-id="ebb75-111">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="ebb75-112">Параметр *овнераус* считывается из реестра, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="ebb75-112">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebb75-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ebb75-113">Return value</span></span>

<span data-ttu-id="ebb75-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ebb75-114">Type: **uint32**</span></span>

<span data-ttu-id="ebb75-115">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к базовым службам TPM.</span><span class="sxs-lookup"><span data-stu-id="ebb75-115">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="ebb75-116">В следующей таблице перечислены некоторые распространенные коды возврата.</span><span class="sxs-lookup"><span data-stu-id="ebb75-116">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="ebb75-117">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="ebb75-117">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="ebb75-118">Описание</span><span class="sxs-lookup"><span data-stu-id="ebb75-118">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ebb75-119"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ebb75-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="ebb75-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="ebb75-120">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="ebb75-121"><dt> **TPM \_ E \_ аусфаил**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="ebb75-121"><dt>**TPM\_E\_AUTHFAIL** </dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>             | <span data-ttu-id="ebb75-122">Предоставленное значение авторизации владельца не может выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="ebb75-122">The provided owner authorization value cannot fulfill the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="ebb75-123"><dt>**Доверенный платформенный модуль \_ \_Блокировка защиты \_ от \_ перезапуска**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="ebb75-123"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="ebb75-124">TPM защищается от атак из словарей и находится в течение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="ebb75-124">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="ebb75-125">Дополнительные сведения см. в описании метода [**ресетауслоккаут**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="ebb75-125">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ebb75-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ebb75-126">Remarks</span></span>

<span data-ttu-id="ebb75-127">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="ebb75-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ebb75-128">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="ebb75-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="ebb75-129">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="ebb75-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ebb75-130">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="ebb75-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ebb75-131">Требования</span><span class="sxs-lookup"><span data-stu-id="ebb75-131">Requirements</span></span>



| <span data-ttu-id="ebb75-132">Требование</span><span class="sxs-lookup"><span data-stu-id="ebb75-132">Requirement</span></span> | <span data-ttu-id="ebb75-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ebb75-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebb75-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ebb75-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ebb75-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ebb75-135">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ebb75-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ebb75-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ebb75-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ebb75-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ebb75-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ebb75-138">Namespace</span></span><br/>                | <span data-ttu-id="ebb75-139">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="ebb75-139">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="ebb75-140">MOF</span><span class="sxs-lookup"><span data-stu-id="ebb75-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ebb75-141"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ebb75-141"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="ebb75-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ebb75-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebb75-143"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="ebb75-143"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebb75-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ebb75-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebb75-145">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="ebb75-145">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
