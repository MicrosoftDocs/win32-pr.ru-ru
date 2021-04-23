---
description: Отключает том и удаляет ключ шифрования тома из системной памяти.
ms.assetid: 8d6e42a0-7b43-46d2-aa5e-941567ef2842
title: Метод Lock класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Lock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 8fb6cd7b4134f4921cdaf57414843fb6522c5823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897054"
---
# <a name="lock-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f190a-103">Метод Lock \_ класса Енкриптаблеволуме Win32</span><span class="sxs-lookup"><span data-stu-id="f190a-103">Lock method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f190a-104">Метод **Lock** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) отключает том и удаляет ключ шифрования тома из системной памяти.</span><span class="sxs-lookup"><span data-stu-id="f190a-104">The **Lock** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class dismounts the volume and removes the volume's encryption key from system memory.</span></span> <span data-ttu-id="f190a-105">Содержимое тома остается недоступным до тех пор, пока не будет разблокировано методом [**унлокквисекстерналкэй**](unlockwithexternalkey-win32-encryptablevolume.md) или методом [**унлокквиснумерикалпассворд**](unlockwithnumericalpassword-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="f190a-105">The contents of the volume remain inaccessible until it is unlocked by either the [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) method or the [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) method.</span></span> <span data-ttu-id="f190a-106">Этот метод не может быть выполнен для текущего тома операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f190a-106">This method cannot be successfully run for the currently running operating system volume.</span></span>

> [!Note]  
> <span data-ttu-id="f190a-107">Если диск поддерживает аппаратное шифрование, для полосы задается значение "заблокировано".</span><span class="sxs-lookup"><span data-stu-id="f190a-107">If the disc supports hardware encryption, the band is set to "locked".</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f190a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f190a-108">Syntax</span></span>


```mof
uint32 Lock(
  [in, optional] boolean ForceDismount
);
```



## <a name="parameters"></a><span data-ttu-id="f190a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f190a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f190a-110">*Форцедисмаунт* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f190a-110">*ForceDismount* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f190a-111">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f190a-111">Type: **boolean**</span></span>

<span data-ttu-id="f190a-112">Если задано **значение true** , диск принудительно отключается.</span><span class="sxs-lookup"><span data-stu-id="f190a-112">If **true** the disk is forcibly dismounted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f190a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f190a-113">Return value</span></span>

<span data-ttu-id="f190a-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f190a-114">Type: **uint32**</span></span>

<span data-ttu-id="f190a-115">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="f190a-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="f190a-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="f190a-116">Return code/value</span></span>                                                                                                                                                                           | <span data-ttu-id="f190a-117">Описание</span><span class="sxs-lookup"><span data-stu-id="f190a-117">Description</span></span>                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f190a-118"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f190a-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                           | <span data-ttu-id="f190a-119">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="f190a-119">The method was successful.</span></span><br/>                                                                                                                                     |
| <dl> <span data-ttu-id="f190a-120"><dt>**Д \_ \_Отказано в доступе**</dt> <dt>2147942405 (0x80070005)</dt></span><span class="sxs-lookup"><span data-stu-id="f190a-120"><dt>**E\_ACCESS\_DENIED**</dt> <dt>2147942405 (0x80070005)</dt></span></span> </dl>               | <span data-ttu-id="f190a-121">Приложения обращаются к этому тому.</span><span class="sxs-lookup"><span data-stu-id="f190a-121">Applications are accessing this volume.</span></span> <span data-ttu-id="f190a-122">Если доступ имеет неисключительный результат, при указании значения true для параметра *форцедисмаунт* можно успешно запустить метод.</span><span class="sxs-lookup"><span data-stu-id="f190a-122">If all access is nonexclusive, specifying the *ForceDismount* parameter as true allows the method to run successfully.</span></span><br/> |
| <dl> <span data-ttu-id="f190a-123"><dt>**ФВЕ \_ E \_ не \_ зашифровано**</dt> <dt>2150694913 (0x80310001)</dt></span><span class="sxs-lookup"><span data-stu-id="f190a-123"><dt>**FVE\_E\_NOT\_ENCRYPTED**</dt> <dt>2150694913 (0x80310001)</dt></span></span> </dl>          | <span data-ttu-id="f190a-124">Том полностью расшифровывается и не может быть заблокирован.</span><span class="sxs-lookup"><span data-stu-id="f190a-124">The volume is fully decrypted and cannot be locked.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="f190a-125"><dt>**ФВЕ \_ \_Защита E Protection \_ отключена**</dt> <dt>2150694945 (0x80310021)</dt></span><span class="sxs-lookup"><span data-stu-id="f190a-125"><dt>**FVE\_E\_PROTECTION\_DISABLED**</dt> <dt>2150694945 (0x80310021)</dt></span></span> </dl>    | <span data-ttu-id="f190a-126">Ключ шифрования тома доступен на диске в открытом виде, что предотвращает блокировку тома.</span><span class="sxs-lookup"><span data-stu-id="f190a-126">The volume's encryption key is available in the clear on the disk, preventing the volume from being locked.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="f190a-127"><dt>**ФВЕ \_ 2150694946 \_ \_ \_ требуется ключ восстановления E**</dt> <dt>(0x80310022)</dt></span><span class="sxs-lookup"><span data-stu-id="f190a-127"><dt>**FVE\_E\_RECOVERY\_KEY\_REQUIRED**</dt> <dt>2150694946 (0x80310022)</dt></span></span> </dl> | <span data-ttu-id="f190a-128">Том не имеет предохранителей ключей типа "числовой пароль" или "внешний ключ", необходимых для разблокировки тома.</span><span class="sxs-lookup"><span data-stu-id="f190a-128">The volume does not have key protectors of the type "Numerical Password" or "External Key" that are necessary to unlock the volume.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="f190a-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f190a-129">Remarks</span></span>

<span data-ttu-id="f190a-130">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="f190a-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f190a-131">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f190a-131">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f190a-132">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="f190a-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f190a-133">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f190a-133">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f190a-134">Требования</span><span class="sxs-lookup"><span data-stu-id="f190a-134">Requirements</span></span>



| <span data-ttu-id="f190a-135">Требование</span><span class="sxs-lookup"><span data-stu-id="f190a-135">Requirement</span></span> | <span data-ttu-id="f190a-136">Значение</span><span class="sxs-lookup"><span data-stu-id="f190a-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f190a-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f190a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f190a-138">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="f190a-138">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f190a-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f190a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f190a-140">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f190a-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f190a-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f190a-141">Namespace</span></span><br/>                | <span data-ttu-id="f190a-142">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="f190a-142">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f190a-143">MOF</span><span class="sxs-lookup"><span data-stu-id="f190a-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f190a-144"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f190a-144"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f190a-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f190a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f190a-146">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="f190a-146">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
