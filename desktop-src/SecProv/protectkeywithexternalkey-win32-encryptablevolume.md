---
description: Защищает ключ шифрования тома с помощью 256-разрядного внешнего ключа.
ms.assetid: 768cef38-a00f-4faa-bbe3-9d4a19be2f6d
title: Метод Протекткэйвисекстерналкэй класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: adcbdfdb9ea55139626bf3d1657b2e154c8d2b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682546"
---
# <a name="protectkeywithexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f5415-103">Метод Протекткэйвисекстерналкэй \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="f5415-103">ProtectKeyWithExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f5415-104">Метод **протекткэйвисекстерналкэй** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) защищает ключ шифрования тома с помощью 256-разрядного внешнего ключа.</span><span class="sxs-lookup"><span data-stu-id="f5415-104">The **ProtectKeyWithExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key with a 256-bit external key.</span></span> <span data-ttu-id="f5415-105">Этот внешний ключ можно использовать для восстановления после сбоев проверки подлинности других предохранителей ключа (например, TPM).</span><span class="sxs-lookup"><span data-stu-id="f5415-105">This external key can be used to recover from the authentication failures of other key protectors (for example, TPM).</span></span>

<span data-ttu-id="f5415-106">Используйте метод [**савикстерналкэйтофиле**](saveexternalkeytofile-win32-encryptablevolume.md) , чтобы сохранить этот внешний ключ в файл.</span><span class="sxs-lookup"><span data-stu-id="f5415-106">Use the [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) method to save this external key to a file.</span></span> <span data-ttu-id="f5415-107">USB-устройства памяти, содержащие этот внешний ключ, можно использовать в качестве ключа запуска или ключа восстановления при запуске компьютера.</span><span class="sxs-lookup"><span data-stu-id="f5415-107">USB memory devices that contain this external key can be used as a startup key or a recovery key when the computer starts.</span></span>

<span data-ttu-id="f5415-108">Для тома создается предохранитель ключа типа "внешний ключ".</span><span class="sxs-lookup"><span data-stu-id="f5415-108">A key protector of type "External Key" is created for the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5415-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5415-109">Syntax</span></span>


```mof
uint32 ProtectKeyWithExternalKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="f5415-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5415-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5415-111">*FriendlyName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f5415-111">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f5415-112">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="f5415-112">Type: **string**</span></span>

<span data-ttu-id="f5415-113">Строка, указывающая назначенный пользователем идентификатор для этого предохранителя ключа.</span><span class="sxs-lookup"><span data-stu-id="f5415-113">A string that specifies a user-assigned identifier for this key protector.</span></span> <span data-ttu-id="f5415-114">Если этот параметр не указан, используется пустое значение.</span><span class="sxs-lookup"><span data-stu-id="f5415-114">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="f5415-115">*Екстерналкэй* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f5415-115">*ExternalKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f5415-116">Тип: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="f5415-116">Type: **uint8\[\]**</span></span>

<span data-ttu-id="f5415-117">Массив байтов, указывающий 256-разрядный внешний ключ, используемый для разблокировки тома.</span><span class="sxs-lookup"><span data-stu-id="f5415-117">An array of bytes that specifies the 256-bit external key used to unlock the volume.</span></span>

<span data-ttu-id="f5415-118">Если внешний ключ не указан, он создается случайным образом.</span><span class="sxs-lookup"><span data-stu-id="f5415-118">If no external key is specified, one is randomly generated.</span></span> <span data-ttu-id="f5415-119">Используйте метод [**жеткэйпротекторекстерналкэй**](getkeyprotectorexternalkey-win32-encryptablevolume.md) для получения созданного случайным образом ключа.</span><span class="sxs-lookup"><span data-stu-id="f5415-119">Use the [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) method to obtain the randomly generated key.</span></span>

</dd> <dt>

<span data-ttu-id="f5415-120">*Волумекэйпротекторид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f5415-120">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5415-121">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="f5415-121">Type: **string**</span></span>

<span data-ttu-id="f5415-122">Уникальный строковый идентификатор, используемый для управления предохранителем ключа зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="f5415-122">A unique string identifier used to manage an encrypted volume key protector.</span></span>

<span data-ttu-id="f5415-123">Если диск поддерживает аппаратное шифрование, а BitLocker не использует нестандартное владение, для строки идентификатора задается значение "BitLocker", а предохранитель ключа записывается в метаданные диапазона.</span><span class="sxs-lookup"><span data-stu-id="f5415-123">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5415-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f5415-124">Return value</span></span>

<span data-ttu-id="f5415-125">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5415-125">Type: **uint32**</span></span>

<span data-ttu-id="f5415-126">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="f5415-126">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="f5415-127">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="f5415-127">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="f5415-128">Описание</span><span class="sxs-lookup"><span data-stu-id="f5415-128">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5415-129"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f5415-129"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="f5415-130">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="f5415-130">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="f5415-131"><dt>**Д \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="f5415-131"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="f5415-132">Параметр *екстерналкэй* предоставляется, но не является массивом размером 4.</span><span class="sxs-lookup"><span data-stu-id="f5415-132">The *ExternalKey* parameter is provided but is not an array of size 4.</span></span><br/>            |
| <dl> <span data-ttu-id="f5415-133"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="f5415-133"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="f5415-134">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="f5415-134">The volume is locked.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="f5415-135"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="f5415-135"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="f5415-136">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="f5415-136">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="f5415-137">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f5415-137">Add a key protector to enable BitLocker.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="f5415-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5415-138">Remarks</span></span>

<span data-ttu-id="f5415-139">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="f5415-139">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f5415-140">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f5415-140">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f5415-141">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="f5415-141">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f5415-142">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f5415-142">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5415-143">Требования</span><span class="sxs-lookup"><span data-stu-id="f5415-143">Requirements</span></span>



| <span data-ttu-id="f5415-144">Требование</span><span class="sxs-lookup"><span data-stu-id="f5415-144">Requirement</span></span> | <span data-ttu-id="f5415-145">Значение</span><span class="sxs-lookup"><span data-stu-id="f5415-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5415-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5415-146">Minimum supported client</span></span><br/> | <span data-ttu-id="f5415-147">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="f5415-147">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f5415-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5415-148">Minimum supported server</span></span><br/> | <span data-ttu-id="f5415-149">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f5415-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f5415-150">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f5415-150">Namespace</span></span><br/>                | <span data-ttu-id="f5415-151">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="f5415-151">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f5415-152">MOF</span><span class="sxs-lookup"><span data-stu-id="f5415-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5415-153"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5415-153"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5415-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5415-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5415-155">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="f5415-155">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
