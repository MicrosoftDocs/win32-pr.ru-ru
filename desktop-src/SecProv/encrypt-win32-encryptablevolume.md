---
description: Начинает шифрование полностью расшифрованного тома или возобновляет шифрование частично зашифрованного тома.
ms.assetid: bba8b800-309b-4268-8278-db69827bbdf6
title: Метод Encrypt класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Encrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 463f13c250404e9a66095144166e74dbfae933ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081480"
---
# <a name="encrypt-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="b27c0-103">Метод Encrypt \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="b27c0-103">Encrypt method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="b27c0-104">Метод **Encrypt** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) начинает шифрование полностью расшифрованного тома или возобновляет шифрование частично зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="b27c0-104">The **Encrypt** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class begins encryption of a fully decrypted volume, or resumes encryption of a partially encrypted volume.</span></span> <span data-ttu-id="b27c0-105">Если шифрование приостановлено или выполняется его выполнение, этот метод ведет себя так же, как [**ресумеконверсион**](resumeconversion-win32-encryptablevolume.md).</span><span class="sxs-lookup"><span data-stu-id="b27c0-105">When encryption is paused or in-progress, this method behaves the same as [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md).</span></span> <span data-ttu-id="b27c0-106">Если расшифровка приостановлена или выполняется ее выполнение, этот метод останавливает расшифровку и начинает шифрование.</span><span class="sxs-lookup"><span data-stu-id="b27c0-106">When decryption is paused or in-progress, this method stops the decryption and begins encryption.</span></span>

> [!Note]  
> <span data-ttu-id="b27c0-107">Если диск является аппаратно зашифрованным, этот метод не шифрует данные.</span><span class="sxs-lookup"><span data-stu-id="b27c0-107">If the drive is hardware encrypted, this method does not encrypt data.</span></span> <span data-ttu-id="b27c0-108">Вместо этого он устанавливает для состояния полосы значение "снято с блокировки" из "всегда разблокировано".</span><span class="sxs-lookup"><span data-stu-id="b27c0-108">Instead, it sets the band status to "unlocked" from "always unlocked".</span></span> <span data-ttu-id="b27c0-109">Если полоса заблокирована, разблокирована или доступна только для чтения, диск считается зашифрованным.</span><span class="sxs-lookup"><span data-stu-id="b27c0-109">If the band is locked, unlocked or is read-only, the drive is considered to be encrypted.</span></span>

 

<span data-ttu-id="b27c0-110">**Windows Vista:** Шифрование тома, отличного от текущего тома операционной системы, не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b27c0-110">**Windows Vista:** Encryption of a volume other than the currently running operating system volume is not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="b27c0-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b27c0-111">Syntax</span></span>


```mof
uint32 Encrypt(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b27c0-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b27c0-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b27c0-113">*Енкриптионмесод* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b27c0-113">*EncryptionMethod* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b27c0-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b27c0-114">Type: **uint32**</span></span>

<span data-ttu-id="b27c0-115">Целое число без знака, указывающее алгоритм шифрования и размер ключа, используемые для шифрования тома.</span><span class="sxs-lookup"><span data-stu-id="b27c0-115">An unsigned integer that specifies the encryption algorithm and key size used to encrypt the volume.</span></span> <span data-ttu-id="b27c0-116">Если этот параметр больше нуля, а том частично или полностью зашифрован, *енкриптионмесод* должен соответствовать существующему методу шифрования тома.</span><span class="sxs-lookup"><span data-stu-id="b27c0-116">If this parameter is greater than zero and the volume is partially or fully encrypted, *EncryptionMethod* must match the volume's existing encryption method.</span></span> <span data-ttu-id="b27c0-117">Если этот параметр больше нуля, а соответствующий параметр групповая политика включен с допустимым значением, *енкриптионмесод* должен соответствовать параметру групповая политика.</span><span class="sxs-lookup"><span data-stu-id="b27c0-117">If this parameter is greater than zero and the corresponding Group Policy setting is enabled with a valid value, *EncryptionMethod* must match the Group Policy setting.</span></span>

<span data-ttu-id="b27c0-118">Список возможных значений Енкриптионмесод см. в описании метода [**жетенкриптионмесод**](getencryptionmethod-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="b27c0-118">For a list of possible EncryptionMethod values, see the [**GetEncryptionMethod**](getencryptionmethod-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="b27c0-119">Значение по умолчанию для Windows 7 или ниже: 1 (AES \_ 128 \_ с \_ диффузором).</span><span class="sxs-lookup"><span data-stu-id="b27c0-119">Default value for Windows 7 or below is: 1 (AES\_128\_WITH\_DIFFUSER).</span></span>

<span data-ttu-id="b27c0-120">Значение по умолчанию для Windows 8, Windows 8.1 или Windows 10, версия 1507:3 (AES \_ 128).</span><span class="sxs-lookup"><span data-stu-id="b27c0-120">Default value for Windows 8, Windows 8.1 or Windows 10, version 1507 is: 3 (AES\_128).</span></span>

<span data-ttu-id="b27c0-121">Значение по умолчанию для Windows 10, 1511 или более поздней версии: 6 (XTS \_ AES \_ 128).</span><span class="sxs-lookup"><span data-stu-id="b27c0-121">Default value for Windows 10, version 1511 or above is: 6 (XTS\_AES\_128).</span></span>

</dd> <dt>

<span data-ttu-id="b27c0-122">*Енкриптионфлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b27c0-122">*EncryptionFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b27c0-123">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b27c0-123">Type: **uint32**</span></span>

<span data-ttu-id="b27c0-124">Флаги, описывающие поведение шифрования.</span><span class="sxs-lookup"><span data-stu-id="b27c0-124">Flags that describe the encryption behavior.</span></span>

<span data-ttu-id="b27c0-125">**Windows 7, Windows server 2008 R2, Windows Vista Enterprise и Windows server 2008:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="b27c0-125">**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise and Windows Server 2008:** This parameter is not available.</span></span>

<span data-ttu-id="b27c0-126">Сочетание 32 бит, в котором в настоящее время определены следующие биты.</span><span class="sxs-lookup"><span data-stu-id="b27c0-126">A combination of 32 bits with following bits currently defined.</span></span>



| <span data-ttu-id="b27c0-127">Значение</span><span class="sxs-lookup"><span data-stu-id="b27c0-127">Value</span></span>                                                                                  | <span data-ttu-id="b27c0-128">Значение</span><span class="sxs-lookup"><span data-stu-id="b27c0-128">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b27c0-129"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="b27c0-129"><dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="b27c0-130">При запуске нового процесса шифрования Шифрование томов выполняется в режиме шифрования только для данных.</span><span class="sxs-lookup"><span data-stu-id="b27c0-130">Perform volume encryption in data-only encryption mode when starting new encryption process.</span></span> <span data-ttu-id="b27c0-131">Если шифрование приостановлено или остановлено, вызов метода **Encrypt** эффективно возобновляет преобразование, а значение этого бита игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b27c0-131">If encryption has been paused or stopped, calling the **Encrypt** method effectively resumes conversion and the value of this bit is ignored.</span></span> <span data-ttu-id="b27c0-132">Этот бит действует только в том случае, если методы **Encrypt** или [**енкриптафтерхардваретест**](encryptafterhardwaretest-win32-encryptablevolume.md) запускают шифрование из полностью расшифрованного состояния, выполняется расшифровка или приостановленное состояние расшифровки.</span><span class="sxs-lookup"><span data-stu-id="b27c0-132">This bit only has effect when either the **Encrypt** or [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) methods start encryption from the fully decrypted state, decryption in progress state, or decryption paused state.</span></span> <span data-ttu-id="b27c0-133">Если этот бит равен нулю, то есть он не задан, при запуске нового процесса шифрования будет выполнено преобразование в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="b27c0-133">If this bit is zero, meaning that it is not set, when starting new encryption process, then full mode conversion will be performed.</span></span><br/> |
| <dl> <span data-ttu-id="b27c0-134"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="b27c0-134"><dt>0x00000002</dt></span></span> </dl>  | <span data-ttu-id="b27c0-135">Выполните очистку свободного места тома по требованию.</span><span class="sxs-lookup"><span data-stu-id="b27c0-135">Perform on-demand wipe of the volume free space.</span></span> <span data-ttu-id="b27c0-136">Вызов метода **Encrypt** с этим набором битов разрешен только в том случае, если в настоящее время не выполняется преобразование или очистка тома и он находится в зашифрованном состоянии.</span><span class="sxs-lookup"><span data-stu-id="b27c0-136">Calling the **Encrypt** method with this bit set is only allowed when volume is not currently converting or wiping and is in an "encrypted" state.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="b27c0-137"><dt>0x00010000 </dt></span><span class="sxs-lookup"><span data-stu-id="b27c0-137"><dt>0x00010000 </dt></span></span> </dl> | <span data-ttu-id="b27c0-138">Выполнение запрошенной операции в синхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="b27c0-138">Perform the requested operation synchronously.</span></span> <span data-ttu-id="b27c0-139">Вызов блокируется до тех пор, пока запрошенная операция не будет завершена или была прервана.</span><span class="sxs-lookup"><span data-stu-id="b27c0-139">The call will block until requested operation has completed or was interrupted.</span></span> <span data-ttu-id="b27c0-140">Этот флаг поддерживается только при использовании метода **Encrypt** .</span><span class="sxs-lookup"><span data-stu-id="b27c0-140">This flag is only supported with the **Encrypt** method.</span></span> <span data-ttu-id="b27c0-141">Этот флаг можно указать при вызове **шифрования** для возобновления остановки или прекращения шифрования или очистки, а также при выполнении шифрования или очистки.</span><span class="sxs-lookup"><span data-stu-id="b27c0-141">This flag can be specified when **Encrypt** is called to resume stopped or interrupted encryption or wiping or when either encryption or wiping is in progress.</span></span> <span data-ttu-id="b27c0-142">Это позволяет вызывающему объекту возобновить синхронное ожидание до завершения или прерывания процесса.</span><span class="sxs-lookup"><span data-stu-id="b27c0-142">This allows the caller to resume synchronously waiting until the process is completed or interrupted.</span></span><br/>                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b27c0-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b27c0-143">Return value</span></span>

<span data-ttu-id="b27c0-144">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b27c0-144">Type: **uint32**</span></span>

<span data-ttu-id="b27c0-145">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="b27c0-145">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="b27c0-146">Этот метод немедленно возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b27c0-146">This method returns immediately.</span></span> <span data-ttu-id="b27c0-147">Если том уже полностью зашифрован и другие ошибки не возвращаются, этот метод возвращает значение 0.</span><span class="sxs-lookup"><span data-stu-id="b27c0-147">If the volume is already fully encrypted and no other errors are returned, this method returns 0.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b27c0-148">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="b27c0-148">Return code/value</span></span></th>
<th><span data-ttu-id="b27c0-149">Описание</span><span class="sxs-lookup"><span data-stu-id="b27c0-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="b27c0-150"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span><span class="sxs-lookup"><span data-stu-id="b27c0-150"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span></span></dl></td>
<td><span data-ttu-id="b27c0-151">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="b27c0-151">The method was successful.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b27c0-152"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span><span class="sxs-lookup"><span data-stu-id="b27c0-152"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span></span></dl></td>
<td><span data-ttu-id="b27c0-153">Параметр <em>енкриптионмесод</em> предоставляется, но не находится в известном диапазоне или не соответствует текущему параметру групповая политика.</span><span class="sxs-lookup"><span data-stu-id="b27c0-153">The <em>EncryptionMethod</em> parameter is provided but is not within the known range or does not match the current Group Policy setting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="b27c0-154"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span><span class="sxs-lookup"><span data-stu-id="b27c0-154"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span></span></dl></td>
<td><span data-ttu-id="b27c0-155">Для тома не существует ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="b27c0-155">No encryption key exists for the volume.</span></span> <span data-ttu-id="b27c0-156">Отключите предохранители ключа с помощью метода <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>дисаблекэйпротекторс</strong></a> или используйте один из следующих методов, чтобы указать предохранители ключа для тома:</span><span class="sxs-lookup"><span data-stu-id="b27c0-156">Either disable key protectors by using the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method or use one of the following methods to specify key protectors for the volume:</span></span><br/>
<ul>
<li><span data-ttu-id="b27c0-157"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>протекткэйвисекстерналкэй</strong></a></span><span class="sxs-lookup"><span data-stu-id="b27c0-157"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="b27c0-158"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>протекткэйвиснумерикалпассворд</strong></a></span><span class="sxs-lookup"><span data-stu-id="b27c0-158"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="b27c0-159"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>протекткэйвистпм</strong></a></span><span class="sxs-lookup"><span data-stu-id="b27c0-159"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="b27c0-160"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>протекткэйвистпмандпин</strong></a></span><span class="sxs-lookup"><span data-stu-id="b27c0-160"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="b27c0-161"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>протекткэйвистпмандпинандстартупкэй</strong></a></span><span class="sxs-lookup"><span data-stu-id="b27c0-161"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="b27c0-162"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>протекткэйвистпмандстартупкэй</strong></a></span><span class="sxs-lookup"><span data-stu-id="b27c0-162"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul><span data-ttu-id="b27c0-163">
<strong>Windows Vista:</strong> Если для тома не существует ключа шифрования, вместо него возвращается ERROR_INVALID_OPERATION.</span><span class="sxs-lookup"><span data-stu-id="b27c0-163">
<strong>Windows Vista:</strong> When no encryption key exists for the volume, ERROR_INVALID_OPERATION is returned instead.</span></span> <span data-ttu-id="b27c0-164">Десятичное значение — 4317, а шестнадцатеричное значение — 0x10DD.</span><span class="sxs-lookup"><span data-stu-id="b27c0-164">The decimal value is 4317 and the hexadecimal value is 0x10DD.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b27c0-165"><dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt> <dt>2150694957 (0x8031002D)</dt> </span><span class="sxs-lookup"><span data-stu-id="b27c0-165"><dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt> <dt>2150694957 (0x8031002D)</dt> </span></span></dl></td>
<td><span data-ttu-id="b27c0-166">Предоставленный метод шифрования не соответствует ни частичному, ни полностью зашифрованному тому.</span><span class="sxs-lookup"><span data-stu-id="b27c0-166">The provided encryption method does not match that of the partially or fully encrypted volume.</span></span> <span data-ttu-id="b27c0-167">Чтобы продолжить шифрование, оставьте параметр <em>енкриптионмесод</em> пустым или используйте нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="b27c0-167">To continue encryption, leave the <em>EncryptionMethod</em> parameter blank or use a value of zero.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="b27c0-168"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span><span class="sxs-lookup"><span data-stu-id="b27c0-168"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span></span></dl></td>
<td><span data-ttu-id="b27c0-169">Невозможно зашифровать том, так как этот компьютер настроен как часть кластера серверов.</span><span class="sxs-lookup"><span data-stu-id="b27c0-169">The volume cannot be encrypted because this computer is configured to be part of a server cluster.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b27c0-170"><dt><strong>FVE_E_LOCKED_VOLUME</strong></dt> <dt>2150694912 (0x80310000)</dt> </span><span class="sxs-lookup"><span data-stu-id="b27c0-170"><dt><strong>FVE_E_LOCKED_VOLUME</strong></dt> <dt>2150694912 (0x80310000)</dt> </span></span></dl></td>
<td><span data-ttu-id="b27c0-171">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="b27c0-171">The volume is locked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="b27c0-172"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span><span class="sxs-lookup"><span data-stu-id="b27c0-172"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span></span></dl></td>
<td><span data-ttu-id="b27c0-173">Предохранители ключа для типа " &quot; числовой пароль" не &quot; указаны.</span><span class="sxs-lookup"><span data-stu-id="b27c0-173">No key protectors of the type &quot;Numerical Password&quot; are specified.</span></span> <span data-ttu-id="b27c0-174">Групповая политика требуется резервное копирование сведений о восстановлении в службы домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b27c0-174">The Group Policy requires a backup of recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="b27c0-175">Чтобы добавить хотя бы один предохранитель ключа этого типа, используйте метод <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>протекткэйвиснумерикалпассворд</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b27c0-175">To add at least one key protector of that type, use the <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> method.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="b27c0-176">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b27c0-176">Remarks</span></span>

<span data-ttu-id="b27c0-177">При использовании этого метода без второго параметра (в соответствии с определением Windows 7 и Windows Vista Enterprise) метод всегда начнет преобразование в полном режиме, чтобы обеспечить обратную совместимость.</span><span class="sxs-lookup"><span data-stu-id="b27c0-177">When you use this method without the second optional parameter (according to the Windows 7 and Windows Vista Enterprise definition), the method will always initiate full mode conversion in order to keep backward compatible behavior.</span></span> <span data-ttu-id="b27c0-178">Таким образом, безопасность существующих приложений и сценариев не будет нарушена с добавлением второго необязательного параметра в Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="b27c0-178">This way the security expectation of existing applications and scripts will not be broken with the addition of the second optional parameter in Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="b27c0-179">Можно вызвать [**жетконверсионстатус**](getconversionstatus-win32-encryptablevolume.md) , чтобы определить, выполняется ли шифрование, а также процент зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="b27c0-179">You can call [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to determine whether encryption is in progress and the percentage of the volume that has been encrypted.</span></span>

<span data-ttu-id="b27c0-180">После полного шифрования тома и добавления и включения предохранителей ключа состояние защиты тома изменится на "вкл.".</span><span class="sxs-lookup"><span data-stu-id="b27c0-180">After the volume is fully encrypted and if key protectors have been added and enabled, the protection status for the volume changes to "on".</span></span>

<span data-ttu-id="b27c0-181">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="b27c0-181">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b27c0-182">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b27c0-182">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="b27c0-183">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="b27c0-183">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b27c0-184">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="b27c0-184">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b27c0-185">Требования</span><span class="sxs-lookup"><span data-stu-id="b27c0-185">Requirements</span></span>



| <span data-ttu-id="b27c0-186">Требование</span><span class="sxs-lookup"><span data-stu-id="b27c0-186">Requirement</span></span> | <span data-ttu-id="b27c0-187">Значение</span><span class="sxs-lookup"><span data-stu-id="b27c0-187">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b27c0-188">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b27c0-188">Minimum supported client</span></span><br/> | <span data-ttu-id="b27c0-189">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="b27c0-189">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b27c0-190">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b27c0-190">Minimum supported server</span></span><br/> | <span data-ttu-id="b27c0-191">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b27c0-191">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b27c0-192">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b27c0-192">Namespace</span></span><br/>                | <span data-ttu-id="b27c0-193">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="b27c0-193">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="b27c0-194">MOF</span><span class="sxs-lookup"><span data-stu-id="b27c0-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b27c0-195"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b27c0-195"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b27c0-196">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b27c0-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b27c0-197">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="b27c0-197">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
