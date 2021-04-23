---
description: Указывает, существуют ли какие либо внешние ключи или связанные сведения, которые могут использоваться для автоматического разблокировки томов данных в текущем томе операционной системы.
ms.assetid: 37e7fe85-312d-49ff-aa6b-8c76c4fc4bba
title: Метод Исаутаунлокккэйсторед класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockKeyStored
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: aedb834bdfd26ce4b348a41b4046c0c4e2c7e260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684056"
---
# <a name="isautounlockkeystored-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="84175-103">Метод Исаутаунлокккэйсторед \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="84175-103">IsAutoUnlockKeyStored method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="84175-104">Метод **исаутаунлокккэйсторед** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) указывает, существуют ли внешние ключи или связанные сведения, которые могут использоваться для автоматического разблокировки томов данных в текущем томе операционной системы.</span><span class="sxs-lookup"><span data-stu-id="84175-104">The **IsAutoUnlockKeyStored** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether any external keys or related information that may be used to automatically unlock data volumes exist in the currently running operating system volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="84175-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84175-105">Syntax</span></span>


```mof
uint32 IsAutoUnlockKeyStored(
  [out] boolean IsAutoUnlockKeyStored
);
```



## <a name="parameters"></a><span data-ttu-id="84175-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="84175-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84175-107">*Исаутаунлокккэйсторед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="84175-107">*IsAutoUnlockKeyStored* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84175-108">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="84175-108">Type: **boolean**</span></span>

<span data-ttu-id="84175-109">Имеет **значение true** , если какие-либо сведения, которые могут использоваться для автоматической разблокировки томов данных, хранятся в реестре текущего тома операционной системы.</span><span class="sxs-lookup"><span data-stu-id="84175-109">Is **true** if any information that can be used to automatically unlock data volumes is stored in the registry of the currently running operating system volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84175-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84175-110">Return value</span></span>

<span data-ttu-id="84175-111">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84175-111">Type: **uint32**</span></span>

<span data-ttu-id="84175-112">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="84175-112">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="84175-113">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="84175-113">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="84175-114">Описание</span><span class="sxs-lookup"><span data-stu-id="84175-114">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="84175-115"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="84175-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="84175-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="84175-116">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="84175-117"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="84175-117"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>  | <span data-ttu-id="84175-118">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="84175-118">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="84175-119">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="84175-119">Add a key protector to enable BitLocker.</span></span> <br/> |
| <dl> <span data-ttu-id="84175-120"><dt>**ФВЕ \_ E \_ не \_ OS \_ Volume**</dt> <dt>2150694952 (0x80310028)</dt></span><span class="sxs-lookup"><span data-stu-id="84175-120"><dt>**FVE\_E\_NOT\_OS\_VOLUME**</dt> <dt>2150694952 (0x80310028)</dt></span></span> </dl> | <span data-ttu-id="84175-121">Этот метод можно выполнить только для текущего тома операционной системы.</span><span class="sxs-lookup"><span data-stu-id="84175-121">The method can only be run for the currently running operating system volume.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="84175-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84175-122">Remarks</span></span>

<span data-ttu-id="84175-123">Используйте [**клеараллаутаунлокккэйс**](clearallautounlockkeys-win32-encryptablevolume.md) , чтобы удалить все сведения об отблокировке из текущего тома операционной системы.</span><span class="sxs-lookup"><span data-stu-id="84175-123">Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) to remove all unlocking information from the currently running operating system volume.</span></span>

<span data-ttu-id="84175-124">Сведения, используемые для разблокировки тома, сохраняются при запуске [**енаблеаутаунлокк**](enableautounlock-win32-encryptablevolume.md) для тома данных во время работы текущего тома операционной системы.</span><span class="sxs-lookup"><span data-stu-id="84175-124">Information used to unlock a volume is stored when [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) is run for a data volume while the currently running operating system volume is running.</span></span>

<span data-ttu-id="84175-125">**Исаутаунлокккэйсторед** отличается от [**исаутаунлоккенаблед**](isautounlockenabled-win32-encryptablevolume.md) в том, что, даже если автоматическая разблокировка отключена для всех томов данных, подключенных к компьютеру в настоящее время, возможно, все равно могут быть разблокированы сведения, связанные с отключенными томами данных или томами данных, которые больше не существуют.</span><span class="sxs-lookup"><span data-stu-id="84175-125">**IsAutoUnlockKeyStored** differs from [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md) in that even if automatic unlocking is disabled for all data volumes currently connected to the computer, there may still be unlocking information associated with disconnected data volumes or data volumes that no longer exist.</span></span>

<span data-ttu-id="84175-126">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="84175-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="84175-127">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="84175-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="84175-128">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="84175-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="84175-129">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="84175-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="84175-130">Требования</span><span class="sxs-lookup"><span data-stu-id="84175-130">Requirements</span></span>



| <span data-ttu-id="84175-131">Требование</span><span class="sxs-lookup"><span data-stu-id="84175-131">Requirement</span></span> | <span data-ttu-id="84175-132">Значение</span><span class="sxs-lookup"><span data-stu-id="84175-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84175-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84175-133">Minimum supported client</span></span><br/> | <span data-ttu-id="84175-134">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="84175-134">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="84175-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84175-135">Minimum supported server</span></span><br/> | <span data-ttu-id="84175-136">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="84175-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84175-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="84175-137">Namespace</span></span><br/>                | <span data-ttu-id="84175-138">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="84175-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="84175-139">MOF</span><span class="sxs-lookup"><span data-stu-id="84175-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84175-140"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84175-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84175-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84175-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84175-142">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="84175-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
