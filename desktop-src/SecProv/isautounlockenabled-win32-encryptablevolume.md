---
description: Указывает, разблокируется ли том при подключении.
ms.assetid: cba04d77-1e7c-4191-8eb7-b8c43694193f
title: Метод Исаутаунлоккенаблед класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockEnabled
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2a144d54ff4564fa322efadd521e44c2fa9a8173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682549"
---
# <a name="isautounlockenabled-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="6f4ba-103">Метод Исаутаунлоккенаблед \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="6f4ba-103">IsAutoUnlockEnabled method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="6f4ba-104">Метод **исаутаунлоккенаблед** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) указывает, разблокируется ли том автоматически при его подключении (например, при подключении к компьютеру съемных устройств памяти).</span><span class="sxs-lookup"><span data-stu-id="6f4ba-104">The **IsAutoUnlockEnabled** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the volume is automatically unlocked when it is mounted (for example, when removable memory devices are connected to the computer).</span></span>

## <a name="syntax"></a><span data-ttu-id="6f4ba-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f4ba-105">Syntax</span></span>


```mof
uint32 IsAutoUnlockEnabled(
  [out] boolean IsAutoUnlockEnabled,
  [out] string  VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="6f4ba-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f4ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f4ba-107">*Исаутаунлоккенаблед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6f4ba-107">*IsAutoUnlockEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f4ba-108">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6f4ba-108">Type: **boolean**</span></span>

<span data-ttu-id="6f4ba-109">Логическое значение, равное true, если внешний ключ, используемый для автоматического разблокировки тома, существует и сохранен в текущем томе операционной системы, в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="6f4ba-109">A Boolean value that is true if the external key used to automatically unlock the volume exists and has been stored in the currently running operating system volume, otherwise it is false.</span></span>

</dd> <dt>

<span data-ttu-id="6f4ba-110">*Волумекэйпротекторид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6f4ba-110">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f4ba-111">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="6f4ba-111">Type: **string**</span></span>

<span data-ttu-id="6f4ba-112">Уникальный строковый идентификатор, содержащий связанный идентификатор предохранителя ключа зашифрованного тома, если *исаутаунлоккенаблед* имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="6f4ba-112">A unique string identifier that contains the associated encrypted volume key protector ID if *IsAutoUnlockEnabled* is true.</span></span>

<span data-ttu-id="6f4ba-113">Если *исаутаунлоккенаблед* имеет значение false, *волумекэйпротекторид* является пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="6f4ba-113">If *IsAutoUnlockEnabled* is false, *VolumeKeyProtectorID* is an empty string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f4ba-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6f4ba-114">Return value</span></span>

<span data-ttu-id="6f4ba-115">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6f4ba-115">Type: **uint32**</span></span>

<span data-ttu-id="6f4ba-116">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="6f4ba-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="6f4ba-117">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="6f4ba-117">Return code/value</span></span>                                                                                                                                                                     | <span data-ttu-id="6f4ba-118">Описание</span><span class="sxs-lookup"><span data-stu-id="6f4ba-118">Description</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6f4ba-119"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6f4ba-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                     | <span data-ttu-id="6f4ba-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="6f4ba-120">The method was successful.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="6f4ba-121"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="6f4ba-121"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>    | <span data-ttu-id="6f4ba-122">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="6f4ba-122">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="6f4ba-123">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="6f4ba-123">Add a key protector to enable BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="6f4ba-124"><dt>**ФВЕ \_ E \_ не \_ DATA \_ Volume**</dt> <dt>2150694937 (0x80310019)</dt></span><span class="sxs-lookup"><span data-stu-id="6f4ba-124"><dt>**FVE\_E\_NOT\_DATA\_VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span></span> </dl> | <span data-ttu-id="6f4ba-125">Этот метод не может быть выполнен для текущего тома операционной системы.</span><span class="sxs-lookup"><span data-stu-id="6f4ba-125">The method cannot be run for the currently running operating system volume.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="6f4ba-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6f4ba-126">Remarks</span></span>

<span data-ttu-id="6f4ba-127">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="6f4ba-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6f4ba-128">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="6f4ba-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="6f4ba-129">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="6f4ba-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6f4ba-130">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="6f4ba-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f4ba-131">Требования</span><span class="sxs-lookup"><span data-stu-id="6f4ba-131">Requirements</span></span>



| <span data-ttu-id="6f4ba-132">Требование</span><span class="sxs-lookup"><span data-stu-id="6f4ba-132">Requirement</span></span> | <span data-ttu-id="6f4ba-133">Значение</span><span class="sxs-lookup"><span data-stu-id="6f4ba-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f4ba-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6f4ba-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6f4ba-135">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="6f4ba-135">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6f4ba-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6f4ba-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6f4ba-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6f4ba-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6f4ba-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6f4ba-138">Namespace</span></span><br/>                | <span data-ttu-id="6f4ba-139">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="6f4ba-139">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="6f4ba-140">MOF</span><span class="sxs-lookup"><span data-stu-id="6f4ba-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f4ba-141"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f4ba-141"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f4ba-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f4ba-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f4ba-143">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="6f4ba-143">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
