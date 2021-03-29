---
description: Начинает шифрование полностью расшифрованного тома операционной системы после проверки оборудования.
ms.assetid: 216c96bb-7737-4421-8b16-1ce295342266
title: Метод Енкриптафтерхардваретест класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EncryptAfterHardwareTest
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f356b9adda5e1b25fdd3d9fc39ace5cf8028da32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540943"
---
# <a name="encryptafterhardwaretest-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="bba6c-103">Метод Енкриптафтерхардваретест \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="bba6c-103">EncryptAfterHardwareTest method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="bba6c-104">Метод **енкриптафтерхардваретест** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) начинает шифрование полностью расшифрованного тома операционной системы после проверки оборудования.</span><span class="sxs-lookup"><span data-stu-id="bba6c-104">The **EncryptAfterHardwareTest** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class begins encryption of a fully decrypted operating system volume after a hardware test.</span></span> <span data-ttu-id="bba6c-105">Для выполнения этой проверки оборудования требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="bba6c-105">A reboot is required to perform this hardware test.</span></span> <span data-ttu-id="bba6c-106">Используйте этот метод вместо метода [**Encrypt**](encrypt-win32-encryptablevolume.md) , чтобы убедиться, что BitLocker будет работать должным образом.</span><span class="sxs-lookup"><span data-stu-id="bba6c-106">Use this method instead of the [**Encrypt**](encrypt-win32-encryptablevolume.md) method to check that BitLocker will work as expected.</span></span>

> [!Note]  
> <span data-ttu-id="bba6c-107">Если жесткий диск является аппаратно зашифрованным, этот метод не шифрует данные.</span><span class="sxs-lookup"><span data-stu-id="bba6c-107">If the hard drive is hardware encrypted, this method does not encrypt data.</span></span> <span data-ttu-id="bba6c-108">Вместо этого он устанавливает состояние полосы снято с «бессрочно разблокирована».</span><span class="sxs-lookup"><span data-stu-id="bba6c-108">Instead, it sets the band status to unlocked from "perpetually unlocked".</span></span> <span data-ttu-id="bba6c-109">Если полоса заблокирована, разблокирована или доступна только для чтения, диск считается зашифрованным.</span><span class="sxs-lookup"><span data-stu-id="bba6c-109">If the band is locked, unlocked or is read-only, the drive is considered to be encrypted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="bba6c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bba6c-110">Syntax</span></span>


```mof
uint32 EncryptAfterHardwareTest(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a><span data-ttu-id="bba6c-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="bba6c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bba6c-112">*Енкриптионмесод* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="bba6c-112">*EncryptionMethod* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bba6c-113">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bba6c-113">Type: **uint32**</span></span>

<span data-ttu-id="bba6c-114">Задает алгоритм шифрования и размер ключа, используемые для шифрования тома.</span><span class="sxs-lookup"><span data-stu-id="bba6c-114">Specifies the encryption algorithm and key size used to encrypt the volume.</span></span> <span data-ttu-id="bba6c-115">Оставьте этот параметр пустым, чтобы использовать нулевое значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bba6c-115">Leave this parameter blank to use the default value of zero.</span></span> <span data-ttu-id="bba6c-116">Если том частично или полностью зашифрован, значение этого параметра должно быть равно 0 или совпадать с существующим методом шифрования тома.</span><span class="sxs-lookup"><span data-stu-id="bba6c-116">If the volume is partially or fully encrypted, the value of this parameter must be 0 or match the volume's existing encryption method.</span></span> <span data-ttu-id="bba6c-117">Если соответствующий параметр групповая политика включен с допустимым значением, значение этого параметра должно быть равно 0 или соответствовать параметру групповая политика.</span><span class="sxs-lookup"><span data-stu-id="bba6c-117">If the corresponding Group Policy setting has been enabled with a valid value, the value of this parameter must be 0 or match the Group Policy setting.</span></span>

<span data-ttu-id="bba6c-118">Если соответствующий параметр групповая политика является недопустимым, используется по умолчанию AES 128 с диффузором.</span><span class="sxs-lookup"><span data-stu-id="bba6c-118">If the corresponding Group Policy setting is invalid, the default of AES 128 with diffuser is used.</span></span>



| <span data-ttu-id="bba6c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bba6c-119">Value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="bba6c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="bba6c-120">Meaning</span></span>                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <span data-ttu-id="bba6c-121">Не <dt>**указано**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bba6c-121"><dt>**Unspecified**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="bba6c-122">Используйте текущий параметр групповая политика, если он доступен и является допустимым, или метод шифрования по умолчанию в противном случае.</span><span class="sxs-lookup"><span data-stu-id="bba6c-122">Use the current Group Policy setting, if available and valid, or the default encryption method otherwise.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="bba6c-123"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="bba6c-123"><dt>1</dt></span></span> </dl>                                                                                                                                                                | <span data-ttu-id="bba6c-124">AES 128 С ДИФФУЗОРОМ</span><span class="sxs-lookup"><span data-stu-id="bba6c-124">AES 128 WITH DIFFUSER</span></span><br/> <span data-ttu-id="bba6c-125">Зашифруйте том с помощью алгоритма AES (AES), улучшенного с помощью слоя диффузора и размера ключа AES размером 128 бит.</span><span class="sxs-lookup"><span data-stu-id="bba6c-125">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer and by using an AES key size of 128 bits.</span></span><br/> |
| <dl> <span data-ttu-id="bba6c-126"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="bba6c-126"><dt>2</dt></span></span> </dl>                                                                                                                                                                | <span data-ttu-id="bba6c-127">AES 256 С ДИФФУЗОРОМ</span><span class="sxs-lookup"><span data-stu-id="bba6c-127">AES 256 WITH DIFFUSER</span></span><br/> <span data-ttu-id="bba6c-128">Зашифруйте том с помощью алгоритма AES (AES), улучшенного с помощью слоя диффузора и размера ключа AES размером 256 бит.</span><span class="sxs-lookup"><span data-stu-id="bba6c-128">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer and by using an AES key size of 256 bits.</span></span><br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <span data-ttu-id="bba6c-129"><dt>**AES \_ 128**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="bba6c-129"><dt>**AES\_128**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="bba6c-130">Зашифруйте том с помощью алгоритма AES (AES) и с помощью ключа AES размером 128 бит.</span><span class="sxs-lookup"><span data-stu-id="bba6c-130">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm and by using an AES key size of 128 bits.</span></span><br/>                                                                 |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <span data-ttu-id="bba6c-131"><dt>**AES \_ 256**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="bba6c-131"><dt>**AES\_256**</dt> <dt>4</dt></span></span> </dl>                                          | <span data-ttu-id="bba6c-132">Зашифруйте том с помощью алгоритма AES (AES) и с помощью ключа AES размером 256 бит.</span><span class="sxs-lookup"><span data-stu-id="bba6c-132">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm and by using an AES key size of 256 bits.</span></span><br/>                                                                 |



 

</dd> <dt>

<span data-ttu-id="bba6c-133">*Енкриптионфлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="bba6c-133">*EncryptionFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bba6c-134">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bba6c-134">Type: **uint32**</span></span>

<span data-ttu-id="bba6c-135">Флаги, описывающие поведение шифрования.</span><span class="sxs-lookup"><span data-stu-id="bba6c-135">Flags that describe the encryption behavior.</span></span>

<span data-ttu-id="bba6c-136">**Windows 7, Windows server 2008 R2, Windows Vista Enterprise и Windows server 2008:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="bba6c-136">**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise and Windows Server 2008:** This parameter is not available.</span></span>

<span data-ttu-id="bba6c-137">Сочетание 32 бит, в котором в настоящее время определены следующие биты.</span><span class="sxs-lookup"><span data-stu-id="bba6c-137">A combination of 32 bits with the following bits currently defined.</span></span>



| <span data-ttu-id="bba6c-138">Значение</span><span class="sxs-lookup"><span data-stu-id="bba6c-138">Value</span></span>                                                                                  | <span data-ttu-id="bba6c-139">Значение</span><span class="sxs-lookup"><span data-stu-id="bba6c-139">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bba6c-140"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="bba6c-140"><dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="bba6c-141">При запуске нового процесса шифрования Шифрование томов выполняется в режиме шифрования только для данных.</span><span class="sxs-lookup"><span data-stu-id="bba6c-141">Perform volume encryption in data-only encryption mode when starting new encryption process.</span></span> <span data-ttu-id="bba6c-142">Если шифрование приостановлено или остановлено, вызов метода [**Encrypt**](encrypt-win32-encryptablevolume.md) эффективно возобновляет преобразование, а значение этого бита игнорируется.</span><span class="sxs-lookup"><span data-stu-id="bba6c-142">If encryption has been paused or stopped, calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method effectively resumes conversion and the value of this bit is ignored.</span></span> <span data-ttu-id="bba6c-143">Этот бит действует только в том случае, если методы **Encrypt** или **енкриптафтерхардваретест** запускают шифрование из полностью расшифрованного состояния, выполняется расшифровка или приостановленное состояние расшифровки.</span><span class="sxs-lookup"><span data-stu-id="bba6c-143">This bit only has effect when either the **Encrypt** or **EncryptAfterHardwareTest** methods start encryption from the fully decrypted state, decryption in progress state, or decryption paused state.</span></span> <span data-ttu-id="bba6c-144">Если этот бит равен нулю, то есть он не задан, при запуске нового процесса шифрования будет выполнено преобразование в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="bba6c-144">If this bit is zero, meaning that it is not set, when starting new encryption process, then full mode conversion will be performed.</span></span><br/> |
| <dl> <span data-ttu-id="bba6c-145"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="bba6c-145"><dt>0x00000002</dt></span></span> </dl>  | <span data-ttu-id="bba6c-146">Выполните очистку свободного места тома по требованию.</span><span class="sxs-lookup"><span data-stu-id="bba6c-146">Perform on-demand wipe of the volume free space.</span></span> <span data-ttu-id="bba6c-147">Вызов метода [**Encrypt**](encrypt-win32-encryptablevolume.md) с этим набором битов разрешен только в том случае, если в настоящее время не выполняется преобразование или очистка тома и он находится в зашифрованном состоянии.</span><span class="sxs-lookup"><span data-stu-id="bba6c-147">Calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method with this bit set is only allowed when volume is not currently converting or wiping and is in an "encrypted" state.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="bba6c-148"><dt>0x00010000 </dt></span><span class="sxs-lookup"><span data-stu-id="bba6c-148"><dt>0x00010000 </dt></span></span> </dl> | <span data-ttu-id="bba6c-149">Выполнение запрошенной операции в синхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="bba6c-149">Perform the requested operation synchronously.</span></span> <span data-ttu-id="bba6c-150">Вызов блокируется до тех пор, пока запрошенная операция не будет завершена или была прервана.</span><span class="sxs-lookup"><span data-stu-id="bba6c-150">The call will block until requested operation has completed or was interrupted.</span></span> <span data-ttu-id="bba6c-151">Этот флаг поддерживается только при использовании метода [**Encrypt**](encrypt-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="bba6c-151">This flag is only supported with the [**Encrypt**](encrypt-win32-encryptablevolume.md) method.</span></span> <span data-ttu-id="bba6c-152">Этот флаг можно указать при вызове **шифрования** для возобновления остановки или прекращения шифрования или очистки, а также при выполнении шифрования или очистки.</span><span class="sxs-lookup"><span data-stu-id="bba6c-152">This flag can be specified when **Encrypt** is called to resume stopped or interrupted encryption or wiping or when either encryption or wiping is in progress.</span></span> <span data-ttu-id="bba6c-153">Это позволяет вызывающему объекту возобновить синхронное ожидание до завершения или прерывания процесса.</span><span class="sxs-lookup"><span data-stu-id="bba6c-153">This allows the caller to resume synchronously waiting until the process is completed or interrupted.</span></span><br/>                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bba6c-154">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bba6c-154">Return value</span></span>

<span data-ttu-id="bba6c-155">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bba6c-155">Type: **uint32**</span></span>

<span data-ttu-id="bba6c-156">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="bba6c-156">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="bba6c-157">Этот метод немедленно возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bba6c-157">This method returns immediately.</span></span> <span data-ttu-id="bba6c-158">Если том уже полностью зашифрован и другие ошибки не возвращаются, этот метод возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="bba6c-158">If the volume is already fully encrypted and no other errors are returned, this method returns zero.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bba6c-159">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="bba6c-159">Return code/value</span></span></th>
<th><span data-ttu-id="bba6c-160">Описание</span><span class="sxs-lookup"><span data-stu-id="bba6c-160">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="bba6c-161"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span><span class="sxs-lookup"><span data-stu-id="bba6c-161"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span></span></dl></td>
<td><span data-ttu-id="bba6c-162">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="bba6c-162">The method was successful.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="bba6c-163"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span><span class="sxs-lookup"><span data-stu-id="bba6c-163"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span></span></dl></td>
<td><span data-ttu-id="bba6c-164">Параметр <em>енкриптионмесод</em> предоставляется, но не находится в известном диапазоне или не соответствует текущему параметру групповая политика.</span><span class="sxs-lookup"><span data-stu-id="bba6c-164">The <em>EncryptionMethod</em> parameter is provided but is not within the known range or does not match the current Group Policy setting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="bba6c-165"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span><span class="sxs-lookup"><span data-stu-id="bba6c-165"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span></span></dl></td>
<td><span data-ttu-id="bba6c-166">Для тома не существует ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="bba6c-166">No encryption key exists for the volume.</span></span><br/> <span data-ttu-id="bba6c-167">Отключите предохранители ключа с помощью метода <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>дисаблекэйпротекторс</strong></a> или используйте один из следующих методов, чтобы указать предохранители ключа для тома:</span><span class="sxs-lookup"><span data-stu-id="bba6c-167">Either disable key protectors by using the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method, or use one of the following methods to specify key protectors for the volume:</span></span>
<ul>
<li><span data-ttu-id="bba6c-168"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>протекткэйвисекстерналкэй</strong></a></span><span class="sxs-lookup"><span data-stu-id="bba6c-168"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="bba6c-169"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>протекткэйвиснумерикалпассворд</strong></a></span><span class="sxs-lookup"><span data-stu-id="bba6c-169"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="bba6c-170"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>протекткэйвистпм</strong></a></span><span class="sxs-lookup"><span data-stu-id="bba6c-170"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="bba6c-171"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>протекткэйвистпмандпин</strong></a></span><span class="sxs-lookup"><span data-stu-id="bba6c-171"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="bba6c-172"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>протекткэйвистпмандпинандстартупкэй</strong></a></span><span class="sxs-lookup"><span data-stu-id="bba6c-172"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="bba6c-173"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>протекткэйвистпмандстартупкэй</strong></a></span><span class="sxs-lookup"><span data-stu-id="bba6c-173"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="bba6c-174"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span><span class="sxs-lookup"><span data-stu-id="bba6c-174"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span></span></dl></td>
<td><span data-ttu-id="bba6c-175">Невозможно зашифровать том, так как этот компьютер настроен как часть кластера серверов.</span><span class="sxs-lookup"><span data-stu-id="bba6c-175">The volume cannot be encrypted because this computer is configured to be part of a server cluster.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="bba6c-176"><dt><strong>FVE_E_NO_PROTECTORS_TO_TEST</strong></dt> <dt>2150694971 (0x8031003B)</dt> </span><span class="sxs-lookup"><span data-stu-id="bba6c-176"><dt><strong>FVE_E_NO_PROTECTORS_TO_TEST</strong></dt> <dt>2150694971 (0x8031003B)</dt> </span></span></dl></td>
<td><span data-ttu-id="bba6c-177">Не удается найти предохранители ключа &quot; доверенного платформенного модуля &quot; , &quot; TPM и ПИН-кода &quot; , &quot; TPM, ПИН-код и ключ запуска &quot; , &quot; TPM и ключ запуска, а &quot; также &quot; внешний ключ &quot; .</span><span class="sxs-lookup"><span data-stu-id="bba6c-177">No key protectors of the type &quot;TPM&quot;, &quot;TPM And PIN&quot;, &quot;TPM And PIN And Startup Key&quot;, &quot;TPM And Startup Key&quot;, or &quot;External Key&quot; can be found.</span></span> <span data-ttu-id="bba6c-178">Проверка оборудования включает только предыдущие предохранители ключа.</span><span class="sxs-lookup"><span data-stu-id="bba6c-178">The hardware test only involves the previous key protectors.</span></span><br/> <span data-ttu-id="bba6c-179">Если вы по-прежнему хотите выполнить тест оборудования, необходимо использовать один из следующих методов для указания предохранителей ключа для тома:</span><span class="sxs-lookup"><span data-stu-id="bba6c-179">If you still want to run a hardware test, you must use one of the following methods to specify key protectors for the volume:</span></span>
<ul>
<li><span data-ttu-id="bba6c-180"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>протекткэйвисекстерналкэй</strong></a></span><span class="sxs-lookup"><span data-stu-id="bba6c-180"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="bba6c-181"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>протекткэйвиснумерикалпассворд</strong></a></span><span class="sxs-lookup"><span data-stu-id="bba6c-181"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="bba6c-182"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>протекткэйвистпм</strong></a></span><span class="sxs-lookup"><span data-stu-id="bba6c-182"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="bba6c-183"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>протекткэйвистпмандпин</strong></a></span><span class="sxs-lookup"><span data-stu-id="bba6c-183"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="bba6c-184"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>протекткэйвистпмандпинандстартупкэй</strong></a></span><span class="sxs-lookup"><span data-stu-id="bba6c-184"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="bba6c-185"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>протекткэйвистпмандстартупкэй</strong></a></span><span class="sxs-lookup"><span data-stu-id="bba6c-185"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="bba6c-186"><dt><strong>FVE_E_NOT_DECRYPTED</strong></dt> <dt>2150694969 (0x80310039)</dt> </span><span class="sxs-lookup"><span data-stu-id="bba6c-186"><dt><strong>FVE_E_NOT_DECRYPTED</strong></dt> <dt>2150694969 (0x80310039)</dt> </span></span></dl></td>
<td><span data-ttu-id="bba6c-187">Том частично или полностью зашифрован.</span><span class="sxs-lookup"><span data-stu-id="bba6c-187">The volume is partially or fully encrypted.</span></span><br/> <span data-ttu-id="bba6c-188">Проверка оборудования применяется перед шифрованием.</span><span class="sxs-lookup"><span data-stu-id="bba6c-188">The hardware test applies before encryption occurs.</span></span> <span data-ttu-id="bba6c-189">Если вы по-прежнему хотите выполнить тест, сначала используйте метод <a href="decrypt-win32-encryptablevolume.md"><strong>дешифровки</strong></a> , а затем используйте один из следующих методов для добавления предохранителей ключа:</span><span class="sxs-lookup"><span data-stu-id="bba6c-189">If you still want to run the test, first use the <a href="decrypt-win32-encryptablevolume.md"><strong>Decrypt</strong></a> method and then use one of the following methods to add key protectors:</span></span>
<ul>
<li><span data-ttu-id="bba6c-190"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>протекткэйвисекстерналкэй</strong></a></span><span class="sxs-lookup"><span data-stu-id="bba6c-190"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="bba6c-191"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>протекткэйвиснумерикалпассворд</strong></a></span><span class="sxs-lookup"><span data-stu-id="bba6c-191"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="bba6c-192"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>протекткэйвистпм</strong></a></span><span class="sxs-lookup"><span data-stu-id="bba6c-192"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="bba6c-193"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>протекткэйвистпмандпин</strong></a></span><span class="sxs-lookup"><span data-stu-id="bba6c-193"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="bba6c-194"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>протекткэйвистпмандстартупкэй</strong></a></span><span class="sxs-lookup"><span data-stu-id="bba6c-194"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="bba6c-195"><dt><strong>FVE_E_NOT_OS_VOLUME</strong></dt> <dt>2150694952 (0x80310028)</dt> </span><span class="sxs-lookup"><span data-stu-id="bba6c-195"><dt><strong>FVE_E_NOT_OS_VOLUME</strong></dt> <dt>2150694952 (0x80310028)</dt> </span></span></dl></td>
<td><span data-ttu-id="bba6c-196">Том является томом данных.</span><span class="sxs-lookup"><span data-stu-id="bba6c-196">The volume is a data volume.</span></span><br/> <span data-ttu-id="bba6c-197">Проверка оборудования применяется только к томам, которые могут запускать операционную систему.</span><span class="sxs-lookup"><span data-stu-id="bba6c-197">The hardware test applies only to volumes that can start the operating system.</span></span> <span data-ttu-id="bba6c-198">Запустите этот метод на том же томе операционной системы, в котором запущен.</span><span class="sxs-lookup"><span data-stu-id="bba6c-198">Run this method on the currently started operating system volume.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="bba6c-199"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span><span class="sxs-lookup"><span data-stu-id="bba6c-199"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span></span></dl></td>
<td><span data-ttu-id="bba6c-200">Предохранители ключа для типа " &quot; числовой пароль" не &quot; указаны.</span><span class="sxs-lookup"><span data-stu-id="bba6c-200">No key protectors of the type &quot;Numerical Password&quot; are specified.</span></span> <span data-ttu-id="bba6c-201">Групповая политика требуется резервное копирование сведений о восстановлении в службы домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bba6c-201">The Group Policy requires a backup of recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="bba6c-202">Чтобы добавить хотя бы один предохранитель ключа этого типа, используйте метод <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>протекткэйвиснумерикалпассворд</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="bba6c-202">To add at least one key protector of that type, use the <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> method.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="bba6c-203">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bba6c-203">Remarks</span></span>

<span data-ttu-id="bba6c-204">При использовании этого метода без второго параметра (в соответствии с определением Windows 7 и Windows Vista Enterprise) метод всегда начнет преобразование в полном режиме, чтобы обеспечить обратную совместимость.</span><span class="sxs-lookup"><span data-stu-id="bba6c-204">When you use this method without the second optional parameter (according to the Windows 7 and Windows Vista Enterprise definition), the method will always initiate full mode conversion in order to keep backward compatible behavior.</span></span> <span data-ttu-id="bba6c-205">Таким образом, безопасность существующих приложений и сценариев не будет нарушена с добавлением второго необязательного параметра в Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="bba6c-205">This way the security expectation of existing applications and scripts will not be broken with the addition of the second optional parameter in Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="bba6c-206">В отличие от метода [**Encrypt**](encrypt-win32-encryptablevolume.md) , этот метод выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="bba6c-206">Unlike the [**Encrypt**](encrypt-win32-encryptablevolume.md) method, this method does the following:</span></span>

-   <span data-ttu-id="bba6c-207">Проверяет, сможет ли доверенный платформенный модуль разблокировки тома, если существует предохранитель ключа, связанный с TPM.</span><span class="sxs-lookup"><span data-stu-id="bba6c-207">Tests whether the TPM will be able to unlock the volume, if a TPM-related key protector exists.</span></span>
-   <span data-ttu-id="bba6c-208">Проверяет, может ли компьютер считывать флэш-накопитель USB, содержащий внешний файл ключа, во время запуска, если том будет разблокирован внешним ключом (включая ключ запуска).</span><span class="sxs-lookup"><span data-stu-id="bba6c-208">Tests whether the computer can read a USB flash drive that contains an external key file during start, if the volume will be unlocked by an external key (including a startup key).</span></span>
-   <span data-ttu-id="bba6c-209">Для запуска проверки оборудования требуется перезагрузка компьютера.</span><span class="sxs-lookup"><span data-stu-id="bba6c-209">Requires a computer restart to run the hardware test.</span></span>
-   <span data-ttu-id="bba6c-210">Начинает шифрование, только если проверка оборудования выполнена.</span><span class="sxs-lookup"><span data-stu-id="bba6c-210">Begins encryption only if the hardware test succeeds.</span></span>
-   <span data-ttu-id="bba6c-211">Не может использоваться на томе данных, на частично или полностью зашифрованном томе или для возобновления шифрования.</span><span class="sxs-lookup"><span data-stu-id="bba6c-211">Cannot be used on a data volume, on a partially or fully encrypted volume, or to resume encryption.</span></span>

<span data-ttu-id="bba6c-212">Перед выполнением этого метода используйте следующие методы, чтобы создать связанные предохранители ключа:</span><span class="sxs-lookup"><span data-stu-id="bba6c-212">Before running this method, use the following methods to create the related key protectors:</span></span>

-   [<span data-ttu-id="bba6c-213">**протекткэйвисекстерналкэй**</span><span class="sxs-lookup"><span data-stu-id="bba6c-213">**ProtectKeyWithExternalKey**</span></span>](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="bba6c-214">**протекткэйвистпм**</span><span class="sxs-lookup"><span data-stu-id="bba6c-214">**ProtectKeyWithTPM**</span></span>](protectkeywithtpm-win32-encryptablevolume.md)
-   [<span data-ttu-id="bba6c-215">**протекткэйвистпмандпин**</span><span class="sxs-lookup"><span data-stu-id="bba6c-215">**ProtectKeyWithTPMAndPIN**</span></span>](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [<span data-ttu-id="bba6c-216">**протекткэйвистпмандпинандстартупкэй**</span><span class="sxs-lookup"><span data-stu-id="bba6c-216">**ProtectKeyWithTPMAndPINAndStartupKey**</span></span>](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="bba6c-217">**протекткэйвистпмандстартупкэй**</span><span class="sxs-lookup"><span data-stu-id="bba6c-217">**ProtectKeyWithTPMAndStartupKey**</span></span>](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

<span data-ttu-id="bba6c-218">После выполнения этого метода выполните следующие дополнительные действия:</span><span class="sxs-lookup"><span data-stu-id="bba6c-218">After running this method, take these additional steps:</span></span>

1.  <span data-ttu-id="bba6c-219">Вставьте в компьютер флэш-накопитель USB, содержащий внешний файл ключа.</span><span class="sxs-lookup"><span data-stu-id="bba6c-219">Insert into the computer a USB flash drive that contains an external key file.</span></span> <span data-ttu-id="bba6c-220">Этот шаг применяется только в том случае, если том имеет предохранитель ключа типа "внешний ключ" или "TPM и ключ запуска".</span><span class="sxs-lookup"><span data-stu-id="bba6c-220">This step applies only if the volume has a key protector of type "External Key" or "TPM And Startup Key".</span></span>
2.  <span data-ttu-id="bba6c-221">Перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="bba6c-221">Restart the computer.</span></span>

<span data-ttu-id="bba6c-222">При перезагрузке компьютера проверка оборудования выполняется автоматически.</span><span class="sxs-lookup"><span data-stu-id="bba6c-222">On computer restart, the hardware test runs automatically.</span></span>

<span data-ttu-id="bba6c-223">Шифрование начинается, если проверка оборудования выполнена.</span><span class="sxs-lookup"><span data-stu-id="bba6c-223">Encryption begins if the hardware test succeeds.</span></span> <span data-ttu-id="bba6c-224">В противном случае попытайтесь устранить сбои оборудования.</span><span class="sxs-lookup"><span data-stu-id="bba6c-224">Otherwise, attempt to resolve any hardware failures.</span></span> <span data-ttu-id="bba6c-225">Запустите [**жесардваретестстатус**](gethardwareteststatus-win32-encryptablevolume.md) после перезагрузки компьютера, чтобы получить результаты теста.</span><span class="sxs-lookup"><span data-stu-id="bba6c-225">Run [**GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md) after restarting the computer to get test results.</span></span>

<span data-ttu-id="bba6c-226">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="bba6c-226">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bba6c-227">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="bba6c-227">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="bba6c-228">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="bba6c-228">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bba6c-229">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="bba6c-229">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bba6c-230">Требования</span><span class="sxs-lookup"><span data-stu-id="bba6c-230">Requirements</span></span>



| <span data-ttu-id="bba6c-231">Требование</span><span class="sxs-lookup"><span data-stu-id="bba6c-231">Requirement</span></span> | <span data-ttu-id="bba6c-232">Значение</span><span class="sxs-lookup"><span data-stu-id="bba6c-232">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bba6c-233">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bba6c-233">Minimum supported client</span></span><br/> | <span data-ttu-id="bba6c-234">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="bba6c-234">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="bba6c-235">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bba6c-235">Minimum supported server</span></span><br/> | <span data-ttu-id="bba6c-236">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bba6c-236">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bba6c-237">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bba6c-237">Namespace</span></span><br/>                | <span data-ttu-id="bba6c-238">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="bba6c-238">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="bba6c-239">MOF</span><span class="sxs-lookup"><span data-stu-id="bba6c-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bba6c-240"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bba6c-240"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bba6c-241">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bba6c-241">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bba6c-242">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="bba6c-242">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
