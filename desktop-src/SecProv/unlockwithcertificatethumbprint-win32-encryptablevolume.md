---
description: Использует предоставленный отпечаток сертификата для получения производного ключа и разблокировки зашифрованного тома.
ms.assetid: 41c25d17-db1b-427e-907b-a547483927e0
title: Метод Унлокквисцертификатесумбпринт класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 5955334b6c147feea43d5e0a2c83a8e00050d900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809269"
---
# <a name="unlockwithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="58e95-103">Метод Унлокквисцертификатесумбпринт \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="58e95-103">UnlockWithCertificateThumbprint method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="58e95-104">Метод **унлокквисцертификатесумбпринт** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) использует предоставленный отпечаток [*сертификата*](../secgloss/c-gly.md) для получения производного ключа и разблокировки зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="58e95-104">The **UnlockWithCertificateThumbprint** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the provided [*certificate*](../secgloss/c-gly.md) thumbprint to obtain the derived key and unlock the encrypted volume.</span></span>

> [!Note]  
> <span data-ttu-id="58e95-105">Если диск поддерживает аппаратное шифрование, эта функция устанавливает для полосы состояние "разблокирован".</span><span class="sxs-lookup"><span data-stu-id="58e95-105">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="58e95-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58e95-106">Syntax</span></span>


```mof
uint32 UnlockWithCertificateThumbprint(
  [in] string CertThumbprint,
  [in] string PIN
);
```



## <a name="parameters"></a><span data-ttu-id="58e95-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="58e95-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58e95-108">*CertThumbprint* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="58e95-108">*CertThumbprint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58e95-109">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="58e95-109">Type: **string**</span></span>

<span data-ttu-id="58e95-110">Значение отпечатка, равное 0, принимается, и в нем задается поиск соответствующего сертификата в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="58e95-110">A thumbprint value of 0 is accepted and results in a search of the local store for the appropriate certificate.</span></span> <span data-ttu-id="58e95-111">При обнаружении одного сертификата BitLocker Поиск будет успешным.</span><span class="sxs-lookup"><span data-stu-id="58e95-111">If a single BitLocker certificate is found, the search is successful.</span></span> <span data-ttu-id="58e95-112">Если не найдено ни одного сертификата, метод завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="58e95-112">If none or more than one certificate is found, the method fails.</span></span>

</dd> <dt>

<span data-ttu-id="58e95-113">*Закрепить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="58e95-113">*PIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58e95-114">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="58e95-114">Type: **string**</span></span>

<span data-ttu-id="58e95-115">Указанная пользователем личная строка идентификации.</span><span class="sxs-lookup"><span data-stu-id="58e95-115">A user-specified personal identification string.</span></span> <span data-ttu-id="58e95-116">Эта строка должна состоять из последовательности из 4 до 20 цифр.</span><span class="sxs-lookup"><span data-stu-id="58e95-116">This string must consist of a sequence of 4 to 20 digits.</span></span> <span data-ttu-id="58e95-117">Эта строка используется для автоматической проверки подлинности [*поставщика хранилища ключей*](../secgloss/k-gly.md) (KSP) при использовании со [*смарт-картой*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="58e95-117">This string is used to silently authenticate the [*key storage provider*](../secgloss/k-gly.md) (KSP) when used with a [*smart card*](../secgloss/s-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58e95-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="58e95-118">Return value</span></span>

<span data-ttu-id="58e95-119">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="58e95-119">Type: **uint32**</span></span>

<span data-ttu-id="58e95-120">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="58e95-120">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="58e95-121">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="58e95-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="58e95-122">Описание</span><span class="sxs-lookup"><span data-stu-id="58e95-122">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="58e95-123"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="58e95-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="58e95-124">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="58e95-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="58e95-125"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="58e95-125"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="58e95-126">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="58e95-126">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="58e95-127">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="58e95-127">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="58e95-128"><dt>**ФВЕ \_ E \_ Failed \_ authentication**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="58e95-128"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>   | <span data-ttu-id="58e95-129">Невозможно разблокировать том, используя предоставленные сведения.</span><span class="sxs-lookup"><span data-stu-id="58e95-129">The volume cannot be unlocked by using the provided information.</span></span> <br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="58e95-130"><dt>**ФВЕ \_ \_ \_ Не \_ найден предохранитель "E**</dt> <dt>" 2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="58e95-130"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="58e95-131">Указанный предохранитель ключа не существует на томе.</span><span class="sxs-lookup"><span data-stu-id="58e95-131">The provided key protector does not exist on the volume.</span></span> <span data-ttu-id="58e95-132">Необходимо ввести другой предохранитель ключа.</span><span class="sxs-lookup"><span data-stu-id="58e95-132">You must enter another key protector.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="58e95-133"><dt>**ФВЕ \_ E \_ PRIVATEKEY \_ AUTH \_ Failed**</dt> <dt>2150695060 (0x80310094)</dt></span><span class="sxs-lookup"><span data-stu-id="58e95-133"><dt>**FVE\_E\_PRIVATEKEY\_AUTH\_FAILED**</dt> <dt>2150695060 (0x80310094)</dt></span></span> </dl> | <span data-ttu-id="58e95-134">Не удалось авторизовать [*закрытый ключ*](../secgloss/p-gly.md) , связанный с указанным сертификатом.</span><span class="sxs-lookup"><span data-stu-id="58e95-134">The [*private key*](../secgloss/p-gly.md) associated with the specified certificate could not be authorized.</span></span> <span data-ttu-id="58e95-135">Не указана авторизация закрытого ключа, или предоставлена недопустимая авторизация.</span><span class="sxs-lookup"><span data-stu-id="58e95-135">The private key authorization was either not provided or the provided authorization was not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="58e95-136">Требования</span><span class="sxs-lookup"><span data-stu-id="58e95-136">Requirements</span></span>



| <span data-ttu-id="58e95-137">Требование</span><span class="sxs-lookup"><span data-stu-id="58e95-137">Requirement</span></span> | <span data-ttu-id="58e95-138">Значение</span><span class="sxs-lookup"><span data-stu-id="58e95-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58e95-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="58e95-139">Minimum supported client</span></span><br/> | <span data-ttu-id="58e95-140">Windows 7 Корпоративная, \[ только классические приложения Windows 7 Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="58e95-140">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="58e95-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="58e95-141">Minimum supported server</span></span><br/> | <span data-ttu-id="58e95-142">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="58e95-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="58e95-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="58e95-143">Namespace</span></span><br/>                | <span data-ttu-id="58e95-144">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="58e95-144">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="58e95-145">MOF</span><span class="sxs-lookup"><span data-stu-id="58e95-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58e95-146"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58e95-146"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58e95-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58e95-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58e95-148">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="58e95-148">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
