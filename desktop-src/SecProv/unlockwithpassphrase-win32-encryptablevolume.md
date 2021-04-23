---
description: Использует парольную фразу для получения производного ключа.
ms.assetid: 09b4ae7f-7084-42bd-8bbe-da686d6280e9
title: Метод Унлокквиспассфрасе класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 75c5522a0781b1cd229bf97d2549433a426fbfc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664374"
---
# <a name="unlockwithpassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f4e8e-103">Метод Унлокквиспассфрасе \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="f4e8e-103">UnlockWithPassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f4e8e-104">Метод **унлокквиспассфрасе** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) использует парольную фразу для получения производного ключа.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-104">The **UnlockWithPassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the passphrase to obtain the derived key.</span></span> <span data-ttu-id="f4e8e-105">После вычисления производного ключа используется производный ключ для разблокировки главного ключа зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-105">After the derived key is calculated, the derived key is used to unlock the encrypted volume's master key.</span></span>

> [!Note]  
> <span data-ttu-id="f4e8e-106">Если диск поддерживает аппаратное шифрование, эта функция устанавливает для полосы состояние "разблокирован".</span><span class="sxs-lookup"><span data-stu-id="f4e8e-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f4e8e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4e8e-107">Syntax</span></span>


```mof
uint32 UnlockWithPassphrase(
  [in] string Passphrase
);
```



## <a name="parameters"></a><span data-ttu-id="f4e8e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4e8e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4e8e-109">*Парольная фраза* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f4e8e-109">*Passphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4e8e-110">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="f4e8e-110">Type: **string**</span></span>

<span data-ttu-id="f4e8e-111">Строка, указывающая парольную фразу.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-111">A string that specifies the passphrase.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4e8e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f4e8e-112">Return value</span></span>

<span data-ttu-id="f4e8e-113">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4e8e-113">Type: **uint32**</span></span>

<span data-ttu-id="f4e8e-114">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-114">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="f4e8e-115">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="f4e8e-115">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="f4e8e-116">Описание</span><span class="sxs-lookup"><span data-stu-id="f4e8e-116">Description</span></span>                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f4e8e-117"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f4e8e-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="f4e8e-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-118">The method was successful.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="f4e8e-119"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="f4e8e-119"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="f4e8e-120">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-120">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="f4e8e-121">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-121">Add a key protector to enable BitLocker.</span></span> <br/>                              |
| <dl> <span data-ttu-id="f4e8e-122"><dt>**ФВЕ \_ E \_ FIPS \_ не защищает \_ парольную фразу**</dt> <dt>2150695020 (0x8031006C)</dt></span><span class="sxs-lookup"><span data-stu-id="f4e8e-122"><dt>**FVE\_E\_FIPS\_PREVENTS\_PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt></span></span> </dl>          | <span data-ttu-id="f4e8e-123">Параметр групповой политики, требующий соответствия FIPS, не позволил создать или использовать парольную фразу.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-123">The group policy setting that requires FIPS compliance prevented the passphrase from being generated or used.</span></span> <br/> |
| <dl> <span data-ttu-id="f4e8e-124"><dt>**ФВЕ \_ E \_ Policy \_ Недопустимая \_ \_ Длина парольной фразы**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="f4e8e-124"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl> | <span data-ttu-id="f4e8e-125">Указанная парольная фраза не соответствует требованиям к минимальной или максимальной длине.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-125">The passphrase provided does not meet the minimum or maximum length requirements.</span></span><br/>                              |
| <dl> <span data-ttu-id="f4e8e-126"><dt>**ФВЕ \_ \_ \_ \_ Слишком \_ простая парольная фраза для политики**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="f4e8e-126"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>     | <span data-ttu-id="f4e8e-127">Парольная фраза не соответствует требованиям сложности, заданным администратором в групповой политике.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-127">The passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span><br/>             |
| <dl> <span data-ttu-id="f4e8e-128"><dt>**ФВЕ \_ E \_ Failed \_ authentication**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="f4e8e-128"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>              | <span data-ttu-id="f4e8e-129">Не удается разблокировать том с помощью предоставленных сведений.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-129">The volume cannot be unlocked with the provided information.</span></span> <br/>                                                  |
| <dl> <span data-ttu-id="f4e8e-130"><dt>**ФВЕ \_ \_ \_ Не \_ найден предохранитель "E**</dt> <dt>" 2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="f4e8e-130"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>               | <span data-ttu-id="f4e8e-131">Указанный предохранитель ключа не существует на томе.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-131">The provided key protector does not exist on the volume.</span></span> <span data-ttu-id="f4e8e-132">Необходимо ввести другой предохранитель ключа.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-132">You must enter another key protector.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="f4e8e-133">Требования</span><span class="sxs-lookup"><span data-stu-id="f4e8e-133">Requirements</span></span>



| <span data-ttu-id="f4e8e-134">Требование</span><span class="sxs-lookup"><span data-stu-id="f4e8e-134">Requirement</span></span> | <span data-ttu-id="f4e8e-135">Значение</span><span class="sxs-lookup"><span data-stu-id="f4e8e-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4e8e-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f4e8e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f4e8e-137">Windows 7 Корпоративная, \[ только классические приложения Windows 7 Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="f4e8e-137">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f4e8e-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f4e8e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f4e8e-139">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f4e8e-139">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f4e8e-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f4e8e-140">Namespace</span></span><br/>                | <span data-ttu-id="f4e8e-141">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="f4e8e-141">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f4e8e-142">MOF</span><span class="sxs-lookup"><span data-stu-id="f4e8e-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4e8e-143"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4e8e-143"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4e8e-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4e8e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4e8e-145">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="f4e8e-145">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




