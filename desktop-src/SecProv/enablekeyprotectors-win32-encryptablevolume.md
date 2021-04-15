---
description: Включает или возобновляет все отключенные или приостановленные предохранители ключей.
ms.assetid: 6f5a17a3-84f2-43a0-a85f-1037cd52439a
title: Метод Енаблекэйпротекторс класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 78f8502ae141458f1ae46a48d21c110b9434acd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682565"
---
# <a name="enablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="18393-103">Метод Енаблекэйпротекторс \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="18393-103">EnableKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="18393-104">Метод **енаблекэйпротекторс** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) включает или возобновляет все отключенные или приостановленные предохранители ключей.</span><span class="sxs-lookup"><span data-stu-id="18393-104">The **EnableKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class enables or resumes all disabled or suspended key protectors.</span></span> <span data-ttu-id="18393-105">Этот метод можно использовать для повторного включения или возобновления защиты BitLocker на зашифрованном томе.</span><span class="sxs-lookup"><span data-stu-id="18393-105">You can use this method to reenable or resume BitLocker protection on an encrypted volume.</span></span> <span data-ttu-id="18393-106">Этот метод гарантирует, что ключ шифрования тома не будет предоставлен на очистку на жестком диске.</span><span class="sxs-lookup"><span data-stu-id="18393-106">This method ensures that the volume's encryption key is not exposed in the clear on the hard disk.</span></span>

> [!Note]  
> <span data-ttu-id="18393-107">Если диск поддерживает аппаратное шифрование, состояние полосы изменится на "Разблокировано" из "всегда разблокировано".</span><span class="sxs-lookup"><span data-stu-id="18393-107">If the disc supports hardware encryption, the band state transitions to "unlocked" from "always unlocked".</span></span>

 

## <a name="syntax"></a><span data-ttu-id="18393-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18393-108">Syntax</span></span>


```mof
uint32 EnableKeyProtectors();
```



## <a name="parameters"></a><span data-ttu-id="18393-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="18393-109">Parameters</span></span>

<span data-ttu-id="18393-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="18393-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="18393-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18393-111">Return value</span></span>

<span data-ttu-id="18393-112">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18393-112">Type: **uint32**</span></span>

<span data-ttu-id="18393-113">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="18393-113">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="18393-114">Если предохранители ключа уже включены и другие ошибки не возникают, этот метод возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="18393-114">If key protectors are already enabled and no other errors occur, this method returns zero.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="18393-115">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="18393-115">Return code/value</span></span></th>
<th><span data-ttu-id="18393-116">Описание</span><span class="sxs-lookup"><span data-stu-id="18393-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="18393-117"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span><span class="sxs-lookup"><span data-stu-id="18393-117"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span></span></dl></td>
<td><span data-ttu-id="18393-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="18393-118">The method was successful.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="18393-119"><dt><strong>FVE_E_SECURE_KEY_REQUIRED</strong></dt> <dt>2150694919 (0x80310007)</dt> </span><span class="sxs-lookup"><span data-stu-id="18393-119"><dt><strong>FVE_E_SECURE_KEY_REQUIRED</strong></dt> <dt>2150694919 (0x80310007)</dt> </span></span></dl></td>
<td><span data-ttu-id="18393-120">На томе не существует предохранителей ключа.</span><span class="sxs-lookup"><span data-stu-id="18393-120">No key protectors exist on the volume.</span></span> <span data-ttu-id="18393-121">Чтобы указать предохранители ключа для тома, используйте один из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="18393-121">Use one of the following methods to specify key protectors for the volume:</span></span><br/>
<ul>
<li><span data-ttu-id="18393-122"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>протекткэйвисцертификатефиле</strong></a></span><span class="sxs-lookup"><span data-stu-id="18393-122"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span></span></li>
<li><span data-ttu-id="18393-123"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>протекткэйвисцертификатесумбпринт</strong></a></span><span class="sxs-lookup"><span data-stu-id="18393-123"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span></span></li>
<li><span data-ttu-id="18393-124"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>протекткэйвисекстерналкэй</strong></a></span><span class="sxs-lookup"><span data-stu-id="18393-124"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="18393-125"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>протекткэйвиснумерикалпассворд</strong></a></span><span class="sxs-lookup"><span data-stu-id="18393-125"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="18393-126"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>протекткэйвиспассфрасе</strong></a></span><span class="sxs-lookup"><span data-stu-id="18393-126"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span></span></li>
<li><span data-ttu-id="18393-127"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>протекткэйвистпм</strong></a></span><span class="sxs-lookup"><span data-stu-id="18393-127"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="18393-128"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>протекткэйвистпмандпин</strong></a></span><span class="sxs-lookup"><span data-stu-id="18393-128"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="18393-129"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>протекткэйвистпмандпинандстартупкэй</strong></a></span><span class="sxs-lookup"><span data-stu-id="18393-129"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="18393-130"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>протекткэйвистпмандстартупкэй</strong></a></span><span class="sxs-lookup"><span data-stu-id="18393-130"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="18393-131"><dt><strong>FVE_E_NOT_ACTIVATED</strong></dt> <dt>2150694920 (0x80310008)</dt> </span><span class="sxs-lookup"><span data-stu-id="18393-131"><dt><strong>FVE_E_NOT_ACTIVATED</strong></dt> <dt>2150694920 (0x80310008)</dt> </span></span></dl></td>
<td><span data-ttu-id="18393-132">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="18393-132">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="18393-133">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="18393-133">Add a key protector to enable BitLocker.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="18393-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18393-134">Remarks</span></span>

<span data-ttu-id="18393-135">Если том полностью зашифрован, успешное выполнение этого метода обеспечит защиту тома.</span><span class="sxs-lookup"><span data-stu-id="18393-135">If the volume is fully encrypted, successfully running this method ensures that the volume is protected.</span></span> <span data-ttu-id="18393-136">Если том является частично зашифрованным, то успешное выполнение этого метода означает, что том будет защищен, когда он станет полностью зашифрован.</span><span class="sxs-lookup"><span data-stu-id="18393-136">If the volume is partially encrypted, successfully running this method implies that the volume will be protected when it becomes fully encrypted.</span></span> <span data-ttu-id="18393-137">Дополнительные сведения см. в описании метода [**жетпротектионстатус**](getprotectionstatus-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="18393-137">For more information, see the [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="18393-138">Если для тома существуют предохранители ключей на основе доверенного платформенного модуля, успешное выполнение этого метода также обновляет эти предохранители, чтобы доверенный платформенный модуль проверял соответствие текущим службам запуска на платформе.</span><span class="sxs-lookup"><span data-stu-id="18393-138">If TPM-based key protectors exist for the volume, successfully running this method also refreshes these protectors so that the TPM validates against the current startup services on the platform.</span></span> <span data-ttu-id="18393-139">Иными словами, вы утверждаете, что текущее состояние компьютера является верным состоянием, на которое проверяется доверенный платформенный модуль на будущих перезапусках компьютера.</span><span class="sxs-lookup"><span data-stu-id="18393-139">In other words, you are asserting that the current computer state is the correct state that the TPM will check against on future computer restarts.</span></span>

<span data-ttu-id="18393-140">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="18393-140">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="18393-141">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="18393-141">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="18393-142">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="18393-142">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="18393-143">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="18393-143">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="18393-144">Требования</span><span class="sxs-lookup"><span data-stu-id="18393-144">Requirements</span></span>



| <span data-ttu-id="18393-145">Требование</span><span class="sxs-lookup"><span data-stu-id="18393-145">Requirement</span></span> | <span data-ttu-id="18393-146">Значение</span><span class="sxs-lookup"><span data-stu-id="18393-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18393-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18393-147">Minimum supported client</span></span><br/> | <span data-ttu-id="18393-148">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="18393-148">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="18393-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18393-149">Minimum supported server</span></span><br/> | <span data-ttu-id="18393-150">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="18393-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="18393-151">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="18393-151">Namespace</span></span><br/>                | <span data-ttu-id="18393-152">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="18393-152">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="18393-153">MOF</span><span class="sxs-lookup"><span data-stu-id="18393-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18393-154"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18393-154"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18393-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18393-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18393-156">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="18393-156">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="18393-157">**дисаблекэйпротекторс**</span><span class="sxs-lookup"><span data-stu-id="18393-157">**DisableKeyProtectors**</span></span>](disablekeyprotectors-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="18393-158">**протекткэйвисцертификатефиле**</span><span class="sxs-lookup"><span data-stu-id="18393-158">**ProtectKeyWithCertificateFile**</span></span>](protectkeywithcertificatefile-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="18393-159">**протекткэйвисцертификатесумбпринт**</span><span class="sxs-lookup"><span data-stu-id="18393-159">**ProtectKeyWithCertificateThumbprint**</span></span>](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="18393-160">**протекткэйвисекстерналкэй**</span><span class="sxs-lookup"><span data-stu-id="18393-160">**ProtectKeyWithExternalKey**</span></span>](protectkeywithexternalkey-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="18393-161">**протекткэйвиснумерикалпассворд**</span><span class="sxs-lookup"><span data-stu-id="18393-161">**ProtectKeyWithNumericalPassword**</span></span>](protectkeywithnumericalpassword-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="18393-162">**протекткэйвиспассфрасе**</span><span class="sxs-lookup"><span data-stu-id="18393-162">**ProtectKeyWithPassphrase**</span></span>](protectkeywithpassphrase-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="18393-163">**протекткэйвистпм**</span><span class="sxs-lookup"><span data-stu-id="18393-163">**ProtectKeyWithTPM**</span></span>](protectkeywithtpm-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="18393-164">**протекткэйвистпмандпин**</span><span class="sxs-lookup"><span data-stu-id="18393-164">**ProtectKeyWithTPMAndPIN**</span></span>](protectkeywithtpmandpin-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="18393-165">**протекткэйвистпмандпинандстартупкэй**</span><span class="sxs-lookup"><span data-stu-id="18393-165">**ProtectKeyWithTPMAndPINAndStartupKey**</span></span>](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="18393-166">**протекткэйвистпмандстартупкэй**</span><span class="sxs-lookup"><span data-stu-id="18393-166">**ProtectKeyWithTPMAndStartupKey**</span></span>](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)
</dt> </dl>

 

 
