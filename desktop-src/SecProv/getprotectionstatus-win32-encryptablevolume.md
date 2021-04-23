---
description: Указывает, защищен ли том и его ключ шифрования.
ms.assetid: bcd8fce5-da39-4aa8-93ff-0768deb900ec
title: Метод Жетпротектионстатус класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetProtectionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 5f3fa2aaa019097a01a6e6d1628d7c4fe9b82710
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809281"
---
# <a name="getprotectionstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="4f565-103">Метод Жетпротектионстатус \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="4f565-103">GetProtectionStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="4f565-104">Метод **жетпротектионстатус** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) указывает, защищен ли том и его ключ шифрования (если он есть).</span><span class="sxs-lookup"><span data-stu-id="4f565-104">The **GetProtectionStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the volume and its encryption key (if any) are secured.</span></span>

<span data-ttu-id="4f565-105">Защита отключена, если том не зашифрован или частично зашифрован, или если ключ шифрования тома доступен на жестком диске в открытом состоянии.</span><span class="sxs-lookup"><span data-stu-id="4f565-105">Protection is off if a volume is unencrypted or partially encrypted, or if the volume's encryption key is available in the clear on the hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f565-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f565-106">Syntax</span></span>


```mof
uint32 GetProtectionStatus(
  [out] uint32 ProtectionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="4f565-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f565-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f565-108">*Состояние защиты* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4f565-108">*ProtectionStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f565-109">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f565-109">Type: **uint32**</span></span>

<span data-ttu-id="4f565-110">Указывает, защищен ли том и ключ шифрования (если он есть).</span><span class="sxs-lookup"><span data-stu-id="4f565-110">Specifies whether the volume and the encryption key (if any) are secured.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4f565-111">Значение</span><span class="sxs-lookup"><span data-stu-id="4f565-111">Value</span></span></th>
<th><span data-ttu-id="4f565-112">Значение</span><span class="sxs-lookup"><span data-stu-id="4f565-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span><dl> <span data-ttu-id="4f565-113"><dt><strong>Незащищенный</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="4f565-113"><dt><strong>Unprotected</strong></dt> <dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="4f565-114">ЗАЩИТА ОТКЛЮЧЕНА</span><span class="sxs-lookup"><span data-stu-id="4f565-114">PROTECTION OFF</span></span><br/> <span data-ttu-id="4f565-115">Для стандартного жесткого диска:</span><span class="sxs-lookup"><span data-stu-id="4f565-115">For a standard HDD:</span></span><br/> <span data-ttu-id="4f565-116">Том не зашифрован, частично зашифрован, или ключ шифрования тома доступен в CLEAR на жестком диске.</span><span class="sxs-lookup"><span data-stu-id="4f565-116">The volume is unencrypted, partially encrypted, or the volume's encryption key is available in the clear on the hard disk.</span></span> <span data-ttu-id="4f565-117">Ключ шифрования можно очистить на жестком диске, если предохранители ключа были отключены с помощью метода <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>дисаблекэйпротекторс</strong></a> или если предохранители ключа не были указаны с помощью следующих методов.</span><span class="sxs-lookup"><span data-stu-id="4f565-117">The encryption key is available in the clear on the hard disk if key protectors have been disabled by using the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method or if no key protectors have been specified by using the following methods:</span></span>
<ul>
<li><span data-ttu-id="4f565-118"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>протекткэйвисцертификатефиле</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f565-118"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span></span></li>
<li><span data-ttu-id="4f565-119"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>протекткэйвисцертификатесумбпринт</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f565-119"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span></span></li>
<li><span data-ttu-id="4f565-120"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>протекткэйвисекстерналкэй</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f565-120"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="4f565-121"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>протекткэйвиснумерикалпассворд</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f565-121"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="4f565-122"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>протекткэйвиспассфрасе</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f565-122"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span></span></li>
<li><span data-ttu-id="4f565-123"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>протекткэйвистпм</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f565-123"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="4f565-124"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>протекткэйвистпмандпин</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f565-124"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="4f565-125"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>протекткэйвистпмандпинандстартупкэй</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f565-125"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="4f565-126"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>протекткэйвистпмандстартупкэй</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f565-126"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="4f565-127">Для ЕХДД:</span><span class="sxs-lookup"><span data-stu-id="4f565-127">For an EHDD:</span></span><br/> <span data-ttu-id="4f565-128">Полоса для тома бессрочно разблокирована, не имеет диспетчера ключей или управляется сторонним диспетчером ключей.</span><span class="sxs-lookup"><span data-stu-id="4f565-128">The band for the volume is perpetually unlocked, has no key manager, or is managed by a third party key manager.</span></span><br/> <span data-ttu-id="4f565-129">Это также может означать, что Управление полосой осуществляется с помощью BitLocker, но был вызван метод <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>дисаблекэйпротекторс</strong></a> и диск приостановлен.</span><span class="sxs-lookup"><span data-stu-id="4f565-129">This can also mean that the band is managed by BitLocker but the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method has been called and the drive is suspended.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span><dl> <span data-ttu-id="4f565-130"><dt><strong>Защищено</strong></dt> <dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="4f565-130"><dt><strong>Protected</strong></dt> <dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="4f565-131">ЗАЩИТА ВКЛЮЧЕНА</span><span class="sxs-lookup"><span data-stu-id="4f565-131">PROTECTION ON</span></span><br/> <span data-ttu-id="4f565-132">Для стандартного жесткого диска:</span><span class="sxs-lookup"><span data-stu-id="4f565-132">For a standard HDD:</span></span><br/> <span data-ttu-id="4f565-133">Том полностью зашифрован, а ключ шифрования для тома недоступен на жестком диске.</span><span class="sxs-lookup"><span data-stu-id="4f565-133">The volume is fully encrypted and the encryption key for the volume is not available in the clear on the hard disk.</span></span><br/> <span data-ttu-id="4f565-134">Для ЕХДД:</span><span class="sxs-lookup"><span data-stu-id="4f565-134">For an EHDD:</span></span><br/> <span data-ttu-id="4f565-135">BitLocker является диспетчером ключей для полосы.</span><span class="sxs-lookup"><span data-stu-id="4f565-135">BitLocker is the key manager for the band.</span></span> <span data-ttu-id="4f565-136">Диск может быть заблокирован или разблокирован, но не может быть бессрочно разблокирован.</span><span class="sxs-lookup"><span data-stu-id="4f565-136">The drive can be locked or unlocked but cannot be perpetually unlocked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="4f565-137"><dt><strong>Неизвестно</strong></dt> <dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="4f565-137"><dt><strong>Unknown</strong></dt> <dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="4f565-138">Невозможно определить состояние защиты тома.</span><span class="sxs-lookup"><span data-stu-id="4f565-138">The volume protection status cannot be determined.</span></span> <span data-ttu-id="4f565-139">Это может быть вызвано тем, что том находится в заблокированном состоянии.</span><span class="sxs-lookup"><span data-stu-id="4f565-139">This can be caused by the volume being in a locked state.</span></span><br/> <span data-ttu-id="4f565-140"><strong>Windows Vista Ultimate, Windows Vista Корпоративная и Windows Server 2008:</strong> Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4f565-140"><strong>Windows Vista Ultimate, Windows Vista Enterprise and Windows Server 2008:</strong> This value is not supported.</span></span> <span data-ttu-id="4f565-141">Это значение поддерживается начиная с Windows 7 и Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="4f565-141">This value is supported beginning with Windows 7 and Windows Server 2008 R2.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f565-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f565-142">Return value</span></span>

<span data-ttu-id="4f565-143">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f565-143">Type: **uint32**</span></span>

<span data-ttu-id="4f565-144">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="4f565-144">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="4f565-145">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="4f565-145">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="4f565-146">Описание</span><span class="sxs-lookup"><span data-stu-id="4f565-146">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="4f565-147"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="4f565-147"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="4f565-148">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="4f565-148">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4f565-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4f565-149">Remarks</span></span>

<span data-ttu-id="4f565-150">Шифрование тома возможно только в том случае, если вы либо вызываете [**дисаблекэйпротекторс**](disablekeyprotectors-win32-encryptablevolume.md) , либо используете один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="4f565-150">You can encrypt a volume only if you either call [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) first or use one of the following methods:</span></span>

-   [<span data-ttu-id="4f565-151">**протекткэйвисцертификатефиле**</span><span class="sxs-lookup"><span data-stu-id="4f565-151">**ProtectKeyWithCertificateFile**</span></span>](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [<span data-ttu-id="4f565-152">**протекткэйвисцертификатесумбпринт**</span><span class="sxs-lookup"><span data-stu-id="4f565-152">**ProtectKeyWithCertificateThumbprint**</span></span>](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [<span data-ttu-id="4f565-153">**протекткэйвисекстерналкэй**</span><span class="sxs-lookup"><span data-stu-id="4f565-153">**ProtectKeyWithExternalKey**</span></span>](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="4f565-154">**протекткэйвиснумерикалпассворд**</span><span class="sxs-lookup"><span data-stu-id="4f565-154">**ProtectKeyWithNumericalPassword**</span></span>](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [<span data-ttu-id="4f565-155">**протекткэйвиспассфрасе**</span><span class="sxs-lookup"><span data-stu-id="4f565-155">**ProtectKeyWithPassphrase**</span></span>](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [<span data-ttu-id="4f565-156">**протекткэйвистпм**</span><span class="sxs-lookup"><span data-stu-id="4f565-156">**ProtectKeyWithTPM**</span></span>](protectkeywithtpm-win32-encryptablevolume.md)
-   [<span data-ttu-id="4f565-157">**протекткэйвистпмандпин**</span><span class="sxs-lookup"><span data-stu-id="4f565-157">**ProtectKeyWithTPMAndPIN**</span></span>](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [<span data-ttu-id="4f565-158">**протекткэйвистпмандпинандстартупкэй**</span><span class="sxs-lookup"><span data-stu-id="4f565-158">**ProtectKeyWithTPMAndPINAndStartupKey**</span></span>](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="4f565-159">**протекткэйвистпмандстартупкэй**</span><span class="sxs-lookup"><span data-stu-id="4f565-159">**ProtectKeyWithTPMAndStartupKey**</span></span>](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

<span data-ttu-id="4f565-160">Поэтому, если диск зашифрован и *состояние защиты* возвращает ноль (защита отключена), ключи отключаются.</span><span class="sxs-lookup"><span data-stu-id="4f565-160">Therefore, if the disk is encrypted and *ProtectionStatus* returns zero (PROTECTION OFF), keys are disabled.</span></span>

<span data-ttu-id="4f565-161">Используйте [**жеткэйпротекторс**](getkeyprotectors-win32-encryptablevolume.md) , чтобы получить список предохранителей ключей, которые были указаны для защиты ключа шифрования тома.</span><span class="sxs-lookup"><span data-stu-id="4f565-161">Use [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md) to list the key protectors that have been specified to secure the volume's encryption key.</span></span> <span data-ttu-id="4f565-162">Если предохранители ключа существуют, но защита равна нулю (защита ОТКЛЮЧЕНа), используйте [**енаблекэйпротекторс**](enablekeyprotectors-win32-encryptablevolume.md) , чтобы включить защиту тома.</span><span class="sxs-lookup"><span data-stu-id="4f565-162">If key protectors exist but protection is zero (PROTECTION OFF), use [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) to turn on volume protection.</span></span>

<span data-ttu-id="4f565-163">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="4f565-163">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4f565-164">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4f565-164">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="4f565-165">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="4f565-165">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4f565-166">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="4f565-166">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f565-167">Требования</span><span class="sxs-lookup"><span data-stu-id="4f565-167">Requirements</span></span>



| <span data-ttu-id="4f565-168">Требование</span><span class="sxs-lookup"><span data-stu-id="4f565-168">Requirement</span></span> | <span data-ttu-id="4f565-169">Значение</span><span class="sxs-lookup"><span data-stu-id="4f565-169">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f565-170">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f565-170">Minimum supported client</span></span><br/> | <span data-ttu-id="4f565-171">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="4f565-171">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4f565-172">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f565-172">Minimum supported server</span></span><br/> | <span data-ttu-id="4f565-173">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4f565-173">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4f565-174">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4f565-174">Namespace</span></span><br/>                | <span data-ttu-id="4f565-175">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="4f565-175">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="4f565-176">MOF</span><span class="sxs-lookup"><span data-stu-id="4f565-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f565-177"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f565-177"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f565-178">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f565-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f565-179">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="4f565-179">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
