---
description: Позволяет владельцу доверенного платформенного модуля отключать или приостанавливать доверенный платформенный модуль.
ms.assetid: d910334d-6da6-423d-ae8d-6e86f300dd52
title: Метод Disable класса Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Disable
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 32012c338646ce11c96d2657233642808fdcdaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682566"
---
# <a name="disable-method-of-the-win32_tpm-class"></a><span data-ttu-id="6c336-103">Метод Disable \_ класса TPM Win32</span><span class="sxs-lookup"><span data-stu-id="6c336-103">Disable method of the Win32\_Tpm class</span></span>

<span data-ttu-id="6c336-104">Метод **Disable** класса [**\_ TPM Win32**](win32-tpm.md) позволяет владельцу доверенного платформенного модуля отключить или приостановить доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="6c336-104">The **Disable** method of the [**Win32\_Tpm**](win32-tpm.md) class allows the TPM owner to disable or suspend the TPM.</span></span> <span data-ttu-id="6c336-105">Этот метод приостанавливает BitLocker, если вызов может привести к необходимости восстановления BitLocker.</span><span class="sxs-lookup"><span data-stu-id="6c336-105">This method suspends BitLocker if calling could cause BitLocker recovery to be required.</span></span> <span data-ttu-id="6c336-106">BitLocker автоматически возобновит работу после подготовки TPM.</span><span class="sxs-lookup"><span data-stu-id="6c336-106">BitLocker would automatically resume once TPM has been provisioned.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c336-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c336-107">Syntax</span></span>


```mof
uint32 Disable(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="6c336-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c336-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c336-109">*Овнераус* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="6c336-109">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6c336-110">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="6c336-110">Type: **string**</span></span>

<span data-ttu-id="6c336-111">Строка, идентифицирующая владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="6c336-111">A string that identifies the TPM owner.</span></span> <span data-ttu-id="6c336-112">Эта строка должна быть строкой в кодировке Base64, которая содержит ровно 20 байт двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="6c336-112">This string must be a base64-encoded string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="6c336-113">Используйте метод [**конверттувнераус**](converttoownerauth-win32-tpm.md) для преобразования парольной фразы в ожидаемый формат.</span><span class="sxs-lookup"><span data-stu-id="6c336-113">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="6c336-114">Параметр *овнераус* считывается из реестра, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="6c336-114">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c336-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c336-115">Return value</span></span>

<span data-ttu-id="6c336-116">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c336-116">Type: **uint32**</span></span>

<span data-ttu-id="6c336-117">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к базовым службам TPM.</span><span class="sxs-lookup"><span data-stu-id="6c336-117">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="6c336-118">В следующей таблице перечислены некоторые распространенные коды возврата.</span><span class="sxs-lookup"><span data-stu-id="6c336-118">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="6c336-119">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="6c336-119">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="6c336-120">Описание</span><span class="sxs-lookup"><span data-stu-id="6c336-120">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c336-121"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6c336-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="6c336-122">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="6c336-122">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="6c336-123"><dt>**Доверенный платформенный модуль \_ E \_ аусфаил**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="6c336-123"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>              | <span data-ttu-id="6c336-124">Предоставленное значение авторизации владельца не может выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="6c336-124">The provided owner authorization value cannot perform the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="6c336-125"><dt>**Доверенный платформенный модуль \_ \_Блокировка защиты \_ от \_ перезапуска**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="6c336-125"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="6c336-126">TPM защищается от атак из словарей и находится в течение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="6c336-126">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="6c336-127">Дополнительные сведения см. в описании метода [**ресетауслоккаут**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="6c336-127">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6c336-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c336-128">Remarks</span></span>

<span data-ttu-id="6c336-129">Чтобы отключить доверенный платформенный модуль без значения авторизации владельца доверенного платформенного модуля, используйте метод [**сетфисикалпресенцерекуест**](setphysicalpresencerequest-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="6c336-129">To disable the TPM without having the TPM owner authorization value, use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span>

<span data-ttu-id="6c336-130">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="6c336-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6c336-131">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="6c336-131">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="6c336-132">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="6c336-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6c336-133">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="6c336-133">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c336-134">Требования</span><span class="sxs-lookup"><span data-stu-id="6c336-134">Requirements</span></span>



| <span data-ttu-id="6c336-135">Требование</span><span class="sxs-lookup"><span data-stu-id="6c336-135">Requirement</span></span> | <span data-ttu-id="6c336-136">Значение</span><span class="sxs-lookup"><span data-stu-id="6c336-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c336-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c336-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6c336-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6c336-138">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6c336-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c336-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6c336-140">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6c336-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6c336-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6c336-141">Namespace</span></span><br/>                | <span data-ttu-id="6c336-142">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="6c336-142">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="6c336-143">MOF</span><span class="sxs-lookup"><span data-stu-id="6c336-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c336-144"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c336-144"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c336-145">DLL</span><span class="sxs-lookup"><span data-stu-id="6c336-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c336-146"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="6c336-146"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c336-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c336-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c336-148">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="6c336-148">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="6c336-149">**сетфисикалпресенцерекуест**</span><span class="sxs-lookup"><span data-stu-id="6c336-149">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
