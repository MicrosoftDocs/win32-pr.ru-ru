---
description: Позволяет владельцу доверенного платформенного модуля включить или возобновить работу доверенного платформенного модуля.
ms.assetid: 9fb0b0aa-a569-4c0c-859e-8640480dbb3e
title: Enable, метод класса Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Enable
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6fe79ee44cb2ef6494b770a53cb57f7b88943dc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264670"
---
# <a name="enable-method-of-the-win32_tpm-class"></a><span data-ttu-id="a6ee8-103">Enable, метод \_ класса TPM Win32</span><span class="sxs-lookup"><span data-stu-id="a6ee8-103">Enable method of the Win32\_Tpm class</span></span>

<span data-ttu-id="a6ee8-104">Метод **Enable** класса [**\_ TPM Win32**](win32-tpm.md) позволяет владельцу доверенного платформенного модуля включить или возобновить работу TPM.</span><span class="sxs-lookup"><span data-stu-id="a6ee8-104">The **Enable** method of the [**Win32\_Tpm**](win32-tpm.md) class allows the TPM owner to enable or resume the TPM.</span></span>

<span data-ttu-id="a6ee8-105">Для выполнения этого метода доверенный платформенный модуль уже должен иметь владельца.</span><span class="sxs-lookup"><span data-stu-id="a6ee8-105">To run this method, the TPM must already have an owner.</span></span> <span data-ttu-id="a6ee8-106">Чтобы включить доверенный платформенный модуль, который еще не имеет владельца, используйте метод [**сетфисикалпресенцерекуест**](setphysicalpresencerequest-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="a6ee8-106">To enable a TPM that does not already have an owner, use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6ee8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6ee8-107">Syntax</span></span>


```mof
uint32 Enable(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="a6ee8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6ee8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6ee8-109">*Овнераус* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="a6ee8-109">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a6ee8-110">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="a6ee8-110">Type: **string**</span></span>

<span data-ttu-id="a6ee8-111">Строка, идентифицирующая владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="a6ee8-111">A string that identifies the TPM owner.</span></span> <span data-ttu-id="a6ee8-112">Эта строка должна быть строкой в кодировке Base64, которая содержит ровно 20 байт двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="a6ee8-112">This string must be a base64-encoded string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="a6ee8-113">Используйте метод [**конверттувнераус**](converttoownerauth-win32-tpm.md) для преобразования парольной фразы в ожидаемый формат.</span><span class="sxs-lookup"><span data-stu-id="a6ee8-113">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="a6ee8-114">Параметр *овнераус* считывается из реестра, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="a6ee8-114">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6ee8-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a6ee8-115">Return value</span></span>

<span data-ttu-id="a6ee8-116">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a6ee8-116">Type: **uint32**</span></span>

<span data-ttu-id="a6ee8-117">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к базовым службам TPM.</span><span class="sxs-lookup"><span data-stu-id="a6ee8-117">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="a6ee8-118">В следующей таблице перечислены некоторые распространенные коды возврата.</span><span class="sxs-lookup"><span data-stu-id="a6ee8-118">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="a6ee8-119">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="a6ee8-119">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="a6ee8-120">Описание</span><span class="sxs-lookup"><span data-stu-id="a6ee8-120">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a6ee8-121"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="a6ee8-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="a6ee8-122">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="a6ee8-122">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="a6ee8-123"><dt>**Доверенный платформенный модуль \_ E \_ аусфаил**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="a6ee8-123"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>              | <span data-ttu-id="a6ee8-124">Предоставленное значение авторизации владельца не может выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="a6ee8-124">The provided owner authorization value cannot perform the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="a6ee8-125"><dt>**Доверенный платформенный модуль \_ \_Блокировка защиты \_ от \_ перезапуска**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="a6ee8-125"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="a6ee8-126">TPM защищается от атак из словарей и находится в течение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="a6ee8-126">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="a6ee8-127">Дополнительные сведения см. в описании метода [**ресетауслоккаут**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="a6ee8-127">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a6ee8-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6ee8-128">Remarks</span></span>

<span data-ttu-id="a6ee8-129">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="a6ee8-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a6ee8-130">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a6ee8-130">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="a6ee8-131">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="a6ee8-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a6ee8-132">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="a6ee8-132">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6ee8-133">Требования</span><span class="sxs-lookup"><span data-stu-id="a6ee8-133">Requirements</span></span>



| <span data-ttu-id="a6ee8-134">Требование</span><span class="sxs-lookup"><span data-stu-id="a6ee8-134">Requirement</span></span> | <span data-ttu-id="a6ee8-135">Значение</span><span class="sxs-lookup"><span data-stu-id="a6ee8-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ee8-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a6ee8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a6ee8-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a6ee8-137">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a6ee8-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a6ee8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a6ee8-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a6ee8-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a6ee8-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a6ee8-140">Namespace</span></span><br/>                | <span data-ttu-id="a6ee8-141">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="a6ee8-141">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="a6ee8-142">MOF</span><span class="sxs-lookup"><span data-stu-id="a6ee8-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6ee8-143"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6ee8-143"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6ee8-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a6ee8-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6ee8-145"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="a6ee8-145"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6ee8-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6ee8-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6ee8-147">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="a6ee8-147">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="a6ee8-148">**сетфисикалпресенцерекуест**</span><span class="sxs-lookup"><span data-stu-id="a6ee8-148">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
