---
description: Указывает состояние шифрования или расшифровки тома.
ms.assetid: b292a380-1b4a-4dff-948b-6494ec3b400b
title: Метод Жетконверсионстатус класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetConversionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 9357db3397b04639329c1afd502d9da30cbb39be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897058"
---
# <a name="getconversionstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="e394a-103">Метод Жетконверсионстатус \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="e394a-103">GetConversionStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="e394a-104">Метод **жетконверсионстатус** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) указывает состояние шифрования или расшифровки тома.</span><span class="sxs-lookup"><span data-stu-id="e394a-104">The **GetConversionStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates the status of the encryption or decryption on the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="e394a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e394a-105">Syntax</span></span>


```mof
uint32 GetConversionStatus(
  [out] uint32 ConversionStatus,
  [out] uint32 EncryptionPercentage,
  [out] uint32 EncryptionFlags,
  [out] uint32 WipingStatus,
  [out] uint32 WipingPercentage,
  [in]  uint32 PrecisionFactor
);
```



## <a name="parameters"></a><span data-ttu-id="e394a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e394a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e394a-107">*Конверсионстатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e394a-107">*ConversionStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e394a-108">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e394a-108">Type: **uint32**</span></span>

<span data-ttu-id="e394a-109">Состояние шифрования тома или расшифровки.</span><span class="sxs-lookup"><span data-stu-id="e394a-109">Volume encryption or decryption status.</span></span> <span data-ttu-id="e394a-110">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e394a-110">This can be one of the following values.</span></span>



| <span data-ttu-id="e394a-111">Значение</span><span class="sxs-lookup"><span data-stu-id="e394a-111">Value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="e394a-112">Значение</span><span class="sxs-lookup"><span data-stu-id="e394a-112">Meaning</span></span>                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FullyDecrypted"></span><span id="fullydecrypted"></span><span id="FULLYDECRYPTED"></span><dl> <span data-ttu-id="e394a-113"><dt>**Фуллидекриптед**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e394a-113"><dt>**FullyDecrypted**</dt> <dt>0</dt></span></span> </dl>                         | <span data-ttu-id="e394a-114">Для стандартного жесткого диска (HDD) том полностью расшифровывается.</span><span class="sxs-lookup"><span data-stu-id="e394a-114">For a standard hard drive (HDD), the volume is fully decrypted.</span></span><br/> <span data-ttu-id="e394a-115">Для аппаратно зашифрованного жесткого диска (ЕХДД) том бессрочно разблокируется.</span><span class="sxs-lookup"><span data-stu-id="e394a-115">For a hardware encrypted hard drive (EHDD), the volume is perpetually unlocked.</span></span><br/>     |
| <span id="FullyEncrypted"></span><span id="fullyencrypted"></span><span id="FULLYENCRYPTED"></span><dl> <span data-ttu-id="e394a-116"><dt>**Фулленкриптед**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e394a-116"><dt>**FullyEncrypted**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="e394a-117">Для стандартного жесткого диска (HDD) том полностью зашифрован.</span><span class="sxs-lookup"><span data-stu-id="e394a-117">For a standard hard drive (HDD), the volume is fully encrypted.</span></span><br/> <span data-ttu-id="e394a-118">Для аппаратно зашифрованного жесткого диска (ЕХДД) том не блокируется бессрочно.</span><span class="sxs-lookup"><span data-stu-id="e394a-118">For a hardware encrypted hard drive (EHDD), the volume is not perpetually unlocked.</span></span><br/> |
| <span id="EncryptionInProgress"></span><span id="encryptioninprogress"></span><span id="ENCRYPTIONINPROGRESS"></span><dl> <span data-ttu-id="e394a-119"><dt>**EncryptionInProgress**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e394a-119"><dt>**EncryptionInProgress**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="e394a-120">Том является частично зашифрованным.</span><span class="sxs-lookup"><span data-stu-id="e394a-120">The volume is partially encrypted.</span></span><br/>                                                                                                                             |
| <span id="DecryptionInProgress"></span><span id="decryptioninprogress"></span><span id="DECRYPTIONINPROGRESS"></span><dl> <span data-ttu-id="e394a-121"><dt>**Декриптионинпрогресс**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e394a-121"><dt>**DecryptionInProgress**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="e394a-122">Том является частично зашифрованным.</span><span class="sxs-lookup"><span data-stu-id="e394a-122">The volume is partially encrypted.</span></span><br/>                                                                                                                             |
| <span id="EncryptionPaused"></span><span id="encryptionpaused"></span><span id="ENCRYPTIONPAUSED"></span><dl> <span data-ttu-id="e394a-123"><dt>**Енкриптионпаусед**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e394a-123"><dt>**EncryptionPaused**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="e394a-124">Том приостановлен во время выполнения шифрования.</span><span class="sxs-lookup"><span data-stu-id="e394a-124">The volume has been paused during the encryption progress.</span></span> <span data-ttu-id="e394a-125">Том является частично зашифрованным.</span><span class="sxs-lookup"><span data-stu-id="e394a-125">The volume is partially encrypted.</span></span><br/>                                                                  |
| <span id="DecryptionPaused"></span><span id="decryptionpaused"></span><span id="DECRYPTIONPAUSED"></span><dl> <span data-ttu-id="e394a-126"><dt>**Декриптионпаусед**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e394a-126"><dt>**DecryptionPaused**</dt> <dt>5</dt></span></span> </dl>                 | <span data-ttu-id="e394a-127">Том был приостановлен во время расшифровки.</span><span class="sxs-lookup"><span data-stu-id="e394a-127">The volume has been paused during the decryption progress.</span></span> <span data-ttu-id="e394a-128">Том является частично зашифрованным.</span><span class="sxs-lookup"><span data-stu-id="e394a-128">The volume is partially encrypted.</span></span><br/>                                                                  |



 

</dd> <dt>

<span data-ttu-id="e394a-129">*Енкриптионперцентаже* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e394a-129">*EncryptionPercentage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e394a-130">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e394a-130">Type: **uint32**</span></span>

<span data-ttu-id="e394a-131">Процент зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="e394a-131">Percentage of the volume that is encrypted.</span></span> <span data-ttu-id="e394a-132">Это целое число от 0 до 100 включительно.</span><span class="sxs-lookup"><span data-stu-id="e394a-132">This is an integer from 0 to 100 inclusive.</span></span>

<span data-ttu-id="e394a-133">Из-за округления чисел значение шифрования 0 или 100 не обязательно указывает на то, что диск полностью расшифровывается или полностью зашифрован.</span><span class="sxs-lookup"><span data-stu-id="e394a-133">Due to rounding of numbers, an encryption percentage of 0 or 100 does not necessarily indicate that the disk is fully decrypted or fully encrypted.</span></span> <span data-ttu-id="e394a-134">Всегда используйте *конверсионстатус* , чтобы определить, полностью ли расшифровывается или полностью зашифрован диск.</span><span class="sxs-lookup"><span data-stu-id="e394a-134">Always use *ConversionStatus* to determine whether the disk is in fact fully decrypted or fully encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="e394a-135">*Енкриптионфлагс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e394a-135">*EncryptionFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e394a-136">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e394a-136">Type: **uint32**</span></span>

<span data-ttu-id="e394a-137">Флаги, описывающие поведение шифрования.</span><span class="sxs-lookup"><span data-stu-id="e394a-137">Flags that describe the encryption behavior.</span></span>

<span data-ttu-id="e394a-138">Сочетание 32 бит, в котором в настоящее время определены следующие биты.</span><span class="sxs-lookup"><span data-stu-id="e394a-138">A combination of 32 bits with following bits currently defined.</span></span>



| <span data-ttu-id="e394a-139">Значение</span><span class="sxs-lookup"><span data-stu-id="e394a-139">Value</span></span>                                                                                  | <span data-ttu-id="e394a-140">Значение</span><span class="sxs-lookup"><span data-stu-id="e394a-140">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e394a-141"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="e394a-141"><dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="e394a-142">При запуске нового процесса шифрования Шифрование томов выполняется в режиме шифрования только для данных.</span><span class="sxs-lookup"><span data-stu-id="e394a-142">Perform volume encryption in data-only encryption mode when starting new encryption process.</span></span> <span data-ttu-id="e394a-143">Если шифрование приостановлено или остановлено, вызов метода [**Encrypt**](encrypt-win32-encryptablevolume.md) эффективно возобновляет преобразование, а значение этого бита игнорируется.</span><span class="sxs-lookup"><span data-stu-id="e394a-143">If encryption has been paused or stopped, calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method effectively resumes conversion and the value of this bit is ignored.</span></span> <span data-ttu-id="e394a-144">Этот бит действует только в том случае, если методы **Encrypt** или [**енкриптафтерхардваретест**](encryptafterhardwaretest-win32-encryptablevolume.md) запускают шифрование из полностью расшифрованного состояния, выполняется расшифровка или приостановленное состояние расшифровки.</span><span class="sxs-lookup"><span data-stu-id="e394a-144">This bit only has effect when either the **Encrypt** or [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) methods start encryption from the fully decrypted state, decryption in progress state, or decryption paused state.</span></span> <span data-ttu-id="e394a-145">Если этот бит равен нулю, то есть он не задан, при запуске нового процесса шифрования будет выполнено преобразование в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="e394a-145">If this bit is zero, meaning that it is not set, when starting new encryption process, then full mode conversion will be performed.</span></span><br/> |
| <dl> <span data-ttu-id="e394a-146"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="e394a-146"><dt>0x00000002</dt></span></span> </dl>  | <span data-ttu-id="e394a-147">Выполните очистку свободного места тома по требованию.</span><span class="sxs-lookup"><span data-stu-id="e394a-147">Perform on-demand wipe of the volume free space.</span></span> <span data-ttu-id="e394a-148">Вызов метода [**Encrypt**](encrypt-win32-encryptablevolume.md) с этим набором битов разрешен только в том случае, если в настоящее время не выполняется преобразование или очистка тома и он находится в зашифрованном состоянии.</span><span class="sxs-lookup"><span data-stu-id="e394a-148">Calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method with this bit set is only allowed when volume is not currently converting or wiping and is in an "encrypted" state.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="e394a-149"><dt>0x00010000 </dt></span><span class="sxs-lookup"><span data-stu-id="e394a-149"><dt>0x00010000 </dt></span></span> </dl> | <span data-ttu-id="e394a-150">Выполнение запрошенной операции в синхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="e394a-150">Perform the requested operation synchronously.</span></span> <span data-ttu-id="e394a-151">Вызов блокируется до тех пор, пока запрошенная операция не будет завершена или была прервана.</span><span class="sxs-lookup"><span data-stu-id="e394a-151">The call will block until requested operation has completed or was interrupted.</span></span> <span data-ttu-id="e394a-152">Этот флаг поддерживается только при использовании метода [**Encrypt**](encrypt-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="e394a-152">This flag is only supported with the [**Encrypt**](encrypt-win32-encryptablevolume.md) method.</span></span> <span data-ttu-id="e394a-153">Этот флаг можно указать при вызове **шифрования** для возобновления остановки или прекращения шифрования или очистки, а также при выполнении шифрования или очистки.</span><span class="sxs-lookup"><span data-stu-id="e394a-153">This flag can be specified when **Encrypt** is called to resume stopped or interrupted encryption or wiping or when either encryption or wiping is in progress.</span></span> <span data-ttu-id="e394a-154">Это позволяет вызывающему объекту возобновить синхронное ожидание до завершения или прерывания процесса.</span><span class="sxs-lookup"><span data-stu-id="e394a-154">This allows the caller to resume synchronously waiting until the process is completed or interrupted.</span></span><br/>                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="e394a-155">*Випингстатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e394a-155">*WipingStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e394a-156">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e394a-156">Type: **uint32**</span></span>

<span data-ttu-id="e394a-157">Состояние очистки свободного пространства.</span><span class="sxs-lookup"><span data-stu-id="e394a-157">Free space wiping status.</span></span> <span data-ttu-id="e394a-158">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e394a-158">This can be one of the following values.</span></span>



| <span data-ttu-id="e394a-159">Значение</span><span class="sxs-lookup"><span data-stu-id="e394a-159">Value</span></span>                                                                                                                                                                                                                                                                                               | <span data-ttu-id="e394a-160">Значение</span><span class="sxs-lookup"><span data-stu-id="e394a-160">Meaning</span></span>                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="FreeSpaceNotWiped"></span><span id="freespacenotwiped"></span><span id="FREESPACENOTWIPED"></span><dl> <span data-ttu-id="e394a-161"><dt>**Фриспаценотвипед**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e394a-161"><dt>**FreeSpaceNotWiped**</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="e394a-162">Свободное пространство не очищено.</span><span class="sxs-lookup"><span data-stu-id="e394a-162">The free space has not been wiped.</span></span><br/>          |
| <span id="FreeSpaceWiped"></span><span id="freespacewiped"></span><span id="FREESPACEWIPED"></span><dl> <span data-ttu-id="e394a-163"><dt>**Фриспацевипед**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e394a-163"><dt>**FreeSpaceWiped**</dt> <dt>1</dt></span></span> </dl>                                             | <span data-ttu-id="e394a-164">Свободное пространство очищено.</span><span class="sxs-lookup"><span data-stu-id="e394a-164">The free space has been wiped.</span></span><br/>              |
| <span id="FreeSpaceWipingInProgress"></span><span id="freespacewipinginprogress"></span><span id="FREESPACEWIPINGINPROGRESS"></span><dl> <span data-ttu-id="e394a-165"><dt>**Фриспацевипингинпрогресс**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e394a-165"><dt>**FreeSpaceWipingInProgress**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="e394a-166">Очистка свободного пространства сейчас выполняется.</span><span class="sxs-lookup"><span data-stu-id="e394a-166">Free space wiping is currently in progress.</span></span><br/> |
| <span id="FreeSpaceWipingPaused"></span><span id="freespacewipingpaused"></span><span id="FREESPACEWIPINGPAUSED"></span><dl> <span data-ttu-id="e394a-167"><dt>**Фриспацевипингпаусед**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e394a-167"><dt>**FreeSpaceWipingPaused**</dt> <dt>3</dt></span></span> </dl>                 | <span data-ttu-id="e394a-168">Очистка свободного пространства приостановлена.</span><span class="sxs-lookup"><span data-stu-id="e394a-168">Free space wiping has been paused.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="e394a-169">*Випингперцентаже* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e394a-169">*WipingPercentage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e394a-170">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e394a-170">Type: **uint32**</span></span>

<span data-ttu-id="e394a-171">Значение от 0 до 100, указывающее процент свободного пространства, которое было очищено.</span><span class="sxs-lookup"><span data-stu-id="e394a-171">A value from 0 to 100 that specifies the percentage of free space that has been wiped.</span></span>

</dd> <dt>

<span data-ttu-id="e394a-172">*ПреЦисионфактор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e394a-172">*PrecisionFactor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e394a-173">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e394a-173">Type: **uint32**</span></span>

<span data-ttu-id="e394a-174">Значение от 0 до 4, указывающее уровень точности</span><span class="sxs-lookup"><span data-stu-id="e394a-174">A value from 0 to 4 that specifies the precision level</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e394a-175">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e394a-175">Return value</span></span>

<span data-ttu-id="e394a-176">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e394a-176">Type: **uint32**</span></span>

<span data-ttu-id="e394a-177">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="e394a-177">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="e394a-178">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="e394a-178">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="e394a-179">Описание</span><span class="sxs-lookup"><span data-stu-id="e394a-179">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="e394a-180"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="e394a-180"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="e394a-181">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="e394a-181">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="e394a-182"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="e394a-182"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="e394a-183">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="e394a-183">The volume is locked.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="e394a-184">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e394a-184">Remarks</span></span>

<span data-ttu-id="e394a-185">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="e394a-185">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e394a-186">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e394a-186">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="e394a-187">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="e394a-187">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e394a-188">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="e394a-188">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e394a-189">Требования</span><span class="sxs-lookup"><span data-stu-id="e394a-189">Requirements</span></span>



| <span data-ttu-id="e394a-190">Требование</span><span class="sxs-lookup"><span data-stu-id="e394a-190">Requirement</span></span> | <span data-ttu-id="e394a-191">Значение</span><span class="sxs-lookup"><span data-stu-id="e394a-191">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e394a-192">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e394a-192">Minimum supported client</span></span><br/> | <span data-ttu-id="e394a-193">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="e394a-193">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e394a-194">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e394a-194">Minimum supported server</span></span><br/> | <span data-ttu-id="e394a-195">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e394a-195">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e394a-196">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e394a-196">Namespace</span></span><br/>                | <span data-ttu-id="e394a-197">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="e394a-197">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="e394a-198">MOF</span><span class="sxs-lookup"><span data-stu-id="e394a-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e394a-199"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e394a-199"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e394a-200">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e394a-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e394a-201">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="e394a-201">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
