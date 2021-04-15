---
description: Возвращает числовой пароль для данного предохранителя ключа.
ms.assetid: 5c4663fb-285d-471c-b355-82d553a7e686
title: Метод Жеткэйпротекторнумерикалпассворд класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 73a6c774386cd88195074092323969d97f4d7563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682556"
---
# <a name="getkeyprotectornumericalpassword-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="aba24-103">Метод Жеткэйпротекторнумерикалпассворд \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="aba24-103">GetKeyProtectorNumericalPassword method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="aba24-104">Метод **жеткэйпротекторнумерикалпассворд** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) извлекает числовой пароль для данного предохранителя ключа соответствующего типа.</span><span class="sxs-lookup"><span data-stu-id="aba24-104">The **GetKeyProtectorNumericalPassword** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the numerical password for a given key protector of the appropriate type.</span></span>

<span data-ttu-id="aba24-105">Идентификатор предохранителя ключа должен ссылаться на предохранитель ключа типа "числовой пароль".</span><span class="sxs-lookup"><span data-stu-id="aba24-105">The key protector identifier must refer to a key protector of type "Numerical Password".</span></span>

## <a name="syntax"></a><span data-ttu-id="aba24-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aba24-106">Syntax</span></span>


```mof
uint32 GetKeyProtectorNumericalPassword(
  [in]  string VolumeKeyProtectorID,
  [out] string NumericalPassword
);
```



## <a name="parameters"></a><span data-ttu-id="aba24-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="aba24-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aba24-108">*Волумекэйпротекторид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aba24-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aba24-109">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="aba24-109">Type: **string**</span></span>

<span data-ttu-id="aba24-110">Уникальный строковый идентификатор, используемый для управления предохранителем ключа зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="aba24-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="aba24-111">*Нумерикалпассворд* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="aba24-111">*NumericalPassword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aba24-112">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="aba24-112">Type: **string**</span></span>

<span data-ttu-id="aba24-113">Строка, представляющая пароль, который можно использовать для разблокировки соответствующего тома.</span><span class="sxs-lookup"><span data-stu-id="aba24-113">A string that represents the password that can be used to unlock the corresponding volume.</span></span>

<span data-ttu-id="aba24-114">Числовой пароль — 48 цифр.</span><span class="sxs-lookup"><span data-stu-id="aba24-114">The numerical password is 48 digits.</span></span> <span data-ttu-id="aba24-115">Эти цифры делятся на 8 групп из 6 цифр, а последняя цифра в каждой группе указывает на значение контрольной суммы для группы.</span><span class="sxs-lookup"><span data-stu-id="aba24-115">These digits are divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="aba24-116">Предполагая, что группа из шести цифр помечена как x1, x2, X3, X4, x5 и X6, контрольная сумма X6 вычисляется как – x1 + x2 – X3 + X4 – x5 mod 11.</span><span class="sxs-lookup"><span data-stu-id="aba24-116">Assuming that a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="aba24-117">Группы цифр разделяются дефисом.</span><span class="sxs-lookup"><span data-stu-id="aba24-117">The groups of digits are separated by a hyphen.</span></span> <span data-ttu-id="aba24-118">Таким образом, "XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX" — это формат возвращаемого пароля.</span><span class="sxs-lookup"><span data-stu-id="aba24-118">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" is the format of the returned password.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aba24-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aba24-119">Return value</span></span>

<span data-ttu-id="aba24-120">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aba24-120">Type: **uint32**</span></span>

<span data-ttu-id="aba24-121">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="aba24-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="aba24-122">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="aba24-122">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="aba24-123">Описание</span><span class="sxs-lookup"><span data-stu-id="aba24-123">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aba24-124"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="aba24-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="aba24-125">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="aba24-125">The method was successful.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="aba24-126"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="aba24-126"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="aba24-127">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="aba24-127">The volume is locked.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="aba24-128"><dt>**Д \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="aba24-128"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="aba24-129">Параметр *волумекэйпротекторид* не ссылается на предохранитель ключа типа "числовой пароль".</span><span class="sxs-lookup"><span data-stu-id="aba24-129">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password".</span></span><br/> |
| <dl> <span data-ttu-id="aba24-130"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="aba24-130"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="aba24-131">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="aba24-131">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="aba24-132">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="aba24-132">Add a key protector to enable BitLocker.</span></span> <br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="aba24-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aba24-133">Remarks</span></span>

<span data-ttu-id="aba24-134">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="aba24-134">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="aba24-135">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="aba24-135">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="aba24-136">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="aba24-136">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="aba24-137">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="aba24-137">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aba24-138">Требования</span><span class="sxs-lookup"><span data-stu-id="aba24-138">Requirements</span></span>



| <span data-ttu-id="aba24-139">Требование</span><span class="sxs-lookup"><span data-stu-id="aba24-139">Requirement</span></span> | <span data-ttu-id="aba24-140">Значение</span><span class="sxs-lookup"><span data-stu-id="aba24-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aba24-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aba24-141">Minimum supported client</span></span><br/> | <span data-ttu-id="aba24-142">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="aba24-142">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="aba24-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aba24-143">Minimum supported server</span></span><br/> | <span data-ttu-id="aba24-144">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aba24-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aba24-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="aba24-145">Namespace</span></span><br/>                | <span data-ttu-id="aba24-146">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="aba24-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="aba24-147">MOF</span><span class="sxs-lookup"><span data-stu-id="aba24-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aba24-148"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aba24-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aba24-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aba24-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aba24-150">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="aba24-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
