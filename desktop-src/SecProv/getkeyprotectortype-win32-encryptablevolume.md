---
description: Указывает тип предохранителя ключа.
ms.assetid: 17cdde18-3979-4a19-b36e-aa71994148c9
title: Метод Жеткэйпротектортипе класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorType
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 483394f2e1c80f97442a9e6758f604093d513c3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546407"
---
# <a name="getkeyprotectortype-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="cb776-103">Метод Жеткэйпротектортипе \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="cb776-103">GetKeyProtectorType method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="cb776-104">Метод **жеткэйпротектортипе** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) указывает тип предохранителя ключа.</span><span class="sxs-lookup"><span data-stu-id="cb776-104">The **GetKeyProtectorType** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates the type of a given key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb776-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb776-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorType(
  [in]  string VolumeKeyProtectorID,
  [out] uint32 KeyProtectorType
);
```



## <a name="parameters"></a><span data-ttu-id="cb776-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb776-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb776-107">*Волумекэйпротекторид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cb776-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb776-108">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="cb776-108">Type: **string**</span></span>

<span data-ttu-id="cb776-109">Уникальный строковый идентификатор, используемый для управления предохранителем ключа зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="cb776-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="cb776-110">*Кэйпротектортипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cb776-110">*KeyProtectorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb776-111">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cb776-111">Type: **uint32**</span></span>

<span data-ttu-id="cb776-112">Целое число без знака, указывающее тип предохранителя ключа.</span><span class="sxs-lookup"><span data-stu-id="cb776-112">An unsigned integer that specifies the type of the key protector.</span></span>



| <span data-ttu-id="cb776-113">Значение</span><span class="sxs-lookup"><span data-stu-id="cb776-113">Value</span></span>                                                                         | <span data-ttu-id="cb776-114">Значение</span><span class="sxs-lookup"><span data-stu-id="cb776-114">Meaning</span></span>                                              |
|-------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="cb776-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cb776-115"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="cb776-116">Неизвестный или другой тип предохранителя</span><span class="sxs-lookup"><span data-stu-id="cb776-116">Unknown or other protector type</span></span><br/>           |
| <dl> <span data-ttu-id="cb776-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="cb776-117"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="cb776-118">Доверенный платформенный модуль (TPM)</span><span class="sxs-lookup"><span data-stu-id="cb776-118">Trusted Platform Module (TPM)</span></span><br/>             |
| <dl> <span data-ttu-id="cb776-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="cb776-119"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="cb776-120">Внешний ключ</span><span class="sxs-lookup"><span data-stu-id="cb776-120">External key</span></span><br/>                              |
| <dl> <span data-ttu-id="cb776-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="cb776-121"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="cb776-122">Числовой пароль</span><span class="sxs-lookup"><span data-stu-id="cb776-122">Numerical password</span></span><br/>                        |
| <dl> <span data-ttu-id="cb776-123"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="cb776-123"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="cb776-124">TPM и ПИН-код</span><span class="sxs-lookup"><span data-stu-id="cb776-124">TPM And PIN</span></span><br/>                               |
| <dl> <span data-ttu-id="cb776-125"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="cb776-125"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="cb776-126">TPM и ключ запуска</span><span class="sxs-lookup"><span data-stu-id="cb776-126">TPM And Startup Key</span></span><br/>                       |
| <dl> <span data-ttu-id="cb776-127"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="cb776-127"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="cb776-128">TPM, ПИН-код и ключ запуска</span><span class="sxs-lookup"><span data-stu-id="cb776-128">TPM And PIN And Startup Key</span></span><br/>               |
| <dl> <span data-ttu-id="cb776-129"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="cb776-129"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="cb776-130">Открытый ключ</span><span class="sxs-lookup"><span data-stu-id="cb776-130">Public Key</span></span><br/>                                |
| <dl> <span data-ttu-id="cb776-131"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="cb776-131"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="cb776-132">Парольная фраза</span><span class="sxs-lookup"><span data-stu-id="cb776-132">Passphrase</span></span><br/>                                |
| <dl> <span data-ttu-id="cb776-133"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="cb776-133"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="cb776-134">Сертификат TPM</span><span class="sxs-lookup"><span data-stu-id="cb776-134">TPM Certificate</span></span><br/>                           |
| <dl> <span data-ttu-id="cb776-135"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="cb776-135"><dt>10</dt></span></span> </dl> | <span data-ttu-id="cb776-136">Средство защиты для следующего поколения CryptoAPI (CNG)</span><span class="sxs-lookup"><span data-stu-id="cb776-136">CryptoAPI Next Generation (CNG) Protector</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb776-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb776-137">Return value</span></span>

<span data-ttu-id="cb776-138">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cb776-138">Type: **uint32**</span></span>

<span data-ttu-id="cb776-139">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="cb776-139">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="cb776-140">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="cb776-140">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="cb776-141">Описание</span><span class="sxs-lookup"><span data-stu-id="cb776-141">Description</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cb776-142"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="cb776-142"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="cb776-143">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="cb776-143">The method was successful.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="cb776-144"><dt>**Д \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="cb776-144"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="cb776-145">Параметр *волумекэйпротекторид* не ссылается на допустимый *кэйпротектортипе*.</span><span class="sxs-lookup"><span data-stu-id="cb776-145">The *VolumeKeyProtectorID* parameter does not refer to a valid *KeyProtectorType*.</span></span><br/> |
| <dl> <span data-ttu-id="cb776-146"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="cb776-146"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="cb776-147">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="cb776-147">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="cb776-148">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="cb776-148">Add a key protector to enable BitLocker.</span></span> <br/>  |



 

## <a name="remarks"></a><span data-ttu-id="cb776-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb776-149">Remarks</span></span>

<span data-ttu-id="cb776-150">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="cb776-150">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="cb776-151">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="cb776-151">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="cb776-152">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="cb776-152">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="cb776-153">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="cb776-153">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb776-154">Требования</span><span class="sxs-lookup"><span data-stu-id="cb776-154">Requirements</span></span>



| <span data-ttu-id="cb776-155">Требование</span><span class="sxs-lookup"><span data-stu-id="cb776-155">Requirement</span></span> | <span data-ttu-id="cb776-156">Значение</span><span class="sxs-lookup"><span data-stu-id="cb776-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb776-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb776-157">Minimum supported client</span></span><br/> | <span data-ttu-id="cb776-158">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="cb776-158">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cb776-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb776-159">Minimum supported server</span></span><br/> | <span data-ttu-id="cb776-160">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cb776-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cb776-161">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cb776-161">Namespace</span></span><br/>                | <span data-ttu-id="cb776-162">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="cb776-162">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="cb776-163">MOF</span><span class="sxs-lookup"><span data-stu-id="cb776-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb776-164"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb776-164"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb776-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb776-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb776-166">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="cb776-166">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
