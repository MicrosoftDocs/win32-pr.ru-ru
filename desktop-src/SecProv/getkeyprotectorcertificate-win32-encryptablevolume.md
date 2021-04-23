---
description: Извлекает открытый ключ и отпечаток сертификата для предохранителя открытого ключа.
ms.assetid: 86fd0562-feb9-4b85-b27b-30270f864d8e
title: Метод Жеткэйпротекторцертификате класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3954d3c55c4695e501d486f309598569b1facfc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684063"
---
# <a name="getkeyprotectorcertificate-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="3237e-103">Метод Жеткэйпротекторцертификате \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="3237e-103">GetKeyProtectorCertificate method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="3237e-104">Метод **жеткэйпротекторцертификате** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) извлекает [*открытый ключ*](../secgloss/p-gly.md) и отпечаток [*сертификата*](../secgloss/c-gly.md) для предохранителя открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="3237e-104">The **GetKeyProtectorCertificate** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the [*public key*](../secgloss/p-gly.md) and [*certificate*](../secgloss/c-gly.md) thumbprint for a public key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="3237e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3237e-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PublicKey[],
  [out] string CertThumbprint,
  [out] uint32 CertType
);
```



## <a name="parameters"></a><span data-ttu-id="3237e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3237e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3237e-107">*Волумекэйпротекторид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3237e-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3237e-108">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="3237e-108">Type: **string**</span></span>

<span data-ttu-id="3237e-109">Уникальный строковый идентификатор, используемый для управления предохранителем ключа зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="3237e-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="3237e-110">*PublicKey* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3237e-110">*PublicKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3237e-111">Тип: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="3237e-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="3237e-112">Массив байтов, указывающий открытый ключ.</span><span class="sxs-lookup"><span data-stu-id="3237e-112">An array of bytes that specifies the public key.</span></span>

</dd> <dt>

<span data-ttu-id="3237e-113">*CertThumbprint* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3237e-113">*CertThumbprint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3237e-114">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="3237e-114">Type: **string**</span></span>

<span data-ttu-id="3237e-115">Строка, указывающая отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="3237e-115">A string that specifies the certificate thumbprint.</span></span>

</dd> <dt>

<span data-ttu-id="3237e-116">*Типом* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3237e-116">*CertType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3237e-117">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3237e-117">Type: **uint32**</span></span>

<span data-ttu-id="3237e-118">Целое число без знака, указывающее тип предохранителя ключа.</span><span class="sxs-lookup"><span data-stu-id="3237e-118">An unsigned integer that specifies the type of the key protector.</span></span> <span data-ttu-id="3237e-119">Это целое число используется для различения агента восстановления данных (DRA) и сертификатов пользователей.</span><span class="sxs-lookup"><span data-stu-id="3237e-119">This integer is used to differentiate between data recovery agent (DRA) and user certificates.</span></span>



| <span data-ttu-id="3237e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="3237e-120">Value</span></span>                                                                        | <span data-ttu-id="3237e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3237e-121">Meaning</span></span>                                  |
|------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="3237e-122"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3237e-122"><dt>1</dt></span></span> </dl> | <span data-ttu-id="3237e-123">Сертификат является агентом DRA.</span><span class="sxs-lookup"><span data-stu-id="3237e-123">The certificate is a DRA.</span></span><br/>     |
| <dl> <span data-ttu-id="3237e-124"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3237e-124"><dt>2</dt></span></span> </dl> | <span data-ttu-id="3237e-125">Сертификат не является агентом DRA.</span><span class="sxs-lookup"><span data-stu-id="3237e-125">The certificate is not a DRA.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3237e-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3237e-126">Return value</span></span>

<span data-ttu-id="3237e-127">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3237e-127">Type: **uint32**</span></span>

<span data-ttu-id="3237e-128">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="3237e-128">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="3237e-129">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="3237e-129">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="3237e-130">Описание</span><span class="sxs-lookup"><span data-stu-id="3237e-130">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3237e-131"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="3237e-131"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="3237e-132">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="3237e-132">The method was successful.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="3237e-133"><dt>**Д \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="3237e-133"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                               | <span data-ttu-id="3237e-134">Указанный предохранитель ключа не является предохранителем ключа.</span><span class="sxs-lookup"><span data-stu-id="3237e-134">The specified key protector is not a key protector.</span></span> <span data-ttu-id="3237e-135">Необходимо ввести другой предохранитель ключа.</span><span class="sxs-lookup"><span data-stu-id="3237e-135">You must enter another key protector.</span></span><br/>            |
| <dl> <span data-ttu-id="3237e-136"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="3237e-136"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                      | <span data-ttu-id="3237e-137">Этот диск заблокирован шифрование диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3237e-137">This drive is locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="3237e-138">Необходимо разблокировать этот том с панели управления.</span><span class="sxs-lookup"><span data-stu-id="3237e-138">You must unlock this volume from Control Panel.</span></span> <br/> |
| <dl> <span data-ttu-id="3237e-139"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="3237e-139"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="3237e-140">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="3237e-140">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="3237e-141">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3237e-141">Add a key protector to enable BitLocker.</span></span> <br/>                    |
| <dl> <span data-ttu-id="3237e-142"><dt>**ФВЕ \_ \_ \_ \_ \_ Требуется сертификат пользователя политики**</dt> <dt>2150695027 (0x80310073)</dt></span><span class="sxs-lookup"><span data-stu-id="3237e-142"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_REQUIRED**</dt> <dt>2150695027 (0x80310073)</dt></span></span> </dl> | <span data-ttu-id="3237e-143">Групповая политика требует использования сертификата пользователя, например смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="3237e-143">Group Policy requires the use of a user certificate, such as a smart card.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="3237e-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3237e-144">Remarks</span></span>

<span data-ttu-id="3237e-145">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="3237e-145">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3237e-146">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="3237e-146">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="3237e-147">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="3237e-147">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3237e-148">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="3237e-148">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3237e-149">Требования</span><span class="sxs-lookup"><span data-stu-id="3237e-149">Requirements</span></span>



| <span data-ttu-id="3237e-150">Требование</span><span class="sxs-lookup"><span data-stu-id="3237e-150">Requirement</span></span> | <span data-ttu-id="3237e-151">Значение</span><span class="sxs-lookup"><span data-stu-id="3237e-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3237e-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3237e-152">Minimum supported client</span></span><br/> | <span data-ttu-id="3237e-153">Windows 7 Корпоративная, \[ только классические приложения Windows 7 Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="3237e-153">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3237e-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3237e-154">Minimum supported server</span></span><br/> | <span data-ttu-id="3237e-155">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3237e-155">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3237e-156">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3237e-156">Namespace</span></span><br/>                | <span data-ttu-id="3237e-157">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="3237e-157">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="3237e-158">MOF</span><span class="sxs-lookup"><span data-stu-id="3237e-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3237e-159"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3237e-159"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3237e-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3237e-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3237e-161">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="3237e-161">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
