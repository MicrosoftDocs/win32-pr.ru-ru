---
description: Использует новую парольную фразу для получения нового производного ключа.
ms.assetid: 89398bae-a2a2-466c-8a1e-a702018d679f
title: Метод Чанжепассфрасе класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f28a78c6cb923b4f8934ec5cc8962b91b7f5139f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684075"
---
# <a name="changepassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="0284f-103">Метод Чанжепассфрасе \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="0284f-103">ChangePassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="0284f-104">Метод **чанжепассфрасе** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) использует новую парольную фразу для получения нового производного ключа.</span><span class="sxs-lookup"><span data-stu-id="0284f-104">The **ChangePassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the new passphrase to obtain a new derived key.</span></span> <span data-ttu-id="0284f-105">После вычисления производного ключа новый производный ключ используется для защиты главного ключа зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="0284f-105">After the derived key is calculated, the new derived key is used to secure the encrypted volume's master key.</span></span>

## <a name="syntax"></a><span data-ttu-id="0284f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0284f-106">Syntax</span></span>


```mof
uint32 ChangePassphrase(
  [in]  string VolumeKeyProtectorID,
  [in]  string NewPassphrase,
  [out] string NewProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="0284f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0284f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0284f-108">*Волумекэйпротекторид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0284f-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0284f-109">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="0284f-109">Type: **string**</span></span>

<span data-ttu-id="0284f-110">Уникальный строковый идентификатор, используемый для управления предохранителем ключа зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="0284f-110">A unique string identifier that is used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="0284f-111">*Невпассфрасе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0284f-111">*NewPassphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0284f-112">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="0284f-112">Type: **string**</span></span>

<span data-ttu-id="0284f-113">Обновленная строка, указывающая парольную фразу.</span><span class="sxs-lookup"><span data-stu-id="0284f-113">An updated string that specifies the passphrase.</span></span>

</dd> <dt>

<span data-ttu-id="0284f-114">*Невпротекторид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0284f-114">*NewProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0284f-115">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="0284f-115">Type: **string**</span></span>

<span data-ttu-id="0284f-116">Обновленный уникальный идентификатор строки, используемый для управления предохранителем ключа зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="0284f-116">An updated unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0284f-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0284f-117">Return value</span></span>

<span data-ttu-id="0284f-118">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0284f-118">Type: **uint32**</span></span>

<span data-ttu-id="0284f-119">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="0284f-119">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="0284f-120">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="0284f-120">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="0284f-121">Описание</span><span class="sxs-lookup"><span data-stu-id="0284f-121">Description</span></span>                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0284f-122"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0284f-122"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="0284f-123">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="0284f-123">The method was successful.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="0284f-124"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="0284f-124"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                      | <span data-ttu-id="0284f-125">Том уже заблокирован шифрование диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0284f-125">The volume is already locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="0284f-126">Необходимо разблокировать диск с помощью панели управления.</span><span class="sxs-lookup"><span data-stu-id="0284f-126">You must unlock the drive from Control Panel.</span></span><br/>   |
| <dl> <span data-ttu-id="0284f-127"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="0284f-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="0284f-128">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="0284f-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="0284f-129">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0284f-129">Add a key protector to enable BitLocker.</span></span> <br/>                           |
| <dl> <span data-ttu-id="0284f-130"><dt>**ФВЕ \_ \_ПЕРЕкрытое \_ Обновление**</dt> <dt>2150694948 (0x80310024)</dt></span><span class="sxs-lookup"><span data-stu-id="0284f-130"><dt>**FVE\_E\_OVERLAPPED\_UPDATE**</dt> <dt>2150694948 (0x80310024)</dt></span></span> </dl>                  | <span data-ttu-id="0284f-131">Блок управления для зашифрованного тома обновлен другим потоком.</span><span class="sxs-lookup"><span data-stu-id="0284f-131">The control block for the encrypted volume was updated by another thread.</span></span><br/>                                   |
| <dl> <span data-ttu-id="0284f-132"><dt>**ФВЕ \_ \_Недопустимый \_ \_ тип предохранителя**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="0284f-132"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl>            | <span data-ttu-id="0284f-133">Указанный предохранитель ключа имеет неправильный тип.</span><span class="sxs-lookup"><span data-stu-id="0284f-133">The specified key protector is not of the correct type.</span></span> <br/>                                                    |
| <dl> <span data-ttu-id="0284f-134"><dt>**ФВЕ \_ E \_ Policy \_ Недопустимая \_ \_ Длина парольной фразы**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="0284f-134"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl> | <span data-ttu-id="0284f-135">Обновленная парольная фраза не соответствует требованиям к минимальной или максимальной длине.</span><span class="sxs-lookup"><span data-stu-id="0284f-135">The updated passphrase provided does not meet the minimum or maximum length requirements.</span></span> <br/>                  |
| <dl> <span data-ttu-id="0284f-136"><dt>**ФВЕ \_ \_ \_ \_ Слишком \_ простая парольная фраза для политики**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="0284f-136"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>     | <span data-ttu-id="0284f-137">Обновленная парольная фраза не соответствует требованиям сложности, заданным администратором в групповой политике.</span><span class="sxs-lookup"><span data-stu-id="0284f-137">The updated passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="0284f-138">Требования</span><span class="sxs-lookup"><span data-stu-id="0284f-138">Requirements</span></span>



| <span data-ttu-id="0284f-139">Требование</span><span class="sxs-lookup"><span data-stu-id="0284f-139">Requirement</span></span> | <span data-ttu-id="0284f-140">Значение</span><span class="sxs-lookup"><span data-stu-id="0284f-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0284f-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0284f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="0284f-142">Windows 7 Корпоративная, \[ только классические приложения Windows 7 Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="0284f-142">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0284f-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0284f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="0284f-144">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0284f-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0284f-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0284f-145">Namespace</span></span><br/>                | <span data-ttu-id="0284f-146">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="0284f-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="0284f-147">MOF</span><span class="sxs-lookup"><span data-stu-id="0284f-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0284f-148"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0284f-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0284f-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0284f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0284f-150">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="0284f-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




