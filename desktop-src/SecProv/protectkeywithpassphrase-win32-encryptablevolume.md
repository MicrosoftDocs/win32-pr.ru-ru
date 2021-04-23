---
description: Использует парольную фразу для получения производного ключа.
ms.assetid: 62b070ec-4788-47cc-bfa4-6811a712ddbd
title: Метод Протекткэйвиспассфрасе класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f97806652d86b104a0f333d40d299cfa9502cf3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662292"
---
# <a name="protectkeywithpassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="618c1-103">Метод Протекткэйвиспассфрасе \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="618c1-103">ProtectKeyWithPassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="618c1-104">Метод **протекткэйвиспассфрасе** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) использует парольную фразу для получения производного ключа.</span><span class="sxs-lookup"><span data-stu-id="618c1-104">The **ProtectKeyWithPassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the passphrase to obtain the derived key.</span></span> <span data-ttu-id="618c1-105">После вычисления производного ключа используется производный ключ для защиты главного ключа зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="618c1-105">After the derived key is calculated, the derived key is used to secure the encrypted volume's master key.</span></span>

## <a name="syntax"></a><span data-ttu-id="618c1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="618c1-106">Syntax</span></span>


```mof
uint32 ProtectKeyWithPassphrase(
  [in, optional] string FriendlyName,
  [in]           string Passphrase,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="618c1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="618c1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="618c1-108">*FriendlyName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="618c1-108">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="618c1-109">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="618c1-109">Type: **string**</span></span>

<span data-ttu-id="618c1-110">Строка, указывающая назначенный пользователем строковый идентификатор для предохранителя ключа.</span><span class="sxs-lookup"><span data-stu-id="618c1-110">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="618c1-111">Если этот параметр не указан, используется пустое значение.</span><span class="sxs-lookup"><span data-stu-id="618c1-111">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="618c1-112">*Парольная фраза* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="618c1-112">*Passphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="618c1-113">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="618c1-113">Type: **string**</span></span>

<span data-ttu-id="618c1-114">Строка, указывающая парольную фразу.</span><span class="sxs-lookup"><span data-stu-id="618c1-114">A string that specifies the passphrase.</span></span>

</dd> <dt>

<span data-ttu-id="618c1-115">*Волумекэйпротекторид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="618c1-115">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="618c1-116">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="618c1-116">Type: **string**</span></span>

<span data-ttu-id="618c1-117">Строка, однозначно определяющая созданный предохранитель ключа.</span><span class="sxs-lookup"><span data-stu-id="618c1-117">A string that uniquely identifies the created key protector.</span></span>

<span data-ttu-id="618c1-118">Если диск поддерживает аппаратное шифрование, а BitLocker не использует нестандартное владение, для строки идентификатора задается значение "BitLocker", а предохранитель ключа записывается в метаданные диапазона.</span><span class="sxs-lookup"><span data-stu-id="618c1-118">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="618c1-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="618c1-119">Return value</span></span>

<span data-ttu-id="618c1-120">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="618c1-120">Type: **uint32**</span></span>

<span data-ttu-id="618c1-121">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="618c1-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="618c1-122">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="618c1-122">Return code/value</span></span>                                                                                                                                                                                        | <span data-ttu-id="618c1-123">Описание</span><span class="sxs-lookup"><span data-stu-id="618c1-123">Description</span></span>                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="618c1-124"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="618c1-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                        | <span data-ttu-id="618c1-125">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="618c1-125">The method was successful.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="618c1-126"><dt>**ФВЕ \_ E \_ не \_ разрешено \_ в \_ защищенном \_ режиме**</dt> <dt>2150694976 (0x80310040)</dt></span><span class="sxs-lookup"><span data-stu-id="618c1-126"><dt>**FVE\_E\_NOT\_ALLOWED\_IN\_SAFE\_MODE**</dt> <dt>2150694976 (0x80310040)</dt></span></span> </dl>         | <span data-ttu-id="618c1-127">Шифрование диска BitLocker можно использовать только в целях восстановления при использовании в защищенном режиме.</span><span class="sxs-lookup"><span data-stu-id="618c1-127">BitLocker Drive Encryption can only be used for recovery purposes when used in Safe Mode.</span></span><br/>                     |
| <dl> <span data-ttu-id="618c1-128"><dt>**ФВЕ \_ \_ \_ \_ Не \_ разрешена парольная фраза для политики**</dt> <dt>2150695018 (0x8031006A)</dt></span><span class="sxs-lookup"><span data-stu-id="618c1-128"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_NOT\_ALLOWED**</dt> <dt>2150695018 (0x8031006A)</dt></span></span> </dl>     | <span data-ttu-id="618c1-129">Групповая политика не позволяет создать парольную фразу.</span><span class="sxs-lookup"><span data-stu-id="618c1-129">Group policy does not permit the creation of a passphrase.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="618c1-130"><dt>**ФВЕ \_ E \_ FIPS \_ не защищает \_ парольную фразу**</dt> <dt>2150695020 (0x8031006C)</dt></span><span class="sxs-lookup"><span data-stu-id="618c1-130"><dt>**FVE\_E\_FIPS\_PREVENTS\_PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt></span></span> </dl>           | <span data-ttu-id="618c1-131">Параметр групповой политики, требующий соответствия FIPS, не позволил создать или использовать парольную фразу.</span><span class="sxs-lookup"><span data-stu-id="618c1-131">The group policy setting that requires FIPS compliance prevented the passphrase from being generated or used.</span></span><br/> |
| <dl> <span data-ttu-id="618c1-132"><dt>**ФВЕ \_ E \_ Policy \_ Недопустимая \_ \_ Длина парольной фразы**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="618c1-132"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl>  | <span data-ttu-id="618c1-133">Указанная парольная фраза не соответствует требованиям к минимальной или максимальной длине.</span><span class="sxs-lookup"><span data-stu-id="618c1-133">The passphrase provided does not meet the minimum or maximum length requirements.</span></span><br/>                             |
| <dl> <span data-ttu-id="618c1-134"><dt>**ФВЕ \_ \_ \_ \_ Слишком \_ простая парольная фраза для политики**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="618c1-134"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>      | <span data-ttu-id="618c1-135">Парольная фраза не соответствует требованиям сложности, заданным администратором в групповой политике.</span><span class="sxs-lookup"><span data-stu-id="618c1-135">The passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span><br/>            |
| <dl> <span data-ttu-id="618c1-136"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="618c1-136"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                       | <span data-ttu-id="618c1-137">Том уже заблокирован шифрование диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="618c1-137">The volume is already locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="618c1-138">Необходимо разблокировать диск с помощью панели управления.</span><span class="sxs-lookup"><span data-stu-id="618c1-138">You must unlock the drive from Control Panel.</span></span><br/>     |
| <dl> <span data-ttu-id="618c1-139"><dt>**ФВЕ \_ \_ПЕРЕкрытое \_ Обновление**</dt> <dt>2150694948 (0x80310024)</dt></span><span class="sxs-lookup"><span data-stu-id="618c1-139"><dt>**FVE\_E\_OVERLAPPED\_UPDATE**</dt> <dt>2150694948 (0x80310024)</dt></span></span> </dl>                   | <span data-ttu-id="618c1-140">Блок управления для зашифрованного тома обновлен другим потоком.</span><span class="sxs-lookup"><span data-stu-id="618c1-140">The control block for the encrypted volume was updated by another thread.</span></span><br/>                                     |
| <dl> <span data-ttu-id="618c1-141"><dt>**ФВЕ \_ \_Предохранитель ключа \_ E \_ не \_ поддерживается**</dt> <dt>2150695017 (0x80310069)</dt></span><span class="sxs-lookup"><span data-stu-id="618c1-141"><dt>**FVE\_E\_KEY\_PROTECTOR\_NOT\_SUPPORTED**</dt> <dt>2150695017 (0x80310069)</dt></span></span> </dl>       | <span data-ttu-id="618c1-142">Предохранитель ключа не поддерживается версией шифрование диска BitLocker в данный момент на томе.</span><span class="sxs-lookup"><span data-stu-id="618c1-142">The key protector is not supported by the version of BitLocker Drive Encryption currently on the volume.</span></span><br/>      |
| <dl> <span data-ttu-id="618c1-143"><dt>**ФВЕ \_ \_ \_ \_ Парольная фраза тома E OS \_ не \_ разрешена**</dt> <dt>2150695021 (0x8031006D)</dt></span><span class="sxs-lookup"><span data-stu-id="618c1-143"><dt>**FVE\_E\_OS\_VOLUME\_PASSPHRASE\_NOT\_ALLOWED**</dt> <dt>2150695021 (0x8031006D)</dt></span></span> </dl> | <span data-ttu-id="618c1-144">Парольную фразу нельзя добавить на том операционной системы.</span><span class="sxs-lookup"><span data-stu-id="618c1-144">The passphrase cannot be added to the operating system volume.</span></span> <br/>                                               |
| <dl> <span data-ttu-id="618c1-145"><dt>**ФВЕ \_ Средство \_ защиты E \_ существует**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="618c1-145"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>                    | <span data-ttu-id="618c1-146">Указанный предохранитель ключа уже существует на этом томе.</span><span class="sxs-lookup"><span data-stu-id="618c1-146">The provided key protector already exists on this volume.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="618c1-147">Требования</span><span class="sxs-lookup"><span data-stu-id="618c1-147">Requirements</span></span>



| <span data-ttu-id="618c1-148">Требование</span><span class="sxs-lookup"><span data-stu-id="618c1-148">Requirement</span></span> | <span data-ttu-id="618c1-149">Значение</span><span class="sxs-lookup"><span data-stu-id="618c1-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="618c1-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="618c1-150">Minimum supported client</span></span><br/> | <span data-ttu-id="618c1-151">Windows 7 Корпоративная, \[ только классические приложения Windows 7 Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="618c1-151">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="618c1-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="618c1-152">Minimum supported server</span></span><br/> | <span data-ttu-id="618c1-153">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="618c1-153">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="618c1-154">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="618c1-154">Namespace</span></span><br/>                | <span data-ttu-id="618c1-155">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="618c1-155">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="618c1-156">MOF</span><span class="sxs-lookup"><span data-stu-id="618c1-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="618c1-157"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="618c1-157"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="618c1-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="618c1-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="618c1-159">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="618c1-159">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




