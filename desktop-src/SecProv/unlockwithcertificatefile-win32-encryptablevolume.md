---
description: Использует предоставленный файл сертификата для получения производного ключа и разблокировки зашифрованного тома.
ms.assetid: 41811d38-5c89-4372-9dbc-3de45b05011f
title: Метод Унлокквисцертификатефиле класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d7ce1705c0ec457f64eb825e49334e76a14c184c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664378"
---
# <a name="unlockwithcertificatefile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="e51cf-103">Метод Унлокквисцертификатефиле \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="e51cf-103">UnlockWithCertificateFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="e51cf-104">Метод **унлокквисцертификатефиле** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) использует предоставленный файл [*сертификата*](../secgloss/c-gly.md) для получения производного ключа и разблокировки зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="e51cf-104">The **UnlockWithCertificateFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the provided [*certificate*](../secgloss/c-gly.md) file to obtain the derived key and unlock the encrypted volume.</span></span>

> [!Note]  
> <span data-ttu-id="e51cf-105">Если диск поддерживает аппаратное шифрование, эта функция устанавливает для полосы состояние "разблокирован".</span><span class="sxs-lookup"><span data-stu-id="e51cf-105">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e51cf-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e51cf-106">Syntax</span></span>


```mof
uint32 UnlockWithCertificateFile(
  [in] string FileName,
  [in] string PIN
);
```



## <a name="parameters"></a><span data-ttu-id="e51cf-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e51cf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e51cf-108">*Имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e51cf-108">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e51cf-109">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="e51cf-109">Type: **string**</span></span>

<span data-ttu-id="e51cf-110">Строка, указывающая расположение и имя CER-файла, используемого для получения отпечатка сертификата.</span><span class="sxs-lookup"><span data-stu-id="e51cf-110">A string that specifies the location and name of the .cer file used to retrieve the certificate thumbprint.</span></span> <span data-ttu-id="e51cf-111">Сертификат [*шифрования*](../secgloss/e-gly.md) должен быть экспортирован в формате cer ([*distinguished Encoding Rules*](../secgloss/d-gly.md) (Der) Binary [*x. 509*](../secgloss/x-gly.md) или Base-64 Encoded x. 509).</span><span class="sxs-lookup"><span data-stu-id="e51cf-111">An [*encryption*](../secgloss/e-gly.md) certificate must be exported in .cer format ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER)-encoded binary [*X.509*](../secgloss/x-gly.md) or Base-64 encoded X.509).</span></span> <span data-ttu-id="e51cf-112">Сертификат шифрования может быть создан из PKI Майкрософт, стороннего PKI или самозаверяющего.</span><span class="sxs-lookup"><span data-stu-id="e51cf-112">The encryption certificate may be generated from Microsoft PKI, third-party PKI, or self-signed.</span></span>

</dd> <dt>

<span data-ttu-id="e51cf-113">*Закрепить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e51cf-113">*PIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e51cf-114">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="e51cf-114">Type: **string**</span></span>

<span data-ttu-id="e51cf-115">Указанная пользователем личная строка идентификации.</span><span class="sxs-lookup"><span data-stu-id="e51cf-115">A user-specified personal identification string.</span></span> <span data-ttu-id="e51cf-116">Эта строка должна состоять из последовательности из 4 до 20 цифр.</span><span class="sxs-lookup"><span data-stu-id="e51cf-116">This string must consist of a sequence of 4 to 20 digits.</span></span> <span data-ttu-id="e51cf-117">Эта строка используется для автоматической проверки подлинности [*поставщика хранилища ключей*](../secgloss/k-gly.md) (KSP) при использовании со [*смарт-картой*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e51cf-117">This string is used to silently authenticate the [*key storage provider*](../secgloss/k-gly.md) (KSP) when used with a [*smart card*](../secgloss/s-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e51cf-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e51cf-118">Return value</span></span>

<span data-ttu-id="e51cf-119">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e51cf-119">Type: **uint32**</span></span>

<span data-ttu-id="e51cf-120">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="e51cf-120">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="e51cf-121">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="e51cf-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="e51cf-122">Описание</span><span class="sxs-lookup"><span data-stu-id="e51cf-122">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e51cf-123"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="e51cf-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="e51cf-124">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="e51cf-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="e51cf-125"><dt>**Ошибка при \_ ФАЙЛ \_ не \_ найден**</dt> <dt>0000000002 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="e51cf-125"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt> <dt>0000000002 (0x2)</dt></span></span> </dl>                 | <span data-ttu-id="e51cf-126">Системе не удается выполнить файл для указанного файла.</span><span class="sxs-lookup"><span data-stu-id="e51cf-126">The system cannot file the specified file.</span></span><br/>                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="e51cf-127"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="e51cf-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="e51cf-128">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="e51cf-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="e51cf-129">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e51cf-129">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="e51cf-130"><dt>**ФВЕ \_ E \_ Failed \_ authentication**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="e51cf-130"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>   | <span data-ttu-id="e51cf-131">Не удается разблокировать том с помощью предоставленных сведений.</span><span class="sxs-lookup"><span data-stu-id="e51cf-131">The volume cannot be unlocked with the provided information.</span></span> <br/>                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="e51cf-132"><dt>**ФВЕ \_ \_ \_ Не \_ найден предохранитель "E**</dt> <dt>" 2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="e51cf-132"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="e51cf-133">Указанный предохранитель ключа не существует на томе.</span><span class="sxs-lookup"><span data-stu-id="e51cf-133">The provided key protector does not exist on the volume.</span></span> <span data-ttu-id="e51cf-134">Необходимо ввести другой предохранитель ключа.</span><span class="sxs-lookup"><span data-stu-id="e51cf-134">You must enter another key protector.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="e51cf-135"><dt>**ФВЕ \_ E \_ PRIVATEKEY \_ AUTH \_ Failed**</dt> <dt>2150695060 (0x80310094)</dt></span><span class="sxs-lookup"><span data-stu-id="e51cf-135"><dt>**FVE\_E\_PRIVATEKEY\_AUTH\_FAILED**</dt> <dt>2150695060 (0x80310094)</dt></span></span> </dl> | <span data-ttu-id="e51cf-136">Не удалось авторизовать [*закрытый ключ*](../secgloss/p-gly.md), связанный с указанным сертификатом.</span><span class="sxs-lookup"><span data-stu-id="e51cf-136">The [*private key*](../secgloss/p-gly.md), associated with the specified certificate, could not be authorized.</span></span> <span data-ttu-id="e51cf-137">Не указана авторизация закрытого ключа, или предоставлена недопустимая авторизация.</span><span class="sxs-lookup"><span data-stu-id="e51cf-137">The private key authorization was either not provided or the provided authorization was invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e51cf-138">Требования</span><span class="sxs-lookup"><span data-stu-id="e51cf-138">Requirements</span></span>



| <span data-ttu-id="e51cf-139">Требование</span><span class="sxs-lookup"><span data-stu-id="e51cf-139">Requirement</span></span> | <span data-ttu-id="e51cf-140">Значение</span><span class="sxs-lookup"><span data-stu-id="e51cf-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e51cf-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e51cf-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e51cf-142">Windows 7 Корпоративная, \[ только классические приложения Windows 7 Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="e51cf-142">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e51cf-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e51cf-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e51cf-144">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e51cf-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e51cf-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e51cf-145">Namespace</span></span><br/>                | <span data-ttu-id="e51cf-146">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="e51cf-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="e51cf-147">MOF</span><span class="sxs-lookup"><span data-stu-id="e51cf-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e51cf-148"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e51cf-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e51cf-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e51cf-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e51cf-150">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="e51cf-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
