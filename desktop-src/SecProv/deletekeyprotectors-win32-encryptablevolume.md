---
description: Удаляет все предохранители ключа для тома.
ms.assetid: 46f61899-87ff-4e86-8409-635117cff4de
title: Метод Делетекэйпротекторс класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0195a89884dcd9f9288cab020d9804dcc81b7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683477"
---
# <a name="deletekeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="c7d21-103">Метод Делетекэйпротекторс \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="c7d21-103">DeleteKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="c7d21-104">Метод **делетекэйпротекторс** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) удаляет все предохранители ключа для тома.</span><span class="sxs-lookup"><span data-stu-id="c7d21-104">The **DeleteKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class deletes all key protectors for the volume.</span></span>

<span data-ttu-id="c7d21-105">Если незашифрованный том содержит предохранители ключа, то при успешном выполнении **делетекэйпротекторс** том возвращается к стандартной файловой системе NTFS.</span><span class="sxs-lookup"><span data-stu-id="c7d21-105">If an unencrypted volume has key protectors, when **DeleteKeyProtectors** is run successfully the volume reverts to a standard NTFS file system.</span></span>

<span data-ttu-id="c7d21-106">Если том еще не полностью расшифрован, используйте [**дисаблекэйпротекторс**](disablekeyprotectors-win32-encryptablevolume.md) перед запуском **делетекэйпротекторс** , чтобы убедиться, что зашифрованные части тома остаются доступными.</span><span class="sxs-lookup"><span data-stu-id="c7d21-106">If the volume is not yet fully decrypted, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before running **DeleteKeyProtectors** to ensure that encrypted portions of the volume remain accessible.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7d21-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7d21-107">Syntax</span></span>


```mof
uint32 DeleteKeyProtectors();
```



## <a name="parameters"></a><span data-ttu-id="c7d21-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7d21-108">Parameters</span></span>

<span data-ttu-id="c7d21-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c7d21-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c7d21-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7d21-110">Return value</span></span>

<span data-ttu-id="c7d21-111">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7d21-111">Type: **uint32**</span></span>

<span data-ttu-id="c7d21-112">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="c7d21-112">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="c7d21-113">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="c7d21-113">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="c7d21-114">Описание</span><span class="sxs-lookup"><span data-stu-id="c7d21-114">Description</span></span>                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c7d21-115"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c7d21-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                          | <span data-ttu-id="c7d21-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="c7d21-116">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="c7d21-117"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="c7d21-117"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>         | <span data-ttu-id="c7d21-118">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="c7d21-118">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="c7d21-119"><dt>**ФВЕ \_ 2150694941 \_ \_ требуется ключ E**</dt> <dt>(0x8031001D)</dt></span><span class="sxs-lookup"><span data-stu-id="c7d21-119"><dt>**FVE\_E\_KEY\_REQUIRED**</dt> <dt>2150694941 (0x8031001D)</dt></span></span> </dl>          | <span data-ttu-id="c7d21-120">Последний предохранитель ключа для частично или полностью зашифрованного тома нельзя удалить, если включены предохранители ключа.</span><span class="sxs-lookup"><span data-stu-id="c7d21-120">The last key protector for a partially or fully encrypted volume cannot be removed if key protectors are enabled.</span></span> <span data-ttu-id="c7d21-121">Используйте [**дисаблекэйпротекторс**](disablekeyprotectors-win32-encryptablevolume.md) перед удалением последнего предохранителя ключа, чтобы убедиться, что зашифрованные части тома остаются доступными.</span><span class="sxs-lookup"><span data-stu-id="c7d21-121">Use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before removing this last key protector to ensure that encrypted portions of the volume remain accessible.</span></span> <br/> |
| <dl> <span data-ttu-id="c7d21-122"><dt>**ФВЕ \_ E \_ \_ с привязкой к тому \_ уже**</dt> <dt>2150694943 (0x8031001F)</dt></span><span class="sxs-lookup"><span data-stu-id="c7d21-122"><dt>**FVE\_E\_VOLUME\_BOUND\_ALREADY**</dt> <dt>2150694943 (0x8031001F)</dt></span></span> </dl> | <span data-ttu-id="c7d21-123">Невозможно удалить предохранители ключа, так как один из них используется для автоматической разблокировки тома.</span><span class="sxs-lookup"><span data-stu-id="c7d21-123">Key protectors cannot be deleted because one of them is being used to automatically unlock the volume.</span></span> <br/> <span data-ttu-id="c7d21-124">Используйте [**дисаблеаутаунлокк**](disableautounlock-win32-encryptablevolume.md) , чтобы отключить автоматическое снятие блокировки перед выполнением этого метода.</span><span class="sxs-lookup"><span data-stu-id="c7d21-124">Use [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) to disable automatic unlocking before running this method.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="c7d21-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7d21-125">Remarks</span></span>

<span data-ttu-id="c7d21-126">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="c7d21-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c7d21-127">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="c7d21-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="c7d21-128">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="c7d21-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c7d21-129">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="c7d21-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7d21-130">Требования</span><span class="sxs-lookup"><span data-stu-id="c7d21-130">Requirements</span></span>



| <span data-ttu-id="c7d21-131">Требование</span><span class="sxs-lookup"><span data-stu-id="c7d21-131">Requirement</span></span> | <span data-ttu-id="c7d21-132">Значение</span><span class="sxs-lookup"><span data-stu-id="c7d21-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7d21-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7d21-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c7d21-134">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="c7d21-134">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c7d21-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7d21-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c7d21-136">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c7d21-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c7d21-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c7d21-137">Namespace</span></span><br/>                | <span data-ttu-id="c7d21-138">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="c7d21-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="c7d21-139">MOF</span><span class="sxs-lookup"><span data-stu-id="c7d21-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7d21-140"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7d21-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7d21-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7d21-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7d21-142">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="c7d21-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
