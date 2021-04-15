---
description: Извлекает внешний ключ для данного предохранителя ключа.
ms.assetid: d2b5e7d4-97c1-4d7f-a155-b5cdca2b552e
title: Метод Жеткэйпротекторекстерналкэй класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7125038a9e93803f7f8773ce5da078983a5a544c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262994"
---
# <a name="getkeyprotectorexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="c9bf3-103">Метод Жеткэйпротекторекстерналкэй \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="c9bf3-103">GetKeyProtectorExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="c9bf3-104">Метод **жеткэйпротекторекстерналкэй** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) извлекает внешний ключ для данного предохранителя ключа соответствующего типа.</span><span class="sxs-lookup"><span data-stu-id="c9bf3-104">The **GetKeyProtectorExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the external key for a given key protector of the appropriate type.</span></span>

<span data-ttu-id="c9bf3-105">Идентификатор предохранителя ключа должен ссылаться на предохранитель ключа типа "внешний ключ", "TPM, ПИН-код и ключ запуска", "TPM и ключ запуска".</span><span class="sxs-lookup"><span data-stu-id="c9bf3-105">The key protector identifier must refer to a key protector of type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="c9bf3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9bf3-106">Syntax</span></span>


```mof
uint32 GetKeyProtectorExternalKey(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a><span data-ttu-id="c9bf3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9bf3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9bf3-108">*Волумекэйпротекторид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c9bf3-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9bf3-109">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="c9bf3-109">Type: **string**</span></span>

<span data-ttu-id="c9bf3-110">Уникальный строковый идентификатор, используемый для управления предохранителем ключа зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="c9bf3-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="c9bf3-111">*Екстерналкэй* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c9bf3-111">*ExternalKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9bf3-112">Тип: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="c9bf3-112">Type: **uint8\[\]**</span></span>

<span data-ttu-id="c9bf3-113">Массив байтов, указывающий 256-разрядный внешний ключ, который можно использовать для разблокировки соответствующего тома.</span><span class="sxs-lookup"><span data-stu-id="c9bf3-113">An array of bytes that specifies the 256-bit external key that can be used to unlock the corresponding volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9bf3-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9bf3-114">Return value</span></span>

<span data-ttu-id="c9bf3-115">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9bf3-115">Type: **uint32**</span></span>

<span data-ttu-id="c9bf3-116">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="c9bf3-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="c9bf3-117">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="c9bf3-117">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="c9bf3-118">Описание</span><span class="sxs-lookup"><span data-stu-id="c9bf3-118">Description</span></span>                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c9bf3-119"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c9bf3-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="c9bf3-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="c9bf3-120">The method was successful.</span></span><br/>                                                                                                                                  |
| <dl> <span data-ttu-id="c9bf3-121"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="c9bf3-121"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="c9bf3-122">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="c9bf3-122">The volume is locked.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="c9bf3-123"><dt>**Д \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="c9bf3-123"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="c9bf3-124">Параметр *волумекэйпротекторид* не ссылается на предохранитель ключа типа "внешний ключ", "TPM, ПИН-код и ключ запуска", "TPM и ключ запуска".</span><span class="sxs-lookup"><span data-stu-id="c9bf3-124">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span><br/> |
| <dl> <span data-ttu-id="c9bf3-125"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="c9bf3-125"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="c9bf3-126">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="c9bf3-126">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="c9bf3-127">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c9bf3-127">Add a key protector to enable BitLocker.</span></span> <br/>                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="c9bf3-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9bf3-128">Remarks</span></span>

<span data-ttu-id="c9bf3-129">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="c9bf3-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c9bf3-130">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="c9bf3-130">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="c9bf3-131">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="c9bf3-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c9bf3-132">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="c9bf3-132">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9bf3-133">Требования</span><span class="sxs-lookup"><span data-stu-id="c9bf3-133">Requirements</span></span>



| <span data-ttu-id="c9bf3-134">Требование</span><span class="sxs-lookup"><span data-stu-id="c9bf3-134">Requirement</span></span> | <span data-ttu-id="c9bf3-135">Значение</span><span class="sxs-lookup"><span data-stu-id="c9bf3-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9bf3-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9bf3-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c9bf3-137">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="c9bf3-137">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c9bf3-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9bf3-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c9bf3-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c9bf3-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c9bf3-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c9bf3-140">Namespace</span></span><br/>                | <span data-ttu-id="c9bf3-141">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="c9bf3-141">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="c9bf3-142">MOF</span><span class="sxs-lookup"><span data-stu-id="c9bf3-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9bf3-143"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9bf3-143"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9bf3-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9bf3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9bf3-145">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="c9bf3-145">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
