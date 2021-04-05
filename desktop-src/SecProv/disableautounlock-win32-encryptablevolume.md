---
description: Удаляет внешний ключ, сохраненный на текущем томе операционной системы.
ms.assetid: a8c4bb3b-6566-4173-b550-e89740f1cba6
title: Метод Дисаблеаутаунлокк класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 6dd4e11e2ff4906627c2d790987500062136d56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910052"
---
# <a name="disableautounlock-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="7160d-103">Метод Дисаблеаутаунлокк \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="7160d-103">DisableAutoUnlock method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="7160d-104">Метод **дисаблеаутаунлокк** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) удаляет внешний ключ, сохраненный в текущем томе операционной системы, чтобы при подключении не автоматически разблокировался том данных, например, когда к компьютеру подключены съемные устройства памяти.</span><span class="sxs-lookup"><span data-stu-id="7160d-104">The **DisableAutoUnlock** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class removes the external key saved onto the currently running operating system volume so that a data volume is not automatically unlocked when it is mounted, such as when removable memory devices are connected to the computer.</span></span>

<span data-ttu-id="7160d-105">Если автоматическая разблокировка отключена или приостановлена, для разблокировки тома необходимо использовать методы [**унлокквисекстерналкэй**](unlockwithexternalkey-win32-encryptablevolume.md) или [**унлокквиснумерикалпассворд**](unlockwithnumericalpassword-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="7160d-105">If automatic unlocking is disabled or suspended, the methods [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) or [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) must be used to unlock the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="7160d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7160d-106">Syntax</span></span>


```mof
uint32 DisableAutoUnlock();
```



## <a name="parameters"></a><span data-ttu-id="7160d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7160d-107">Parameters</span></span>

<span data-ttu-id="7160d-108">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7160d-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7160d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7160d-109">Return value</span></span>

<span data-ttu-id="7160d-110">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7160d-110">Type: **uint32**</span></span>

<span data-ttu-id="7160d-111">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="7160d-111">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="7160d-112">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="7160d-112">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="7160d-113">Описание</span><span class="sxs-lookup"><span data-stu-id="7160d-113">Description</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7160d-114"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="7160d-114"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                       | <span data-ttu-id="7160d-115">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="7160d-115">The method was successful.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="7160d-116"><dt> **\_ Том ФВЕ \_ E \_ не \_ привязан**</dt> <dt>2150694935 (0x80310017)</dt></span><span class="sxs-lookup"><span data-stu-id="7160d-116"><dt>**FVE\_E\_VOLUME\_NOT\_BOUND** </dt> <dt>2150694935 (0x80310017)</dt></span></span> </dl> | <span data-ttu-id="7160d-117">Автоматическая разблокировка тома отключена.</span><span class="sxs-lookup"><span data-stu-id="7160d-117">Automatic unlocking on the volume is disabled.</span></span><br/>                                   |
| <dl> <span data-ttu-id="7160d-118"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="7160d-118"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>      | <span data-ttu-id="7160d-119">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="7160d-119">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="7160d-120">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7160d-120">Add a key protector to enable BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="7160d-121"><dt>**ФВЕ \_ E \_ не \_ DATA \_ Volume**</dt> <dt>2150694937 (0x80310019)</dt></span><span class="sxs-lookup"><span data-stu-id="7160d-121"><dt>**FVE\_E\_NOT\_DATA\_VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span></span> </dl>   | <span data-ttu-id="7160d-122">Этот метод не может быть выполнен для текущего тома операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7160d-122">The method cannot be run for the currently running operating system volume.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="7160d-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7160d-123">Remarks</span></span>

<span data-ttu-id="7160d-124">Если ошибки не возвращаются, этот метод удаляет из реестра все идентификаторы предохранителя томов и внешние ключи, используемые для автоматического разблокировки тома.</span><span class="sxs-lookup"><span data-stu-id="7160d-124">If no errors are returned, this method removes from the registry any volume protector IDs and external keys used to automatically unlock the volume.</span></span>

<span data-ttu-id="7160d-125">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="7160d-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7160d-126">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7160d-126">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7160d-127">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="7160d-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7160d-128">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="7160d-128">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7160d-129">Требования</span><span class="sxs-lookup"><span data-stu-id="7160d-129">Requirements</span></span>



| <span data-ttu-id="7160d-130">Требование</span><span class="sxs-lookup"><span data-stu-id="7160d-130">Requirement</span></span> | <span data-ttu-id="7160d-131">Значение</span><span class="sxs-lookup"><span data-stu-id="7160d-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7160d-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7160d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7160d-133">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="7160d-133">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7160d-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7160d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7160d-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7160d-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7160d-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7160d-136">Namespace</span></span><br/>                | <span data-ttu-id="7160d-137">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="7160d-137">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="7160d-138">MOF</span><span class="sxs-lookup"><span data-stu-id="7160d-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7160d-139"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7160d-139"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7160d-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7160d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7160d-141">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="7160d-141">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
