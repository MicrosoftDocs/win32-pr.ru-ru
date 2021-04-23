---
description: Указывает, доступны ли содержимое тома из Windows.
ms.assetid: 54b2a41b-11c6-40ec-97fa-74996c15554e
title: Метод Жетлоккстатус класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetLockStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3e81f77c37904f26e87f22b8e2b3b88763fe86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682554"
---
# <a name="getlockstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="8ffa2-103">Метод Жетлоккстатус \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="8ffa2-103">GetLockStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="8ffa2-104">Метод **жетлоккстатус** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) указывает, доступно ли содержимое тома из Windows.</span><span class="sxs-lookup"><span data-stu-id="8ffa2-104">The **GetLockStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the contents of the volume are accessible from Windows.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ffa2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ffa2-105">Syntax</span></span>


```mof
uint32 GetLockStatus(
  [out] uint32 LockStatus
);
```



## <a name="parameters"></a><span data-ttu-id="8ffa2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ffa2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ffa2-107">*Локкстатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8ffa2-107">*LockStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffa2-108">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8ffa2-108">Type: **uint32**</span></span>

<span data-ttu-id="8ffa2-109">Указывает, доступны ли содержимое тома в Windows.</span><span class="sxs-lookup"><span data-stu-id="8ffa2-109">Specifies whether the contents of the volume are accessible from Windows.</span></span>



| <span data-ttu-id="8ffa2-110">Значение</span><span class="sxs-lookup"><span data-stu-id="8ffa2-110">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="8ffa2-111">Значение</span><span class="sxs-lookup"><span data-stu-id="8ffa2-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unlocked"></span><span id="unlocked"></span><span id="UNLOCKED"></span><dl> <span data-ttu-id="8ffa2-112"><dt>**Разблокировано**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8ffa2-112"><dt>**Unlocked**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="8ffa2-113">Для стандартного жесткого диска:</span><span class="sxs-lookup"><span data-stu-id="8ffa2-113">For a standard HDD:</span></span><br/> <span data-ttu-id="8ffa2-114">Все содержимое тома доступно.</span><span class="sxs-lookup"><span data-stu-id="8ffa2-114">The full contents of the volume are accessible.</span></span> <span data-ttu-id="8ffa2-115">Незаблокированный том либо полностью расшифровывается, либо имеет ключ шифрования, доступный на диске Clear on.</span><span class="sxs-lookup"><span data-stu-id="8ffa2-115">An unlocked volume is either fully decrypted or has the encryption key available in the clear on disk.</span></span> <span data-ttu-id="8ffa2-116">Том, содержащий текущую работающую операционную систему (например, запуск тома Windows), всегда доступен и не может быть заблокирован.</span><span class="sxs-lookup"><span data-stu-id="8ffa2-116">The volume containing the current running operating system (for example, the running Windows volume) is always accessible and cannot be locked.</span></span><br/> <span data-ttu-id="8ffa2-117">Для ЕХДД:</span><span class="sxs-lookup"><span data-stu-id="8ffa2-117">For an EHDD:</span></span><br/> <span data-ttu-id="8ffa2-118">Диапазон бессрочно разблокируется.</span><span class="sxs-lookup"><span data-stu-id="8ffa2-118">The band is perpetually unlocked.</span></span><br/> |
| <span id="Locked"></span><span id="locked"></span><span id="LOCKED"></span><dl> <span data-ttu-id="8ffa2-119"><dt>**Заблокировано**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8ffa2-119"><dt>**Locked**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="8ffa2-120">Для стандартного жесткого диска:</span><span class="sxs-lookup"><span data-stu-id="8ffa2-120">For a standard HDD:</span></span><br/> <span data-ttu-id="8ffa2-121">Все содержимое тома или его часть недоступна.</span><span class="sxs-lookup"><span data-stu-id="8ffa2-121">All or a portion of the contents of the volume are not accessible.</span></span> <span data-ttu-id="8ffa2-122">Заблокированный том должен быть частично или полностью зашифрован и не должен иметь ключ шифрования, доступный на диске Clear on.</span><span class="sxs-lookup"><span data-stu-id="8ffa2-122">A locked volume must be partially or fully encrypted and must not have the encryption key available in the clear on disk.</span></span><br/> <span data-ttu-id="8ffa2-123">Для ЕХДД:</span><span class="sxs-lookup"><span data-stu-id="8ffa2-123">For an EHDD:</span></span><br/> <span data-ttu-id="8ffa2-124">Полоса разблокирована или заблокирована.</span><span class="sxs-lookup"><span data-stu-id="8ffa2-124">The band is unlocked or locked.</span></span><br/>                                                                                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ffa2-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ffa2-125">Return value</span></span>

<span data-ttu-id="8ffa2-126">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8ffa2-126">Type: **uint32**</span></span>

<span data-ttu-id="8ffa2-127">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="8ffa2-127">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="8ffa2-128">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="8ffa2-128">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="8ffa2-129">Описание</span><span class="sxs-lookup"><span data-stu-id="8ffa2-129">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="8ffa2-130"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8ffa2-130"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="8ffa2-131">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="8ffa2-131">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8ffa2-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ffa2-132">Remarks</span></span>

<span data-ttu-id="8ffa2-133">Используйте [**унлокквисекстерналкэй**](unlockwithexternalkey-win32-encryptablevolume.md) и [**унлокквиснумерикалпассворд**](unlockwithnumericalpassword-win32-encryptablevolume.md) для получения доступа к содержимому тома.</span><span class="sxs-lookup"><span data-stu-id="8ffa2-133">Use the [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) and [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) to get access to the volume contents.</span></span> <span data-ttu-id="8ffa2-134">Используйте метод [**Lock**](lock-win32-encryptablevolume.md) для получения доступа к содержимому тома.</span><span class="sxs-lookup"><span data-stu-id="8ffa2-134">Use the [**Lock**](lock-win32-encryptablevolume.md) method to relinquish access to volume contents.</span></span>

<span data-ttu-id="8ffa2-135">Том, содержащий текущую операционную систему, всегда доступен и не может быть заблокирован.</span><span class="sxs-lookup"><span data-stu-id="8ffa2-135">The volume that contains the currently running operating system is always accessible and cannot be locked.</span></span>

<span data-ttu-id="8ffa2-136">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="8ffa2-136">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8ffa2-137">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8ffa2-137">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="8ffa2-138">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="8ffa2-138">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8ffa2-139">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="8ffa2-139">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ffa2-140">Требования</span><span class="sxs-lookup"><span data-stu-id="8ffa2-140">Requirements</span></span>



| <span data-ttu-id="8ffa2-141">Требование</span><span class="sxs-lookup"><span data-stu-id="8ffa2-141">Requirement</span></span> | <span data-ttu-id="8ffa2-142">Значение</span><span class="sxs-lookup"><span data-stu-id="8ffa2-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ffa2-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8ffa2-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8ffa2-144">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="8ffa2-144">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8ffa2-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8ffa2-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8ffa2-146">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8ffa2-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8ffa2-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8ffa2-147">Namespace</span></span><br/>                | <span data-ttu-id="8ffa2-148">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="8ffa2-148">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="8ffa2-149">MOF</span><span class="sxs-lookup"><span data-stu-id="8ffa2-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ffa2-150"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ffa2-150"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ffa2-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ffa2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ffa2-152">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="8ffa2-152">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
