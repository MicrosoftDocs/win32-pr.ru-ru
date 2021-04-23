---
description: Список предохранителей, используемых для защиты ключа шифрования тома.
ms.assetid: ea88f128-c835-49e3-a395-c5ba472fff4b
title: Метод Жеткэйпротекторс класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3a7d6a4110953d905b10eb4f7ef9a255af77897a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682555"
---
# <a name="getkeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="624df-103">Метод Жеткэйпротекторс \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="624df-103">GetKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="624df-104">Метод **жеткэйпротекторс** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) содержит список предохранителей, используемых для защиты ключа шифрования тома.</span><span class="sxs-lookup"><span data-stu-id="624df-104">The **GetKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class lists the protectors used to secure the volume's encryption key.</span></span> <span data-ttu-id="624df-105">Если указан тип предохранителя, то возвращаются только предохранители ключей томов указанного типа.</span><span class="sxs-lookup"><span data-stu-id="624df-105">If a protector type is provided, then only volume key protectors of the specified type are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="624df-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="624df-106">Syntax</span></span>


```mof
uint32 GetKeyProtectors(
  [in, optional] uint32 KeyProtectorType,
  [out]          string VolumeKeyProtectorID[]
);
```



## <a name="parameters"></a><span data-ttu-id="624df-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="624df-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="624df-108">*Кэйпротектортипе* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="624df-108">*KeyProtectorType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="624df-109">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="624df-109">Type: **uint32**</span></span>

<span data-ttu-id="624df-110">Целое число без знака, указывающее тип возвращаемого предохранителя ключа.</span><span class="sxs-lookup"><span data-stu-id="624df-110">An unsigned integer that specifies the type of key protector to return.</span></span>

<span data-ttu-id="624df-111">Если этот параметр не указан, возвращаются все доступные предохранители ключа тома.</span><span class="sxs-lookup"><span data-stu-id="624df-111">If this parameter is not specified, all available key protectors of the volume are returned.</span></span>



| <span data-ttu-id="624df-112">Значение</span><span class="sxs-lookup"><span data-stu-id="624df-112">Value</span></span>                                                                         | <span data-ttu-id="624df-113">Значение</span><span class="sxs-lookup"><span data-stu-id="624df-113">Meaning</span></span>                                                           |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="624df-114"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="624df-114"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="624df-115">Все типы.</span><span class="sxs-lookup"><span data-stu-id="624df-115">All types.</span></span><br/> <span data-ttu-id="624df-116">Возвращаются все предохранители ключа.</span><span class="sxs-lookup"><span data-stu-id="624df-116">All key protectors are returned.</span></span><br/> |
| <dl> <span data-ttu-id="624df-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="624df-117"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="624df-118">Доверенный платформенный модуль (TPM) (доверенный платформенный модуль).</span><span class="sxs-lookup"><span data-stu-id="624df-118">Trusted Platform Module (TPM).</span></span><br/>                         |
| <dl> <span data-ttu-id="624df-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="624df-119"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="624df-120">Внешний ключ.</span><span class="sxs-lookup"><span data-stu-id="624df-120">External key.</span></span><br/>                                          |
| <dl> <span data-ttu-id="624df-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="624df-121"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="624df-122">Числовой пароль.</span><span class="sxs-lookup"><span data-stu-id="624df-122">Numeric password.</span></span><br/>                                      |
| <dl> <span data-ttu-id="624df-123"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="624df-123"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="624df-124">TPM и ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="624df-124">TPM And PIN.</span></span><br/>                                           |
| <dl> <span data-ttu-id="624df-125"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="624df-125"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="624df-126">TPM и ключ запуска.</span><span class="sxs-lookup"><span data-stu-id="624df-126">TPM And Startup Key.</span></span><br/>                                   |
| <dl> <span data-ttu-id="624df-127"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="624df-127"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="624df-128">TPM, ПИН-код и ключ запуска.</span><span class="sxs-lookup"><span data-stu-id="624df-128">TPM And PIN And Startup Key.</span></span><br/>                           |
| <dl> <span data-ttu-id="624df-129"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="624df-129"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="624df-130">Открытый ключ.</span><span class="sxs-lookup"><span data-stu-id="624df-130">Public Key.</span></span><br/>                                            |
| <dl> <span data-ttu-id="624df-131"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="624df-131"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="624df-132">Кодов.</span><span class="sxs-lookup"><span data-stu-id="624df-132">Passphrase.</span></span><br/>                                            |
| <dl> <span data-ttu-id="624df-133"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="624df-133"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="624df-134">Сертификат TPM</span><span class="sxs-lookup"><span data-stu-id="624df-134">TPM Certificate</span></span><br/>                                        |
| <dl> <span data-ttu-id="624df-135"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="624df-135"><dt>10</dt></span></span> </dl> | <span data-ttu-id="624df-136">Идентификатор безопасности (SID)</span><span class="sxs-lookup"><span data-stu-id="624df-136">Security Identifier (SID)</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="624df-137">*Волумекэйпротекторид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="624df-137">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="624df-138">Тип: **строка \[ \]**</span><span class="sxs-lookup"><span data-stu-id="624df-138">Type: **string\[\]**</span></span>

<span data-ttu-id="624df-139">Массив строк, который определяет предохранители ключа, используемые для защиты ключа шифрования тома.</span><span class="sxs-lookup"><span data-stu-id="624df-139">An array of strings that identify the key protectors used to secure the volume's encryption key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="624df-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="624df-140">Return value</span></span>

<span data-ttu-id="624df-141">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="624df-141">Type: **uint32**</span></span>

<span data-ttu-id="624df-142">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="624df-142">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="624df-143">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="624df-143">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="624df-144">Описание</span><span class="sxs-lookup"><span data-stu-id="624df-144">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="624df-145"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="624df-145"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="624df-146">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="624df-146">The method was successful.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="624df-147"><dt>**Д \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="624df-147"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="624df-148">Параметр *волумекэйпротекторид* указан, но не ссылается на допустимый *кэйпротектортипе*.</span><span class="sxs-lookup"><span data-stu-id="624df-148">The *VolumeKeyProtectorID* parameter is specified but does not refer to a valid *KeyProtectorType*.</span></span><br/> |
| <dl> <span data-ttu-id="624df-149"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="624df-149"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="624df-150">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="624df-150">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="624df-151">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="624df-151">Add a key protector to enable BitLocker.</span></span> <br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="624df-152">Комментарии</span><span class="sxs-lookup"><span data-stu-id="624df-152">Remarks</span></span>

<span data-ttu-id="624df-153">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="624df-153">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="624df-154">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="624df-154">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="624df-155">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="624df-155">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="624df-156">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="624df-156">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="624df-157">Требования</span><span class="sxs-lookup"><span data-stu-id="624df-157">Requirements</span></span>



| <span data-ttu-id="624df-158">Требование</span><span class="sxs-lookup"><span data-stu-id="624df-158">Requirement</span></span> | <span data-ttu-id="624df-159">Значение</span><span class="sxs-lookup"><span data-stu-id="624df-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="624df-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="624df-160">Minimum supported client</span></span><br/> | <span data-ttu-id="624df-161">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="624df-161">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="624df-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="624df-162">Minimum supported server</span></span><br/> | <span data-ttu-id="624df-163">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="624df-163">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="624df-164">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="624df-164">Namespace</span></span><br/>                | <span data-ttu-id="624df-165">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="624df-165">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="624df-166">MOF</span><span class="sxs-lookup"><span data-stu-id="624df-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="624df-167"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="624df-167"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="624df-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="624df-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="624df-169">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="624df-169">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
