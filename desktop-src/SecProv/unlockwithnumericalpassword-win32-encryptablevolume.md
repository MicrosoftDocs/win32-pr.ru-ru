---
description: Использует предоставленный числовой пароль для доступа к содержимому тома данных.
ms.assetid: ee968372-18a4-4748-ab18-2f1b8d297f0e
title: Метод Унлокквиснумерикалпассворд класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 09676e4a57e03f86b18259a7ffb472a6682eafd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897042"
---
# <a name="unlockwithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="2aa62-103">Метод Унлокквиснумерикалпассворд \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="2aa62-103">UnlockWithNumericalPassword method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="2aa62-104">Метод **унлокквиснумерикалпассворд** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) использует предоставленный числовой пароль для доступа к содержимому тома данных.</span><span class="sxs-lookup"><span data-stu-id="2aa62-104">The **UnlockWithNumericalPassword** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses a provided numerical password to access the contents of a data volume.</span></span>

<span data-ttu-id="2aa62-105">Ключ шифрования тома должен быть защищен с помощью одного или нескольких предохранителей ключа типа "числовой пароль" (с помощью метода [**протекткэйвиснумерикалпассворд**](protectkeywithnumericalpassword-win32-encryptablevolume.md) ), чтобы иметь возможность разблокировать том с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="2aa62-105">The volume's encryption key must have been secured with one or more key protectors of the type "Numerical Password" (by using the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) method) to be able to unlock the volume with this method.</span></span>

> [!Note]  
> <span data-ttu-id="2aa62-106">Если диск поддерживает аппаратное шифрование, эта функция устанавливает для полосы состояние "разблокирован".</span><span class="sxs-lookup"><span data-stu-id="2aa62-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2aa62-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2aa62-107">Syntax</span></span>


```mof
uint32 UnlockWithNumericalPassword(
  [in] string NumericalPassword
);
```



## <a name="parameters"></a><span data-ttu-id="2aa62-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2aa62-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2aa62-109">*Нумерикалпассворд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2aa62-109">*NumericalPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aa62-110">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="2aa62-110">Type: **string**</span></span>

<span data-ttu-id="2aa62-111">Строка, указывающая числовой пароль.</span><span class="sxs-lookup"><span data-stu-id="2aa62-111">A string that specifies the numerical password.</span></span>

<span data-ttu-id="2aa62-112">Числовой пароль должен содержать 48 цифр.</span><span class="sxs-lookup"><span data-stu-id="2aa62-112">The numerical password must contain 48 digits.</span></span> <span data-ttu-id="2aa62-113">Эти цифры можно разделить на 8 групп из 6 цифр, с последней цифрой в каждой группе, указывающей на значение контрольной суммы для группы.</span><span class="sxs-lookup"><span data-stu-id="2aa62-113">These digits can be divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="2aa62-114">Каждая группа из 6 цифр должна быть кратной 11 и должна быть меньше 65536.</span><span class="sxs-lookup"><span data-stu-id="2aa62-114">Each group of 6 digits must be divisible by 11 and must be less than 65536.</span></span> <span data-ttu-id="2aa62-115">При условии, что группа из шести цифр помечена как x1, x2, X3, X4, x5 и X6, контрольная сумма X6 вычисляется как – x1 + x2 – X3 + X4 – x5 mod 11.</span><span class="sxs-lookup"><span data-stu-id="2aa62-115">Assuming a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="2aa62-116">Группы цифр можно разделять пробелами или дефисами.</span><span class="sxs-lookup"><span data-stu-id="2aa62-116">The groups of digits can optionally be separated by a space or hyphen.</span></span> <span data-ttu-id="2aa62-117">Таким образом, "XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX" или "XXXXXX XXXXXX XXXXXX XXXXXX (xxxxxx) XXXXXX XXXXXX" может также содержать допустимые числовые пароли.</span><span class="sxs-lookup"><span data-stu-id="2aa62-117">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" or "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" may also contain valid numerical passwords.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2aa62-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2aa62-118">Return value</span></span>

<span data-ttu-id="2aa62-119">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2aa62-119">Type: **uint32**</span></span>

<span data-ttu-id="2aa62-120">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="2aa62-120">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="2aa62-121">Если том уже разблокирован и другие ошибки не возникают, этот метод возвращает значение 0.</span><span class="sxs-lookup"><span data-stu-id="2aa62-121">If the volume is already unlocked and no other errors occur, this method returns 0.</span></span>



| <span data-ttu-id="2aa62-122">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="2aa62-122">Return code/value</span></span>                                                                                                                                                                             | <span data-ttu-id="2aa62-123">Описание</span><span class="sxs-lookup"><span data-stu-id="2aa62-123">Description</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2aa62-124"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="2aa62-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                             | <span data-ttu-id="2aa62-125">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="2aa62-125">The method was successful.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="2aa62-126"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="2aa62-126"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>            | <span data-ttu-id="2aa62-127">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="2aa62-127">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="2aa62-128">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2aa62-128">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                   |
| <dl> <span data-ttu-id="2aa62-129"><dt>**ФВЕ \_ \_ \_ Не \_ найден предохранитель "E**</dt> <dt>" 2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="2aa62-129"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>     | <span data-ttu-id="2aa62-130">Том не имеет предохранителя ключа типа "числовой пароль".</span><span class="sxs-lookup"><span data-stu-id="2aa62-130">The volume does not have a key protector of the type "Numerical Password".</span></span><br/> <span data-ttu-id="2aa62-131">Параметр *нумерикалпассворд* имеет допустимый формат, но для разблокировки тома нельзя использовать числовой пароль.</span><span class="sxs-lookup"><span data-stu-id="2aa62-131">The *NumericalPassword* parameter has a valid format, but you cannot use a numerical password to unlock the volume.</span></span><br/>           |
| <dl> <span data-ttu-id="2aa62-132"><dt>**ФВЕ \_ E \_ Failed \_ authentication**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="2aa62-132"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>    | <span data-ttu-id="2aa62-133">Параметр *нумерикалпассворд* не может разблокировать том.</span><span class="sxs-lookup"><span data-stu-id="2aa62-133">The *NumericalPassword* parameter cannot unlock the volume.</span></span><br/> <span data-ttu-id="2aa62-134">Один или несколько предохранителей ключа типа "числовой пароль" существуют, но указанный параметр *нумерикалпассворд* не может разблокировать том.</span><span class="sxs-lookup"><span data-stu-id="2aa62-134">One or more key protectors of the type "Numerical Password" exist, but the specified *NumericalPassword* parameter cannot unlock the volume.</span></span><br/> |
| <dl> <span data-ttu-id="2aa62-135"><dt>**ФВЕ \_ \_Недопустимый \_ \_ формат пароля**</dt> <dt>2150694965 (0x80310035)</dt></span><span class="sxs-lookup"><span data-stu-id="2aa62-135"><dt>**FVE\_E\_INVALID\_PASSWORD\_FORMAT**</dt> <dt>2150694965 (0x80310035)</dt></span></span> </dl> | <span data-ttu-id="2aa62-136">Параметр *нумерикалпассворд* имеет недопустимый формат.</span><span class="sxs-lookup"><span data-stu-id="2aa62-136">The *NumericalPassword* parameter does not have a valid format.</span></span><br/>                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="2aa62-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2aa62-137">Remarks</span></span>

<span data-ttu-id="2aa62-138">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="2aa62-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2aa62-139">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="2aa62-139">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="2aa62-140">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="2aa62-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2aa62-141">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="2aa62-141">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2aa62-142">Требования</span><span class="sxs-lookup"><span data-stu-id="2aa62-142">Requirements</span></span>



| <span data-ttu-id="2aa62-143">Требование</span><span class="sxs-lookup"><span data-stu-id="2aa62-143">Requirement</span></span> | <span data-ttu-id="2aa62-144">Значение</span><span class="sxs-lookup"><span data-stu-id="2aa62-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2aa62-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2aa62-145">Minimum supported client</span></span><br/> | <span data-ttu-id="2aa62-146">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="2aa62-146">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2aa62-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2aa62-147">Minimum supported server</span></span><br/> | <span data-ttu-id="2aa62-148">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2aa62-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2aa62-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2aa62-149">Namespace</span></span><br/>                | <span data-ttu-id="2aa62-150">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="2aa62-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="2aa62-151">MOF</span><span class="sxs-lookup"><span data-stu-id="2aa62-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2aa62-152"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2aa62-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2aa62-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2aa62-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aa62-154">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="2aa62-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
