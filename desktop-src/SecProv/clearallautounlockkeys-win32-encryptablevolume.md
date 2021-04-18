---
description: Удаляет все внешние ключи и связанные сведения, сохраненные в текущем томе операционной системы, которые используются для автоматической разблокировки томов данных.
ms.assetid: a5fef793-0634-493d-b62d-cb842844b1e8
title: Метод Клеараллаутаунлокккэйс класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ClearAllAutoUnlockKeys
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b7f7e68891865893c1444a2c5de2370799b74426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682568"
---
# <a name="clearallautounlockkeys-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="862fa-103">Метод Клеараллаутаунлокккэйс \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="862fa-103">ClearAllAutoUnlockKeys method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="862fa-104">Метод **клеараллаутаунлокккэйс** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) удаляет все внешние ключи и связанные сведения, сохраненные в текущем томе операционной системы, которые используются для автоматической разблокировки томов данных.</span><span class="sxs-lookup"><span data-stu-id="862fa-104">The **ClearAllAutoUnlockKeys** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class removes all external keys and related information saved onto the currently running operating system volume that are used to automatically unlock data volumes.</span></span>

## <a name="syntax"></a><span data-ttu-id="862fa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="862fa-105">Syntax</span></span>


```mof
uint32 ClearAllAutoUnlockKeys();
```



## <a name="parameters"></a><span data-ttu-id="862fa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="862fa-106">Parameters</span></span>

<span data-ttu-id="862fa-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="862fa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="862fa-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="862fa-108">Return value</span></span>

<span data-ttu-id="862fa-109">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="862fa-109">Type: **uint32**</span></span>

<span data-ttu-id="862fa-110">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="862fa-110">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="862fa-111">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="862fa-111">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="862fa-112">Описание</span><span class="sxs-lookup"><span data-stu-id="862fa-112">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="862fa-113"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="862fa-113"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="862fa-114">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="862fa-114">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="862fa-115"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="862fa-115"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>  | <span data-ttu-id="862fa-116">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="862fa-116">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="862fa-117">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="862fa-117">Add a key protector to enable BitLocker.</span></span> <br/> |
| <dl> <span data-ttu-id="862fa-118"><dt>**ФВЕ \_ E \_ не \_ OS \_ Volume**</dt> <dt>2150694952 (0x80310028)</dt></span><span class="sxs-lookup"><span data-stu-id="862fa-118"><dt>**FVE\_E\_NOT\_OS\_VOLUME**</dt> <dt>2150694952 (0x80310028)</dt></span></span> </dl> | <span data-ttu-id="862fa-119">Этот метод можно выполнить только для текущего тома операционной системы.</span><span class="sxs-lookup"><span data-stu-id="862fa-119">The method can only be run for the currently running operating system volume.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="862fa-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="862fa-120">Remarks</span></span>

<span data-ttu-id="862fa-121">**Клеараллаутаунлокккэйс** обеспечивает те же функции, что и запуск [**дисаблеаутаунлокк**](disableautounlock-win32-encryptablevolume.md) для каждого тома данных, который когда-либо был связан с работающей в данный момент операционной системой, даже те тома данных, которые в настоящее время не подключены к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="862fa-121">**ClearAllAutoUnlockKeys** achieves the same functionality as running [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) for every data volume that has ever been associated with the currently running operating system, even data volumes that are not currently connected to the computer.</span></span> <span data-ttu-id="862fa-122">Она также удаляет все устаревшие сведения о разблокировании, связанные с томами данных, которые больше не существуют.</span><span class="sxs-lookup"><span data-stu-id="862fa-122">It also removes any stale unlocking information associated with data volumes that no longer exist.</span></span>

<span data-ttu-id="862fa-123">Перед вызовом [**расшифрования**](decrypt-win32-encryptablevolume.md) для текущего тома операционной системы используйте **клеараллаутаунлокккэйс** , чтобы убедиться, что информация, помещенная в реестр операционной системы для автоматической разблокировки томов данных, недоступна на диске Clear on.</span><span class="sxs-lookup"><span data-stu-id="862fa-123">Before calling [**Decrypt**](decrypt-win32-encryptablevolume.md) on the currently running operating system volume, use **ClearAllAutoUnlockKeys** to ensure that information placed in the operating system registry to automatically unlock data volumes is not accessible in the clear on disk.</span></span>

<span data-ttu-id="862fa-124">После успешного выполнения **клеараллаутаунлокккэйс** методы [**унлокквисекстерналкэй**](unlockwithexternalkey-win32-encryptablevolume.md) или [**унлокквиснумерикалпассворд**](unlockwithnumericalpassword-win32-encryptablevolume.md) можно использовать для разблокировки всех томов данных на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="862fa-124">After **ClearAllAutoUnlockKeys** runs successfully, the methods [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) or [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) can be used to unlock all data volumes on this computer.</span></span> <span data-ttu-id="862fa-125">Используйте [**енаблеаутаунлокк**](enableautounlock-win32-encryptablevolume.md) для повторного включения автоматического разблокировки тома данных.</span><span class="sxs-lookup"><span data-stu-id="862fa-125">Use [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) to re-enable automatic unlocking of a data volume.</span></span>

<span data-ttu-id="862fa-126">Если другие ошибки не возвращаются, **клеараллаутаунлокккэйс** удаляет из реестра все идентификаторы предохранителя томов и внешние ключи, используемые для автоматической разблокировки любого тома данных, который когда-либо был связан с текущим томом операционной системы.</span><span class="sxs-lookup"><span data-stu-id="862fa-126">If no other errors are returned, **ClearAllAutoUnlockKeys** removes from the registry any volume protector IDs and external keys used to automatically unlock any data volume that has ever been associated with the currently running operating system volume.</span></span>

<span data-ttu-id="862fa-127">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="862fa-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="862fa-128">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="862fa-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="862fa-129">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="862fa-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="862fa-130">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="862fa-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="862fa-131">Требования</span><span class="sxs-lookup"><span data-stu-id="862fa-131">Requirements</span></span>



| <span data-ttu-id="862fa-132">Требование</span><span class="sxs-lookup"><span data-stu-id="862fa-132">Requirement</span></span> | <span data-ttu-id="862fa-133">Значение</span><span class="sxs-lookup"><span data-stu-id="862fa-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="862fa-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="862fa-134">Minimum supported client</span></span><br/> | <span data-ttu-id="862fa-135">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="862fa-135">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="862fa-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="862fa-136">Minimum supported server</span></span><br/> | <span data-ttu-id="862fa-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="862fa-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="862fa-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="862fa-138">Namespace</span></span><br/>                | <span data-ttu-id="862fa-139">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="862fa-139">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="862fa-140">MOF</span><span class="sxs-lookup"><span data-stu-id="862fa-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="862fa-141"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="862fa-141"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="862fa-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="862fa-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="862fa-143">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="862fa-143">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
