---
description: Защищает ключ шифрования тома с помощью специального отформатированного пароля с 48 цифрами.
ms.assetid: 23e0b79a-2feb-441a-9785-7ecd3bb4b6c6
title: Метод Протекткэйвиснумерикалпассворд класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: fd17727bc71dbbe517b6424135e1205035027a00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911571"
---
# <a name="protectkeywithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="11de0-103">Метод Протекткэйвиснумерикалпассворд \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="11de0-103">ProtectKeyWithNumericalPassword method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="11de0-104">Метод **протекткэйвиснумерикалпассворд** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) защищает ключ шифрования тома с помощью специального отформатированного пароля с 48 цифрами.</span><span class="sxs-lookup"><span data-stu-id="11de0-104">The **ProtectKeyWithNumericalPassword** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key with a specially formatted 48-digit password.</span></span> <span data-ttu-id="11de0-105">Этот числовой пароль можно использовать для восстановления после сбоев проверки подлинности других предохранителей ключа (например, TPM).</span><span class="sxs-lookup"><span data-stu-id="11de0-105">This numerical password can be used to recover from the authentication failures of other key protectors (for example, TPM).</span></span>

<span data-ttu-id="11de0-106">Для тома создается предохранитель ключа типа "числовой пароль".</span><span class="sxs-lookup"><span data-stu-id="11de0-106">A key protector of type "Numerical Password" is created for the volume.</span></span>

<span data-ttu-id="11de0-107">Используйте метод [**иснумерикалпассвордвалид**](isnumericalpasswordvalid-win32-encryptablevolume.md) для проверки формата числового пароля.</span><span class="sxs-lookup"><span data-stu-id="11de0-107">Use the [**IsNumericalPasswordValid**](isnumericalpasswordvalid-win32-encryptablevolume.md) method to validate the format of the numerical password.</span></span>

## <a name="syntax"></a><span data-ttu-id="11de0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11de0-108">Syntax</span></span>


```mof
uint32 ProtectKeyWithNumericalPassword(
  [in, optional] string FriendlyName,
  [in, optional] string NumericalPassword,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="11de0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="11de0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11de0-110">*FriendlyName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="11de0-110">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="11de0-111">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="11de0-111">Type: **string**</span></span>

<span data-ttu-id="11de0-112">Строка, указывающая назначенный пользователем идентификатор для этого предохранителя ключа.</span><span class="sxs-lookup"><span data-stu-id="11de0-112">A string that specifies a user-assigned identifier for this key protector.</span></span> <span data-ttu-id="11de0-113">Если этот параметр не указан, используется пустое значение.</span><span class="sxs-lookup"><span data-stu-id="11de0-113">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="11de0-114">*Нумерикалпассворд* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="11de0-114">*NumericalPassword* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="11de0-115">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="11de0-115">Type: **string**</span></span>

<span data-ttu-id="11de0-116">Строка, указывающая специально отформатированный числовой пароль в 48 цифр.</span><span class="sxs-lookup"><span data-stu-id="11de0-116">A string that specifies the specially formatted 48-digit numerical password.</span></span>

<span data-ttu-id="11de0-117">Числовой пароль должен содержать 48 цифр.</span><span class="sxs-lookup"><span data-stu-id="11de0-117">The numerical password must contain 48 digits.</span></span> <span data-ttu-id="11de0-118">Эти цифры можно разделить на 8 групп из 6 цифр, с последней цифрой в каждой группе, указывающей на значение контрольной суммы для группы.</span><span class="sxs-lookup"><span data-stu-id="11de0-118">These digits can be divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="11de0-119">Каждая группа из 6 цифр должна быть кратной 11 и должна быть меньше 720896.</span><span class="sxs-lookup"><span data-stu-id="11de0-119">Each group of 6 digits must be divisible by 11 and must be less than 720896.</span></span> <span data-ttu-id="11de0-120">При условии, что группа из шести цифр помечена как x1, x2, X3, X4, x5 и X6, контрольная сумма X6 вычисляется как – x1 + x2 – X3 + X4 – x5 mod 11.</span><span class="sxs-lookup"><span data-stu-id="11de0-120">Assuming a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="11de0-121">Группы цифр можно разделять пробелами или дефисами.</span><span class="sxs-lookup"><span data-stu-id="11de0-121">The groups of digits can optionally be separated by a space or hyphen.</span></span> <span data-ttu-id="11de0-122">Таким образом, "XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX" или "XXXXXX XXXXXX XXXXXX XXXXXX (xxxxxx) XXXXXX XXXXXX" может также содержать допустимые числовые пароли.</span><span class="sxs-lookup"><span data-stu-id="11de0-122">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" or "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" may also contain valid numerical passwords.</span></span>

<span data-ttu-id="11de0-123">Если числовой пароль не указан, он создается случайным образом.</span><span class="sxs-lookup"><span data-stu-id="11de0-123">If no numerical password is specified, one is randomly generated.</span></span> <span data-ttu-id="11de0-124">Используйте метод [**жеткэйпротекторнумерикалпассворд**](getkeyprotectornumericalpassword-win32-encryptablevolume.md) для получения пароля, созданного случайным образом.</span><span class="sxs-lookup"><span data-stu-id="11de0-124">Use the [**GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md) method to obtain the randomly generated password.</span></span>

</dd> <dt>

<span data-ttu-id="11de0-125">*Волумекэйпротекторид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="11de0-125">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11de0-126">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="11de0-126">Type: **string**</span></span>

<span data-ttu-id="11de0-127">Строка, которая является уникальным идентификатором, связанным с созданным предохранителем, который можно использовать для управления предохранителем ключа.</span><span class="sxs-lookup"><span data-stu-id="11de0-127">A string that is the unique identifier associated with the created protector and that can be used to manage the key protector.</span></span>

<span data-ttu-id="11de0-128">Если диск поддерживает аппаратное шифрование, а BitLocker не использует нестандартное владение, для строки идентификатора задается значение "BitLocker", а предохранитель ключа записывается в метаданные диапазона.</span><span class="sxs-lookup"><span data-stu-id="11de0-128">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11de0-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11de0-129">Return value</span></span>

<span data-ttu-id="11de0-130">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11de0-130">Type: **uint32**</span></span>

<span data-ttu-id="11de0-131">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="11de0-131">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="11de0-132">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="11de0-132">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="11de0-133">Описание</span><span class="sxs-lookup"><span data-stu-id="11de0-133">Description</span></span>                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11de0-134"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="11de0-134"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="11de0-135">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="11de0-135">The method was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="11de0-136"><dt>**Д \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="11de0-136"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="11de0-137">Параметр *нумерикалпассворд* имеет недопустимый формат.</span><span class="sxs-lookup"><span data-stu-id="11de0-137">The *NumericalPassword* parameter does not have a valid format.</span></span><br/> |
| <dl> <span data-ttu-id="11de0-138"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="11de0-138"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="11de0-139">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="11de0-139">The volume is locked.</span></span><br/>                                           |
| <dl> <span data-ttu-id="11de0-140"><dt>**ФВЕ \_ \_Недопустимый \_ \_ формат пароля**</dt> <dt>2150694965 (0x80310035)</dt></span><span class="sxs-lookup"><span data-stu-id="11de0-140"><dt>**FVE\_E\_INVALID\_PASSWORD\_FORMAT**</dt> <dt>2150694965 (0x80310035)</dt></span></span> </dl> | <span data-ttu-id="11de0-141">Параметр *нумерикалпассворд* имеет недопустимый формат.</span><span class="sxs-lookup"><span data-stu-id="11de0-141">The *NumericalPassword* parameter does not have a valid format.</span></span><br/>                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="11de0-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11de0-142">Remarks</span></span>

<span data-ttu-id="11de0-143">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="11de0-143">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="11de0-144">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="11de0-144">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="11de0-145">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="11de0-145">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="11de0-146">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="11de0-146">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11de0-147">Требования</span><span class="sxs-lookup"><span data-stu-id="11de0-147">Requirements</span></span>



| <span data-ttu-id="11de0-148">Требование</span><span class="sxs-lookup"><span data-stu-id="11de0-148">Requirement</span></span> | <span data-ttu-id="11de0-149">Значение</span><span class="sxs-lookup"><span data-stu-id="11de0-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11de0-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11de0-150">Minimum supported client</span></span><br/> | <span data-ttu-id="11de0-151">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="11de0-151">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="11de0-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11de0-152">Minimum supported server</span></span><br/> | <span data-ttu-id="11de0-153">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="11de0-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="11de0-154">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="11de0-154">Namespace</span></span><br/>                | <span data-ttu-id="11de0-155">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="11de0-155">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="11de0-156">MOF</span><span class="sxs-lookup"><span data-stu-id="11de0-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11de0-157"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11de0-157"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11de0-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11de0-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11de0-159">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="11de0-159">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
