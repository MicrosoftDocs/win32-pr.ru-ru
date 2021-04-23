---
description: Сбрасывает доверенный платформенный модуль до заводских состояний по умолчанию.
ms.assetid: 55d6702f-bd57-43e3-b790-617940dd2e01
title: Метод Clear класса Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Clear
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: cf75a8af6764e542cecd9bd296c1b1511c4f4513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265905"
---
# <a name="clear-method-of-the-win32_tpm-class"></a><span data-ttu-id="9040c-103">Метод Clear \_ класса TPM Win32</span><span class="sxs-lookup"><span data-stu-id="9040c-103">Clear method of the Win32\_Tpm class</span></span>

<span data-ttu-id="9040c-104">Метод **clear** класса [**\_ TPM Win32**](win32-tpm.md) сбрасывает доверенный платформенный модуль до заводских состояний по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9040c-104">The **Clear** method of the [**Win32\_Tpm**](win32-tpm.md) class resets the TPM to its factory-default state.</span></span> <span data-ttu-id="9040c-105">Владелец TPM может использовать этот метод, чтобы отменить владение TPM и сделать недействительными материалы по шифрованию, созданные предыдущим владельцем.</span><span class="sxs-lookup"><span data-stu-id="9040c-105">A TPM owner can use this method to cancel TPM ownership and invalidate cryptographic materials created by the previous owner.</span></span> <span data-ttu-id="9040c-106">Этот метод приостанавливает BitLocker, если вызов может привести к необходимости восстановления BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9040c-106">This method suspends BitLocker if calling could cause BitLocker recovery to be required.</span></span> <span data-ttu-id="9040c-107">BitLocker автоматически возобновит работу после подготовки TPM.</span><span class="sxs-lookup"><span data-stu-id="9040c-107">BitLocker would automatically resume once TPM has been provisioned.</span></span>

> [!Caution]  
> <span data-ttu-id="9040c-108">При очистке доверенного платформенного модуля будут потеряны все ключи доверенного платформенного модуля, созданные и используемые приложениями.</span><span class="sxs-lookup"><span data-stu-id="9040c-108">By clearing the TPM, you will lose all TPM keys created and used by applications.</span></span> <span data-ttu-id="9040c-109">Если эти ключи использовались для шифрования данных, убедитесь, что у вас есть другой способ доступа к данным перед очисткой доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="9040c-109">If these keys were used to encrypt data, ensure that you have another way to access the data before clearing the TPM.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9040c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9040c-110">Syntax</span></span>


```mof
uint32 Clear(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="9040c-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="9040c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9040c-112">*Овнераус* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9040c-112">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9040c-113">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="9040c-113">Type: **string**</span></span>

<span data-ttu-id="9040c-114">Строка, идентифицирующая владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="9040c-114">A string that identifies the TPM owner.</span></span> <span data-ttu-id="9040c-115">Эта строка должна быть строкой в кодировке Base64, которая содержит ровно 20 байт двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="9040c-115">This string must be a base64-encoded string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="9040c-116">Используйте метод [**конверттувнераус**](converttoownerauth-win32-tpm.md) для преобразования парольной фразы в ожидаемый формат.</span><span class="sxs-lookup"><span data-stu-id="9040c-116">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="9040c-117">Параметр *овнераус* считывается из реестра, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="9040c-117">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9040c-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9040c-118">Return value</span></span>

<span data-ttu-id="9040c-119">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9040c-119">Type: **uint32**</span></span>

<span data-ttu-id="9040c-120">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к базовым службам TPM.</span><span class="sxs-lookup"><span data-stu-id="9040c-120">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="9040c-121">В следующей таблице перечислены некоторые распространенные коды возврата.</span><span class="sxs-lookup"><span data-stu-id="9040c-121">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="9040c-122">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="9040c-122">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="9040c-123">Описание</span><span class="sxs-lookup"><span data-stu-id="9040c-123">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9040c-124"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="9040c-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="9040c-125">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="9040c-125">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="9040c-126"><dt>**Доверенный платформенный модуль \_ E \_ аусфаил**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="9040c-126"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>              | <span data-ttu-id="9040c-127">Предоставленное значение авторизации владельца не может выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="9040c-127">The provided owner authorization value cannot perform the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="9040c-128"><dt>**Доверенный платформенный модуль \_ \_Блокировка защиты \_ от \_ перезапуска**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="9040c-128"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="9040c-129">TPM защищается от атак из словарей и находится в течение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="9040c-129">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="9040c-130">Дополнительные сведения см. в описании метода [**ресетауслоккаут**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="9040c-130">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9040c-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9040c-131">Remarks</span></span>

<span data-ttu-id="9040c-132">Выполнение этого метода может помочь подготовить компьютер, оснащенный доверенным платформенным модулем, для повторного использования.</span><span class="sxs-lookup"><span data-stu-id="9040c-132">Running this method can help prepare a TPM-equipped computer for recycling.</span></span>

<span data-ttu-id="9040c-133">Чтобы очистить доверенный платформенный модуль, но у него больше нет авторизации владельца доверенного платформенного модуля, необходим физический доступ к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="9040c-133">To clear the TPM but no longer have the TPM owner authorization, you need physical access to the computer.</span></span> <span data-ttu-id="9040c-134">Метод [**сетфисикалпресенцерекуест**](setphysicalpresencerequest-win32-tpm.md) включает в себя функции для очистки доверенного платформенного модуля без авторизации владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="9040c-134">The [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method includes functionality to help clear the TPM without TPM owner authorization.</span></span>

<span data-ttu-id="9040c-135">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="9040c-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9040c-136">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="9040c-136">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="9040c-137">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="9040c-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9040c-138">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="9040c-138">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9040c-139">Требования</span><span class="sxs-lookup"><span data-stu-id="9040c-139">Requirements</span></span>



| <span data-ttu-id="9040c-140">Требование</span><span class="sxs-lookup"><span data-stu-id="9040c-140">Requirement</span></span> | <span data-ttu-id="9040c-141">Значение</span><span class="sxs-lookup"><span data-stu-id="9040c-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9040c-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9040c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="9040c-143">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9040c-143">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9040c-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9040c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="9040c-145">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9040c-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9040c-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9040c-146">Namespace</span></span><br/>                | <span data-ttu-id="9040c-147">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="9040c-147">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="9040c-148">MOF</span><span class="sxs-lookup"><span data-stu-id="9040c-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9040c-149"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9040c-149"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="9040c-150">DLL</span><span class="sxs-lookup"><span data-stu-id="9040c-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9040c-151"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="9040c-151"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9040c-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9040c-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9040c-153">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="9040c-153">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
