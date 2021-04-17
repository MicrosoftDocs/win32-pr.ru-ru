---
description: Изменяет внешний ключ, связанный с зашифрованным томом.
ms.assetid: 14c7e643-f685-40bb-be86-aabc5b883d7e
title: Метод Чанжеекстерналкэй класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangeExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7441666ded1acc2234df84fc98ce6d02a117167d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684077"
---
# <a name="changeexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="63a3d-103">Метод Чанжеекстерналкэй \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="63a3d-103">ChangeExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="63a3d-104">Метод **чанжеекстерналкэй** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) изменяет внешний ключ, связанный с зашифрованным томом.</span><span class="sxs-lookup"><span data-stu-id="63a3d-104">The **ChangeExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class changes an external key that is associated with an encrypted volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="63a3d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63a3d-105">Syntax</span></span>


```mof
uint32 ChangeExternalKey(
  [in]           string VolumeKeyProtectorID,
  [in, optional] uint8   NewExternalKey[],
  [out]          string NewVolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="63a3d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="63a3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63a3d-107">*Волумекэйпротекторид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63a3d-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63a3d-108">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="63a3d-108">Type: **string**</span></span>

<span data-ttu-id="63a3d-109">Уникальный строковый идентификатор, используемый для управления предохранителем ключа зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="63a3d-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

 <span data-ttu-id="63a3d-110">*Невекстерналкэй* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="63a3d-110">*NewExternalKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="63a3d-111">Тип: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="63a3d-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="63a3d-112">Массив байтов, указывающий 256-разрядный внешний ключ, используемый для разблокировки тома.</span><span class="sxs-lookup"><span data-stu-id="63a3d-112">An array of bytes that specifies the 256-bit external key used to unlock the volume.</span></span>

</dd> <dt>

<span data-ttu-id="63a3d-113">*Невволумекэйпротекторид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="63a3d-113">*NewVolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63a3d-114">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="63a3d-114">Type: **string**</span></span>

<span data-ttu-id="63a3d-115">Обновленный уникальный идентификатор строки, используемый для управления предохранителем ключа зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="63a3d-115">An updated unique string identifier that is used to manage an encrypted volume key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63a3d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63a3d-116">Return value</span></span>

<span data-ttu-id="63a3d-117">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63a3d-117">Type: **uint32**</span></span>

<span data-ttu-id="63a3d-118">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="63a3d-118">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="63a3d-119">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="63a3d-119">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="63a3d-120">Описание</span><span class="sxs-lookup"><span data-stu-id="63a3d-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="63a3d-121"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="63a3d-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="63a3d-122">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="63a3d-122">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="63a3d-123"><dt>**Д \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="63a3d-123"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                    | <span data-ttu-id="63a3d-124">Параметр *невекстерналкэй* не является массивом размером 32.</span><span class="sxs-lookup"><span data-stu-id="63a3d-124">The *NewExternalKey* parameter is not an array of size 32.</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="63a3d-125"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="63a3d-125"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>           | <span data-ttu-id="63a3d-126">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="63a3d-126">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="63a3d-127"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="63a3d-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="63a3d-128">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="63a3d-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="63a3d-129">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="63a3d-129">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="63a3d-130"><dt>**ФВЕ \_ E \_ загрузочная \_ кддвд**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="63a3d-130"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>          | <span data-ttu-id="63a3d-131">На этом компьютере находится загрузочный компакт-диск или DVD-диск.</span><span class="sxs-lookup"><span data-stu-id="63a3d-131">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="63a3d-132">Удалите компакт-диск или диск DVD и перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="63a3d-132">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="63a3d-133"><dt>**ФВЕ \_ \_ \_ Не \_ найден предохранитель "E**</dt> <dt>" 2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="63a3d-133"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="63a3d-134">Указанный предохранитель ключа не существует на томе.</span><span class="sxs-lookup"><span data-stu-id="63a3d-134">The provided key protector does not exist on the volume.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="63a3d-135"><dt>**ФВЕ \_ \_Недопустимый \_ \_ тип предохранителя**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="63a3d-135"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl> | <span data-ttu-id="63a3d-136">Параметр *волумекэйпротекторид* не ссылается на предохранитель ключа типа "числовой пароль" или "внешний ключ".</span><span class="sxs-lookup"><span data-stu-id="63a3d-136">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="63a3d-137">Используйте метод [**протекткэйвиснумерикалпассворд**](protectkeywithnumericalpassword-win32-encryptablevolume.md) или [**протекткэйвисекстерналкэй**](protectkeywithexternalkey-win32-encryptablevolume.md) для создания предохранителя ключа соответствующего типа.</span><span class="sxs-lookup"><span data-stu-id="63a3d-137">Use either the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) or [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to create a key protector of the appropriate type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="63a3d-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63a3d-138">Remarks</span></span>

<span data-ttu-id="63a3d-139">Этот метод можно использовать для изменения внешнего ключа для любого предохранителя ключа, использующего внешний ключ.</span><span class="sxs-lookup"><span data-stu-id="63a3d-139">This method can be used to change the external key for any key protector that uses an external key.</span></span>

## <a name="requirements"></a><span data-ttu-id="63a3d-140">Требования</span><span class="sxs-lookup"><span data-stu-id="63a3d-140">Requirements</span></span>



| <span data-ttu-id="63a3d-141">Требование</span><span class="sxs-lookup"><span data-stu-id="63a3d-141">Requirement</span></span> | <span data-ttu-id="63a3d-142">Значение</span><span class="sxs-lookup"><span data-stu-id="63a3d-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63a3d-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63a3d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="63a3d-144">Windows 7 Корпоративная, \[ только классические приложения Windows 7 Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="63a3d-144">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="63a3d-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63a3d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="63a3d-146">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="63a3d-146">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="63a3d-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="63a3d-147">Namespace</span></span><br/>                | <span data-ttu-id="63a3d-148">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="63a3d-148">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="63a3d-149">MOF</span><span class="sxs-lookup"><span data-stu-id="63a3d-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63a3d-150"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63a3d-150"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63a3d-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63a3d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63a3d-152">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="63a3d-152">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




