---
description: Изменяет ПИН-код, связанный с зашифрованным томом.
ms.assetid: 8b0043cc-cf86-44e5-ab7c-038a6782f347
title: Метод Чанжепин класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 385f8cc66eb08bc020cc126cec587eee57a14ca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540951"
---
# <a name="changepin-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="bfe58-103">Метод Чанжепин \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="bfe58-103">ChangePIN method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="bfe58-104">Метод **чанжепин** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) изменяет ПИН-код, связанный с зашифрованным томом.</span><span class="sxs-lookup"><span data-stu-id="bfe58-104">The **ChangePIN** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class changes the PIN associated with an encrypted volume.</span></span> <span data-ttu-id="bfe58-105">Если включена групповая политика "разрешить Расширенные ПИН-коды для запуска", в дополнение к числам ПИН может содержать буквы, символы и пробелы.</span><span class="sxs-lookup"><span data-stu-id="bfe58-105">If the "Allow enhanced PINs for startup" group policy is enabled, a PIN can contain letters, symbols, and spaces in addition to numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfe58-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bfe58-106">Syntax</span></span>


```mof
uint32 ChangePIN(
  [in] string VolumeKeyProtectorID,
  [in] string NewPIN
);
```



## <a name="parameters"></a><span data-ttu-id="bfe58-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bfe58-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfe58-108">*Волумекэйпротекторид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bfe58-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfe58-109">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="bfe58-109">Type: **string**</span></span>

<span data-ttu-id="bfe58-110">Уникальный строковый идентификатор, используемый для управления предохранителем ключа зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="bfe58-110">The unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="bfe58-111">*Невпин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bfe58-111">*NewPIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfe58-112">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="bfe58-112">Type: **string**</span></span>

<span data-ttu-id="bfe58-113">Указанная пользователем личная строка идентификации.</span><span class="sxs-lookup"><span data-stu-id="bfe58-113">A user-specified personal identification string.</span></span> <span data-ttu-id="bfe58-114">Эта строка должна состоять из 4 – 20 цифр или, если включена групповая политика "разрешить Расширенные ПИН-коды для запуска", от 4 до 20 букв, символов, пробелов или чисел.</span><span class="sxs-lookup"><span data-stu-id="bfe58-114">This string must consist of a sequence of 4 to 20 digits or, if the "Allow enhanced PINs for startup" group policy is enabled, 4 to 20 letters, symbols, spaces, or numbers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfe58-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bfe58-115">Return value</span></span>

<span data-ttu-id="bfe58-116">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bfe58-116">Type: **uint32**</span></span>

<span data-ttu-id="bfe58-117">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="bfe58-117">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="bfe58-118">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="bfe58-118">Return code/value</span></span>                                                                                                                                                                                | <span data-ttu-id="bfe58-119">Описание</span><span class="sxs-lookup"><span data-stu-id="bfe58-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bfe58-120"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="bfe58-120"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                | <span data-ttu-id="bfe58-121">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="bfe58-121">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="bfe58-122"><dt>**ФВЕ \_ E \_ загрузочная \_ кддвд**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="bfe58-122"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>              | <span data-ttu-id="bfe58-123">На этом компьютере находится загрузочный компакт-диск или DVD-диск.</span><span class="sxs-lookup"><span data-stu-id="bfe58-123">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="bfe58-124">Удалите компакт-диск или диск DVD и перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="bfe58-124">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="bfe58-125"><dt>**ФВЕ \_ E \_ Недопустимый \_ ПИН-код \_**</dt> <dt>2150695066 (0x8031009A)</dt></span><span class="sxs-lookup"><span data-stu-id="bfe58-125"><dt>**FVE\_E\_INVALID\_PIN\_CHARS**</dt> <dt>2150695066 (0x8031009A)</dt></span></span> </dl>          | <span data-ttu-id="bfe58-126">Параметр *невпин* содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="bfe58-126">The *NewPIN* parameter contains characters that are not valid.</span></span> <span data-ttu-id="bfe58-127">При отключении групповая политика "разрешить Расширенные ПИН-коды для запуска" поддерживаются только цифры.</span><span class="sxs-lookup"><span data-stu-id="bfe58-127">When the "Allow enhanced PINs for startup" Group Policy is disabled, only numbers are supported.</span></span><br/>                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="bfe58-128"><dt>**ФВЕ \_ \_Недопустимый \_ \_ тип предохранителя**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="bfe58-128"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl>     | <span data-ttu-id="bfe58-129">Параметр *волумекэйпротекторид* не ссылается на предохранитель ключа типа "числовой пароль" или "внешний ключ".</span><span class="sxs-lookup"><span data-stu-id="bfe58-129">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="bfe58-130">Используйте метод [**протекткэйвиснумерикалпассворд**](protectkeywithnumericalpassword-win32-encryptablevolume.md) или [**протекткэйвисекстерналкэй**](protectkeywithexternalkey-win32-encryptablevolume.md) для создания предохранителя ключа соответствующего типа.</span><span class="sxs-lookup"><span data-stu-id="bfe58-130">Use either the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) or [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to create a key protector of the appropriate type.</span></span><br/> |
| <dl> <span data-ttu-id="bfe58-131"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="bfe58-131"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>               | <span data-ttu-id="bfe58-132">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="bfe58-132">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="bfe58-133"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="bfe58-133"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>               | <span data-ttu-id="bfe58-134">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="bfe58-134">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="bfe58-135">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="bfe58-135">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="bfe58-136"><dt>**ФВЕ \_ E \_ Policy \_ Недопустимая \_ \_ длина ПИН-кода**</dt> <dt>2150695016 (0x80310068)</dt></span><span class="sxs-lookup"><span data-stu-id="bfe58-136"><dt>**FVE\_E\_POLICY\_INVALID\_PIN\_LENGTH**</dt> <dt>2150695016 (0x80310068)</dt></span></span> </dl> | <span data-ttu-id="bfe58-137">Предоставленный параметр *невпин* имеет длину более 20 символов, короче 4 символов, или короче минимальной длины, указанной групповая политика.</span><span class="sxs-lookup"><span data-stu-id="bfe58-137">The *NewPIN* parameter supplied is either longer than 20 characters, shorter than 4 characters, or shorter than the minimum length specified by Group Policy.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="bfe58-138"><dt>**ФВЕ \_ \_ \_ Не \_ найден предохранитель "E**</dt> <dt>" 2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="bfe58-138"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>        | <span data-ttu-id="bfe58-139">Указанный предохранитель ключа не существует на томе.</span><span class="sxs-lookup"><span data-stu-id="bfe58-139">The provided key protector does not exist on the volume.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="bfe58-140"><dt>**TBS \_ \_Служба E \_ не \_ работает**</dt> <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="bfe58-140"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl>        | <span data-ttu-id="bfe58-141">На этом компьютере не найдены совместимые доверенный платформенный модуль (TPM) (TPM).</span><span class="sxs-lookup"><span data-stu-id="bfe58-141">No compatible Trusted Platform Module (TPM) is found on this computer.</span></span><br/>                                                                                                                                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="bfe58-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bfe58-142">Remarks</span></span>

<span data-ttu-id="bfe58-143">Метод **чанжепин** создает новый модуль TPM и предохранитель ПИН-кода на основе существующих данных предохранителя и вновь предоставленного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="bfe58-143">The **ChangePIN** method creates a new TPM and PIN protector based on the existing protector information and the newly provided PIN.</span></span> <span data-ttu-id="bfe58-144">Новый предохранитель будет иметь тот же идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="bfe58-144">The new protector will have the same GUID.</span></span> <span data-ttu-id="bfe58-145">Метод **чанжепин** также можно вызвать для изменения ПИН-кода любого предохранителя ключа, использующего ПИН-код, например TPM, ПИН-код или доверенный платформенный модуль с ПИН-кодом и USB-портом.</span><span class="sxs-lookup"><span data-stu-id="bfe58-145">The **ChangePIN** method can also be called to change the PIN of any key protector that uses a PIN, for example, TPM and PIN or TPM with PIN and USB.</span></span>

<span data-ttu-id="bfe58-146">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="bfe58-146">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bfe58-147">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="bfe58-147">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="bfe58-148">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="bfe58-148">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bfe58-149">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="bfe58-149">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bfe58-150">Требования</span><span class="sxs-lookup"><span data-stu-id="bfe58-150">Requirements</span></span>



| <span data-ttu-id="bfe58-151">Требование</span><span class="sxs-lookup"><span data-stu-id="bfe58-151">Requirement</span></span> | <span data-ttu-id="bfe58-152">Значение</span><span class="sxs-lookup"><span data-stu-id="bfe58-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfe58-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bfe58-153">Minimum supported client</span></span><br/> | <span data-ttu-id="bfe58-154">Windows 7 Корпоративная, \[ только классические приложения Windows 7 Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="bfe58-154">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bfe58-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bfe58-155">Minimum supported server</span></span><br/> | <span data-ttu-id="bfe58-156">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="bfe58-156">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bfe58-157">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bfe58-157">Namespace</span></span><br/>                | <span data-ttu-id="bfe58-158">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="bfe58-158">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="bfe58-159">MOF</span><span class="sxs-lookup"><span data-stu-id="bfe58-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bfe58-160"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bfe58-160"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfe58-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bfe58-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfe58-162">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="bfe58-162">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
