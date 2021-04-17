---
description: Сбрасывает время ожидания или другой механизм, реализуемый производителями TPM для защиты от атак из словаря на основе значений авторизации доверенного платформенного модуля.
ms.assetid: c2fba6a2-2d03-4ffd-9841-4a9eac0a20ac
title: Метод Ресетауслоккаут класса Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetAuthLockOut
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d28287e410fbaf65ce5b1e617113c35cfece160b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662290"
---
# <a name="resetauthlockout-method-of-the-win32_tpm-class"></a><span data-ttu-id="266f1-103">Метод Ресетауслоккаут \_ класса TPM Win32</span><span class="sxs-lookup"><span data-stu-id="266f1-103">ResetAuthLockOut method of the Win32\_Tpm class</span></span>

<span data-ttu-id="266f1-104">Метод **ресетауслоккаут** класса [**\_ TPM Win32**](win32-tpm.md) сбрасывает период времени ожидания или другой механизм, реализуемый производителями TPM для защиты от атак из словаря на основе значений авторизации доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="266f1-104">The **ResetAuthLockOut** method of the [**Win32\_Tpm**](win32-tpm.md) class resets the time-out period or other mechanism that TPM manufacturers implement to protect against dictionary attacks on TPM authorization values.</span></span> <span data-ttu-id="266f1-105">При атаке по словарю злоумышленник пытается угадать правильное значение авторизации TPM, выполнив неполную попытку выполнить все возможные значения.</span><span class="sxs-lookup"><span data-stu-id="266f1-105">In a dictionary attack, an attacker tries to guess a correct TPM authorization value by exhaustively attempting all possible values.</span></span>

<span data-ttu-id="266f1-106">Используйте этот метод, если доверенный платформенный модуль заблокирован из-за слишком большого числа неудачных попыток входа в систему авторизации владельца или других значений авторизации.</span><span class="sxs-lookup"><span data-stu-id="266f1-106">Use this method if the TPM is locked out due to too many incorrect attempts at entering the owner authorization or other authorization values.</span></span> <span data-ttu-id="266f1-107">Если доверенный платформенный модуль заблокирован, некоторые или все команды, выданные доверенному платформенному модулю, будут возвращать ошибку, а \_ \_ Блокировка защиты от TPM 0x80280803 — \_ \_ запущена.</span><span class="sxs-lookup"><span data-stu-id="266f1-107">When the TPM is locked out, some or all commands issued to the TPM will return an error, TPM\_E\_DEFEND\_LOCK\_RUNNING (0x80280803).</span></span>

> [!Note]  
> <span data-ttu-id="266f1-108">Этот метод можно использовать только один раз, если доверенный платформенный модуль заблокирован. Если авторизация владельца, предоставленная этому методу, неверна, доверенный платформенный модуль блокируется на весь период ожидания, а дополнительные попытки сброса блокировки завершатся неудачей.</span><span class="sxs-lookup"><span data-stu-id="266f1-108">This method can only be used exactly once when the TPM is locked out. If the owner authorization provided to this method is incorrect, the TPM will lock out for the entire time-out period and additional attempts at resetting the lock will fail.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="266f1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="266f1-109">Syntax</span></span>


```mof
uint32 ResetAuthLockOut(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="266f1-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="266f1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="266f1-111">*Овнераус* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="266f1-111">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="266f1-112">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="266f1-112">Type: **string**</span></span>

<span data-ttu-id="266f1-113">Строка, идентифицирующая владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="266f1-113">A string that identifies the TPM owner.</span></span>

<span data-ttu-id="266f1-114">Эта строка должна быть строкой в кодировке Base64, завершающейся нулем, которая содержит ровно 20 байт двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="266f1-114">This string must be a base64-encoded null-terminated string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="266f1-115">Используйте метод [**конверттувнераус**](converttoownerauth-win32-tpm.md) для преобразования парольной фразы в ожидаемый формат.</span><span class="sxs-lookup"><span data-stu-id="266f1-115">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="266f1-116">Параметр *овнераус* считывается из реестра, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="266f1-116">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="266f1-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="266f1-117">Return value</span></span>

<span data-ttu-id="266f1-118">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="266f1-118">Type: **uint32**</span></span>

<span data-ttu-id="266f1-119">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к базовым службам TPM.</span><span class="sxs-lookup"><span data-stu-id="266f1-119">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span> <span data-ttu-id="266f1-120">В следующей таблице перечислены некоторые из стандартных возвращаемых значений.</span><span class="sxs-lookup"><span data-stu-id="266f1-120">The following table lists some of the common return values.</span></span>



| <span data-ttu-id="266f1-121">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="266f1-121">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="266f1-122">Описание</span><span class="sxs-lookup"><span data-stu-id="266f1-122">Description</span></span>                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="266f1-123"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="266f1-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                            | <span data-ttu-id="266f1-124">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="266f1-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="266f1-125"><dt>**Доверенный платформенный модуль \_ E \_ аусфаил**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="266f1-125"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl> | <span data-ttu-id="266f1-126">Предоставленное значение авторизации владельца неверно.</span><span class="sxs-lookup"><span data-stu-id="266f1-126">The provided owner authorization value is incorrect.</span></span> <span data-ttu-id="266f1-127">Дополнительные попытки сброса блокировки будут завершаться с такой же ошибкой.</span><span class="sxs-lookup"><span data-stu-id="266f1-127">Additional attempts at resetting the lock will fail with this same error.</span></span> <span data-ttu-id="266f1-128">Дождитесь истечения времени ожидания или другого механизма, зависящего от производителя, перед повторной попыткой блокировки команд TPM.</span><span class="sxs-lookup"><span data-stu-id="266f1-128">Please wait until the time-out period or other manufacturer-specific mechanism has expired before retrying locked TPM commands.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="266f1-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="266f1-129">Remarks</span></span>

<span data-ttu-id="266f1-130">Этот метод вызывает команду TPM \_ ресетлокквалуе в доверенном платформенном модуле.</span><span class="sxs-lookup"><span data-stu-id="266f1-130">This method calls the TPM\_ResetLockValue command on the TPM.</span></span> <span data-ttu-id="266f1-131">Точное поведение этого метода зависит от производителей доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="266f1-131">The exact behavior of this method varies among TPM manufacturers.</span></span> <span data-ttu-id="266f1-132">Документация от изготовителя компьютера или доверенного платформенного модуля может предоставить дополнительные сведения о реализации механизма атак с помощью антисловарей.</span><span class="sxs-lookup"><span data-stu-id="266f1-132">Documentation from the computer or TPM manufacturer may provide additional information on the implementation of the anti-dictionary attack mechanism.</span></span>

<span data-ttu-id="266f1-133">Как правило, производители могут обнаруживать атаки из словарей, отслеживая неудачные проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="266f1-133">In general, manufacturers can detect dictionary attacks by keeping track of failed authentications.</span></span> <span data-ttu-id="266f1-134">Если число или частота сбоев становится достаточно высокой, TPM блокирует дальнейшие команды в течение определенного времени.</span><span class="sxs-lookup"><span data-stu-id="266f1-134">If the number or frequency of failures become high enough, the TPM will lock out further commands for a certain time.</span></span> <span data-ttu-id="266f1-135">Как правило, начальное время ожидания будет небольшим, чтобы позволить законному пользователю исправить ситуацию.</span><span class="sxs-lookup"><span data-stu-id="266f1-135">Generally, the initial time-out period will be short, to allow a legitimate user a chance to correct the situation.</span></span> <span data-ttu-id="266f1-136">Если сбои продолжаются, то продолжительность каждого последующего времени ожидания может увеличиваться быстро.</span><span class="sxs-lookup"><span data-stu-id="266f1-136">If failures continue, the duration of each subsequent time-out period may increase rapidly.</span></span>

<span data-ttu-id="266f1-137">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="266f1-137">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="266f1-138">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="266f1-138">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="266f1-139">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="266f1-139">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="266f1-140">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="266f1-140">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="266f1-141">Требования</span><span class="sxs-lookup"><span data-stu-id="266f1-141">Requirements</span></span>



| <span data-ttu-id="266f1-142">Требование</span><span class="sxs-lookup"><span data-stu-id="266f1-142">Requirement</span></span> | <span data-ttu-id="266f1-143">Значение</span><span class="sxs-lookup"><span data-stu-id="266f1-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="266f1-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="266f1-144">Minimum supported client</span></span><br/> | <span data-ttu-id="266f1-145">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="266f1-145">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="266f1-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="266f1-146">Minimum supported server</span></span><br/> | <span data-ttu-id="266f1-147">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="266f1-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="266f1-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="266f1-148">Namespace</span></span><br/>                | <span data-ttu-id="266f1-149">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="266f1-149">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="266f1-150">MOF</span><span class="sxs-lookup"><span data-stu-id="266f1-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="266f1-151"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="266f1-151"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="266f1-152">DLL</span><span class="sxs-lookup"><span data-stu-id="266f1-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="266f1-153"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="266f1-153"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="266f1-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="266f1-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="266f1-155">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="266f1-155">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
