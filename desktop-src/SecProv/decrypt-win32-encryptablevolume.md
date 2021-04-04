---
description: Начинает расшифровку полностью зашифрованного тома или возобновляет расшифровку частично зашифрованного тома.
ms.assetid: 3cdbb1c1-1084-4ddb-ba8d-fc2e3ec75224
title: Метод дешифровки класса Win32_EncryptableVolume (InfoCard. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Decrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 96f7ab1c237879d83be25ddb54425ac31fcb855d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910055"
---
# <a name="decrypt-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="7a0ef-103">Метод дешифровки \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="7a0ef-103">Decrypt method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="7a0ef-104">Метод **дешифровки** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) начинает расшифровку полностью зашифрованного тома или возобновляет расшифровку частично зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="7a0ef-104">The **Decrypt** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class begins decryption of a fully encrypted volume, or resumes decryption of a partially encrypted volume.</span></span>

<span data-ttu-id="7a0ef-105">Если расшифровка приостановлена или выполняется ее выполнение, этот метод ведет себя так же, как [**ресумеконверсион**](resumeconversion-win32-encryptablevolume.md).</span><span class="sxs-lookup"><span data-stu-id="7a0ef-105">When decryption is paused or in-progress, this method behaves the same as [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md).</span></span> <span data-ttu-id="7a0ef-106">Если шифрование приостановлено или выполняется его выполнение, этот метод возвращает шифрование и начинает расшифровку.</span><span class="sxs-lookup"><span data-stu-id="7a0ef-106">When encryption is paused or in-progress, this method reverts the encryption and begins decryption.</span></span> <span data-ttu-id="7a0ef-107">После завершения расшифровки все предохранители ключа на этом томе удаляются из системы, а том преобразуется в стандартную файловую систему NTFS.</span><span class="sxs-lookup"><span data-stu-id="7a0ef-107">After decryption completes, all key protectors on this volume are removed from the system and the volume converts to a standard NTFS file system.</span></span>

> [!Note]  
> <span data-ttu-id="7a0ef-108">Если диск зашифрован аппаратно, метод **дешифровки** устанавливает для полосы состояние значение "всегда разблокировано", удаляет все связанные метаданные и обнуляет идентификатор безопасности для диска.</span><span class="sxs-lookup"><span data-stu-id="7a0ef-108">If the disc is hardware encrypted, the **Decrypt** method sets band status to "always unlocked", removes all associated metadata, and zeroes the security ID for the drive.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7a0ef-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a0ef-109">Syntax</span></span>


```mof
uint32 Decrypt();
```



## <a name="parameters"></a><span data-ttu-id="7a0ef-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a0ef-110">Parameters</span></span>

<span data-ttu-id="7a0ef-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7a0ef-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7a0ef-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a0ef-112">Return value</span></span>

<span data-ttu-id="7a0ef-113">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7a0ef-113">Type: **uint32**</span></span>

<span data-ttu-id="7a0ef-114">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="7a0ef-114">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="7a0ef-115">Этот метод немедленно возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7a0ef-115">This method returns immediately.</span></span> <span data-ttu-id="7a0ef-116">Если том уже полностью расшифровывается и другие ошибки не существуют, этот метод возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="7a0ef-116">If the volume is already fully decrypted and no other errors exist, this method returns 0.</span></span>



| <span data-ttu-id="7a0ef-117">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="7a0ef-117">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="7a0ef-118">Описание</span><span class="sxs-lookup"><span data-stu-id="7a0ef-118">Description</span></span>                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7a0ef-119"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="7a0ef-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                       | <span data-ttu-id="7a0ef-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="7a0ef-120">The method was successful.</span></span><br/>                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="7a0ef-121"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="7a0ef-121"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>      | <span data-ttu-id="7a0ef-122">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="7a0ef-122">The volume is locked.</span></span><br/>                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="7a0ef-123"><dt>**ФВЕ \_ Автоматическое \_ разблокирование с \_ включенным разкреплением**</dt> <dt>2150694953 (0x80310029)</dt></span><span class="sxs-lookup"><span data-stu-id="7a0ef-123"><dt>**FVE\_E\_AUTOUNLOCK\_ENABLED**</dt> <dt>2150694953 (0x80310029)</dt></span></span> </dl> | <span data-ttu-id="7a0ef-124">Этот том невозможно расшифровать, так как доступны ключи, используемые для автоматической разблокировки томов данных.</span><span class="sxs-lookup"><span data-stu-id="7a0ef-124">This volume cannot be decrypted because keys used to automatically unlock data volumes are available.</span></span> <br/> <span data-ttu-id="7a0ef-125">Удалите эти ключи с помощью [**клеараллаутаунлокккэйс**](clearallautounlockkeys-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="7a0ef-125">Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) to remove these keys.</span></span><br/> |



 

## <a name="security-considerations"></a><span data-ttu-id="7a0ef-126">Соображения безопасности</span><span class="sxs-lookup"><span data-stu-id="7a0ef-126">Security Considerations</span></span>

<span data-ttu-id="7a0ef-127">Вызов метода **дешифровки** оставляет данные незащищенными.</span><span class="sxs-lookup"><span data-stu-id="7a0ef-127">Calling the **Decrypt** method leaves data unprotected.</span></span>

<span data-ttu-id="7a0ef-128">Если перед использованием этого метода состояние защиты тома равно 1 (защита включена), то при успешном завершении этого метода состояние защиты изменится на 0 (защита ОТКЛЮЧЕНа), так как определение частично зашифрованного тома не защищено.</span><span class="sxs-lookup"><span data-stu-id="7a0ef-128">If the protection status of the volume is 1 (PROTECTION ON) before this method is used, successful completion of this method changes the protection status to 0 (PROTECTION OFF), since by definition a partially encrypted volume is not protected.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a0ef-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a0ef-129">Remarks</span></span>

<span data-ttu-id="7a0ef-130">Если том не был полностью расшифрован, при выполнении **расшифровки** [**жетконверсионстатус**](getconversionstatus-win32-encryptablevolume.md) указывает, что расшифровка выполняется, и показывает процентное соотношение тома, который остается зашифрованным.</span><span class="sxs-lookup"><span data-stu-id="7a0ef-130">If the volume is not already fully decrypted, running **Decrypt** causes [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to indicate that decryption is progress and shows the percentage of the volume that remains encrypted.</span></span>

<span data-ttu-id="7a0ef-131">Если перед запуском этого метода состояние защиты тома равно "on", при выполнении этого метода состояние защиты изменится на "Выкл.", так как определение частично зашифрованного тома не защищено.</span><span class="sxs-lookup"><span data-stu-id="7a0ef-131">If the protection status of the volume is "on" before this method is run, running this method changes the protection status to "off", since by definition a partially encrypted volume is not protected.</span></span>

<span data-ttu-id="7a0ef-132">Если этот метод выполняется на текущем томе операционной системы, а этот том операционной системы используется для автоматической разблокировки томов данных (см. метод [**енаблеаутаунлокк**](enableautounlock-win32-encryptablevolume.md)), необходимо сначала вызвать метод [**клеараллаутаунлокккэйс**](clearallautounlockkeys-win32-encryptablevolume.md).</span><span class="sxs-lookup"><span data-stu-id="7a0ef-132">If this method is run on the currently running operating system volume and this operating system volume is being used to automatically unlock data volumes (see method [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)) you must first call the method [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md).</span></span>

<span data-ttu-id="7a0ef-133">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="7a0ef-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7a0ef-134">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7a0ef-134">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7a0ef-135">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="7a0ef-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7a0ef-136">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="7a0ef-136">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a0ef-137">Требования</span><span class="sxs-lookup"><span data-stu-id="7a0ef-137">Requirements</span></span>



| <span data-ttu-id="7a0ef-138">Требование</span><span class="sxs-lookup"><span data-stu-id="7a0ef-138">Requirement</span></span> | <span data-ttu-id="7a0ef-139">Значение</span><span class="sxs-lookup"><span data-stu-id="7a0ef-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a0ef-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a0ef-140">Minimum supported client</span></span><br/> | <span data-ttu-id="7a0ef-141">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="7a0ef-141">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7a0ef-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a0ef-142">Minimum supported server</span></span><br/> | <span data-ttu-id="7a0ef-143">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7a0ef-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7a0ef-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7a0ef-144">Namespace</span></span><br/>                | <span data-ttu-id="7a0ef-145">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="7a0ef-145">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="7a0ef-146">Header</span><span class="sxs-lookup"><span data-stu-id="7a0ef-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a0ef-147"><dt>InfoCard. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a0ef-147"><dt>Infocard.h</dt></span></span> </dl>                   |
| <span data-ttu-id="7a0ef-148">MOF</span><span class="sxs-lookup"><span data-stu-id="7a0ef-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a0ef-149"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a0ef-149"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a0ef-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a0ef-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a0ef-151">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="7a0ef-151">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
