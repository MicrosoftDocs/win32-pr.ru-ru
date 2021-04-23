---
description: Удаляет данный предохранитель ключа для тома.
ms.assetid: fa6b89b0-83b6-4be2-8b7b-61b0501747d2
title: Метод Делетекэйпротектор класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtector
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b1f539683bb76559d08066d01de6aeca0394ced3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343075"
---
# <a name="deletekeyprotector-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="7be29-103">Метод Делетекэйпротектор \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="7be29-103">DeleteKeyProtector method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="7be29-104">Метод **делетекэйпротектор** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) Удаляет данный предохранитель ключа для тома.</span><span class="sxs-lookup"><span data-stu-id="7be29-104">The **DeleteKeyProtector** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class deletes a given key protector for the volume.</span></span>

<span data-ttu-id="7be29-105">Если в незашифрованном томе есть предохранители ключа, то когда **делетекэйпротектор** удаляет последний предохранитель ключа, том возвращается к стандартной файловой системе NTFS.</span><span class="sxs-lookup"><span data-stu-id="7be29-105">If an unencrypted volume has key protectors, when **DeleteKeyProtector** removes the last key protector, the volume reverts to a standard NTFS file system.</span></span>

<span data-ttu-id="7be29-106">Если том не был зашифрован, Удаление предохранителя ключа приведет к восстановлению файловой системы NTFS.</span><span class="sxs-lookup"><span data-stu-id="7be29-106">If a volume has never been encrypted, deleting the key protector will revert to NTFS.</span></span>

<span data-ttu-id="7be29-107">Если том еще не полностью расшифрован, используйте [**дисаблекэйпротекторс**](disablekeyprotectors-win32-encryptablevolume.md) перед удалением предохранителя последнего ключа тома, чтобы убедиться, что зашифрованные части тома остаются доступными.</span><span class="sxs-lookup"><span data-stu-id="7be29-107">If the volume is not yet fully decrypted, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before removing the volume's last key protector to ensure that encrypted portions of the volume remain accessible.</span></span>

## <a name="syntax"></a><span data-ttu-id="7be29-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7be29-108">Syntax</span></span>


```mof
uint32 DeleteKeyProtector(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="7be29-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7be29-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7be29-110">*Волумекэйпротекторид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7be29-110">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7be29-111">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="7be29-111">Type: **string**</span></span>

<span data-ttu-id="7be29-112">Уникальный строковый идентификатор, используемый для управления предохранителем ключа зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="7be29-112">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7be29-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7be29-113">Return value</span></span>

<span data-ttu-id="7be29-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7be29-114">Type: **uint32**</span></span>

<span data-ttu-id="7be29-115">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="7be29-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="7be29-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="7be29-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="7be29-117">Описание</span><span class="sxs-lookup"><span data-stu-id="7be29-117">Description</span></span>                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7be29-118"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="7be29-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                          | <span data-ttu-id="7be29-119">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="7be29-119">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="7be29-120"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="7be29-120"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>         | <span data-ttu-id="7be29-121">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="7be29-121">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="7be29-122"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="7be29-122"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>         | <span data-ttu-id="7be29-123">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="7be29-123">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="7be29-124">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7be29-124">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="7be29-125"><dt>**Д \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="7be29-125"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                  | <span data-ttu-id="7be29-126">Параметр *волумекэйпротекторид* не ссылается на допустимый предохранитель ключа.</span><span class="sxs-lookup"><span data-stu-id="7be29-126">The *VolumeKeyProtectorID* parameter does not refer to a valid key protector.</span></span><br/>                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="7be29-127"><dt>**ФВЕ \_ 2150694941 \_ \_ требуется ключ E**</dt> <dt>(0x8031001D)</dt></span><span class="sxs-lookup"><span data-stu-id="7be29-127"><dt>**FVE\_E\_KEY\_REQUIRED**</dt> <dt>2150694941 (0x8031001D)</dt></span></span> </dl>          | <span data-ttu-id="7be29-128">Последний предохранитель ключа для частично или полностью зашифрованного тома нельзя удалить, если включены предохранители ключа.</span><span class="sxs-lookup"><span data-stu-id="7be29-128">The last key protector for a partially or fully encrypted volume cannot be removed if key protectors are enabled.</span></span> <span data-ttu-id="7be29-129">Используйте [**дисаблекэйпротекторс**](disablekeyprotectors-win32-encryptablevolume.md) перед удалением последнего предохранителя ключа, чтобы убедиться, что зашифрованные части тома остаются доступными.</span><span class="sxs-lookup"><span data-stu-id="7be29-129">Use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before removing this last key protector to ensure that encrypted portions of the volume remain accessible.</span></span> <br/> |
| <dl> <span data-ttu-id="7be29-130"><dt>**ФВЕ \_ E \_ \_ с привязкой к тому \_ уже**</dt> <dt>2150694943 (0x8031001F)</dt></span><span class="sxs-lookup"><span data-stu-id="7be29-130"><dt>**FVE\_E\_VOLUME\_BOUND\_ALREADY**</dt> <dt>2150694943 (0x8031001F)</dt></span></span> </dl> | <span data-ttu-id="7be29-131">Невозможно удалить этот предохранитель ключа, так как он используется для автоматической разблокировки тома.</span><span class="sxs-lookup"><span data-stu-id="7be29-131">This key protector cannot be deleted because it is being used to automatically unlock the volume.</span></span> <br/> <span data-ttu-id="7be29-132">Используйте [**дисаблеаутаунлокк**](disableautounlock-win32-encryptablevolume.md) , чтобы отключить автоматическое снятие блокировки перед удалением предохранителя ключа.</span><span class="sxs-lookup"><span data-stu-id="7be29-132">Use [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) to disable automatic unlocking before deleting this key protector.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="7be29-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7be29-133">Remarks</span></span>

<span data-ttu-id="7be29-134">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="7be29-134">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7be29-135">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7be29-135">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7be29-136">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="7be29-136">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7be29-137">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="7be29-137">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7be29-138">Требования</span><span class="sxs-lookup"><span data-stu-id="7be29-138">Requirements</span></span>



| <span data-ttu-id="7be29-139">Требование</span><span class="sxs-lookup"><span data-stu-id="7be29-139">Requirement</span></span> | <span data-ttu-id="7be29-140">Значение</span><span class="sxs-lookup"><span data-stu-id="7be29-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7be29-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7be29-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7be29-142">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="7be29-142">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7be29-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7be29-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7be29-144">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7be29-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7be29-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7be29-145">Namespace</span></span><br/>                | <span data-ttu-id="7be29-146">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="7be29-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="7be29-147">MOF</span><span class="sxs-lookup"><span data-stu-id="7be29-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7be29-148"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7be29-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7be29-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7be29-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7be29-150">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="7be29-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
