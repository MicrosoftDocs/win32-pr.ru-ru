---
description: Позволяет автоматически разблокировать том данных при подключении тома.
ms.assetid: ec77b17f-545b-40a7-91b2-ff0b32b8370d
title: Метод Енаблеаутаунлокк класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 39456e9130081e52820cd91ba3e191ee40ab2374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910043"
---
# <a name="enableautounlock-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="3cb7d-103">Метод Енаблеаутаунлокк \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="3cb7d-103">EnableAutoUnlock method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="3cb7d-104">Метод **енаблеаутаунлокк** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) позволяет автоматически разблокировать том данных при подключении тома.</span><span class="sxs-lookup"><span data-stu-id="3cb7d-104">The **EnableAutoUnlock** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class allows a data volume to be automatically unlocked when the volume is mounted.</span></span>

<span data-ttu-id="3cb7d-105">Автоматическое снятие блокировки сохраняет внешний ключ в операционной системе, который может автоматически разблокировать том на текущем томе операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3cb7d-105">Automatic unlocking saves an external key to the operating system that can automatically unlock the volume onto the currently running operating system volume.</span></span>

<span data-ttu-id="3cb7d-106">Чтобы использовать этот метод, том операционной системы уже должен быть защищен шифрование диска BitLocker или должен выполняться шифрование.</span><span class="sxs-lookup"><span data-stu-id="3cb7d-106">To use this method, the operating system volume must already be protected by BitLocker Drive Encryption or must have encryption in progress.</span></span> <span data-ttu-id="3cb7d-107">Кроме того, уже должен существовать внешний ключ для тома данных.</span><span class="sxs-lookup"><span data-stu-id="3cb7d-107">In addition, there must already exist an external key for the data volume.</span></span> <span data-ttu-id="3cb7d-108">Используйте [**протекткэйвисекстерналкэй**](protectkeywithexternalkey-win32-encryptablevolume.md) для создания внешнего ключа, который может автоматически разблокировать том.</span><span class="sxs-lookup"><span data-stu-id="3cb7d-108">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) to create the external key that can automatically unlock the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cb7d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3cb7d-109">Syntax</span></span>


```mof
uint32 EnableAutoUnlock(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="3cb7d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="3cb7d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cb7d-111">*Волумекэйпротекторид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3cb7d-111">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cb7d-112">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="3cb7d-112">Type: **string**</span></span>

<span data-ttu-id="3cb7d-113">Строка, определяющая предохранитель ключа типа "внешний ключ", используемый для автоматического разблокировки тома.</span><span class="sxs-lookup"><span data-stu-id="3cb7d-113">A string that identifies the key protector of the type "External Key" used to automatically unlock the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cb7d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3cb7d-114">Return value</span></span>

<span data-ttu-id="3cb7d-115">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3cb7d-115">Type: **uint32**</span></span>

<span data-ttu-id="3cb7d-116">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="3cb7d-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="3cb7d-117">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="3cb7d-117">Return code/value</span></span>                                                                                                                                                                           | <span data-ttu-id="3cb7d-118">Описание</span><span class="sxs-lookup"><span data-stu-id="3cb7d-118">Description</span></span>                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3cb7d-119"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="3cb7d-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                           | <span data-ttu-id="3cb7d-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="3cb7d-120">The method was successful.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="3cb7d-121"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="3cb7d-121"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>          | <span data-ttu-id="3cb7d-122">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="3cb7d-122">The volume is locked.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="3cb7d-123"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="3cb7d-123"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>          | <span data-ttu-id="3cb7d-124">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="3cb7d-124">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="3cb7d-125">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3cb7d-125">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                 |
| <dl> <span data-ttu-id="3cb7d-126"><dt>**Д \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="3cb7d-126"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                   | <span data-ttu-id="3cb7d-127">Параметр *волумекэйпротекторид* не ссылается на допустимый предохранитель ключа типа "внешний ключ".</span><span class="sxs-lookup"><span data-stu-id="3cb7d-127">The *VolumeKeyProtectorID* parameter does not refer to a valid key protector of the type "External Key".</span></span><br/>                                                          |
| <dl> <span data-ttu-id="3cb7d-128"><dt>**ФВЕ \_ E \_ не \_ DATA \_ Volume**</dt> <dt>2150694937 (0x80310019)</dt></span><span class="sxs-lookup"><span data-stu-id="3cb7d-128"><dt>**FVE\_E\_NOT\_DATA\_VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span></span> </dl>       | <span data-ttu-id="3cb7d-129">Этот метод не может быть выполнен для текущего тома операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3cb7d-129">The method cannot be run for the currently running operating system volume.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="3cb7d-130"><dt>**ФВЕ \_ Электронная \_ система \_ не \_ защищена**</dt> <dt>2150694944 (0x80310020)</dt></span><span class="sxs-lookup"><span data-stu-id="3cb7d-130"><dt>**FVE\_E\_OS\_NOT\_PROTECTED**</dt> <dt>2150694944 (0x80310020)</dt></span></span> </dl>      | <span data-ttu-id="3cb7d-131">Метод не может быть выполнен, если запущенный в данный момент том операционной системы не защищен шифрование диска BitLocker или не выполняется шифрование.</span><span class="sxs-lookup"><span data-stu-id="3cb7d-131">The method cannot be run if the currently running operating system volume is not protected by BitLocker Drive Encryption or does not have encryption in progress.</span></span><br/> |
| <dl> <span data-ttu-id="3cb7d-132"><dt> **ФВЕ \_ E \_ \_ с привязкой к тому \_ уже**</dt> <dt>2150694943 (0x8031001F)</dt></span><span class="sxs-lookup"><span data-stu-id="3cb7d-132"><dt>**FVE\_E\_VOLUME\_BOUND\_ALREADY** </dt> <dt>2150694943 (0x8031001F)</dt></span></span> </dl> | <span data-ttu-id="3cb7d-133">Автоматическое снятие блокировки тома включено ранее.</span><span class="sxs-lookup"><span data-stu-id="3cb7d-133">Automatic unlocking on the volume has previously been enabled.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="3cb7d-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3cb7d-134">Remarks</span></span>

<span data-ttu-id="3cb7d-135">При наличии допустимого предохранителя ключа тома типа "внешний ключ" связанный 256-разрядный внешний ключ извлекается из предохранителя и сохраняется в реестре выполняющейся операционной системы вместе с ИДЕНТИФИКАТОРом предохранителя ключа тома.</span><span class="sxs-lookup"><span data-stu-id="3cb7d-135">Given a valid volume key protector of the type "External Key", the related 256-bit external key is extracted from the protector and stored into the registry of the currently running operating system, along with the volume key protector ID.</span></span>

<span data-ttu-id="3cb7d-136">Если внешний ключ, связанный с ИДЕНТИФИКАТОРом предохранителя ключа тома, удаляется, функции автоматического разблокировки тома отключаются или приостанавливаются.</span><span class="sxs-lookup"><span data-stu-id="3cb7d-136">If the external key associated with the volume key protector ID is deleted, the functionality to automatically unlock the volume is disabled or suspended.</span></span>

> [!Note]  
> <span data-ttu-id="3cb7d-137">Съемные носители в настоящее время не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="3cb7d-137">Removable media is not currently supported.</span></span>

 

<span data-ttu-id="3cb7d-138">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="3cb7d-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3cb7d-139">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="3cb7d-139">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="3cb7d-140">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="3cb7d-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3cb7d-141">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="3cb7d-141">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3cb7d-142">Требования</span><span class="sxs-lookup"><span data-stu-id="3cb7d-142">Requirements</span></span>



| <span data-ttu-id="3cb7d-143">Требование</span><span class="sxs-lookup"><span data-stu-id="3cb7d-143">Requirement</span></span> | <span data-ttu-id="3cb7d-144">Значение</span><span class="sxs-lookup"><span data-stu-id="3cb7d-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cb7d-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3cb7d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="3cb7d-146">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="3cb7d-146">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3cb7d-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3cb7d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="3cb7d-148">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3cb7d-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3cb7d-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3cb7d-149">Namespace</span></span><br/>                | <span data-ttu-id="3cb7d-150">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="3cb7d-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="3cb7d-151">MOF</span><span class="sxs-lookup"><span data-stu-id="3cb7d-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3cb7d-152"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3cb7d-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cb7d-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3cb7d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cb7d-154">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="3cb7d-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
