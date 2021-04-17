---
description: Возвращает имя файла, содержащего внешний ключ.
ms.assetid: c02d8dca-f30b-4ab5-a770-1ec6ac0b81c6
title: Метод Жетекстерналкэйфиленаме класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetExternalKeyFileName
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: bf8de41befa7414c9970ac451d34ee7c5f40dd84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682563"
---
# <a name="getexternalkeyfilename-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="01329-103">Метод Жетекстерналкэйфиленаме \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="01329-103">GetExternalKeyFileName method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="01329-104">Метод **жетекстерналкэйфиленаме** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) возвращает имя файла, содержащего внешний ключ, если этот внешний ключ сохранен в расположение файла с помощью метода [**савикстерналкэйтофиле**](saveexternalkeytofile-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="01329-104">The **GetExternalKeyFileName** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the name of the file that contains the external key, if this external key is saved to a file location by using the [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="01329-105">Этот метод применим только для предохранителей ключей типа "внешний ключ", "TPM, ПИН-код и ключ запуска" или "TPM и ключ запуска".</span><span class="sxs-lookup"><span data-stu-id="01329-105">This method is only applicable for key protectors of the type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="01329-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01329-106">Syntax</span></span>


```mof
uint32 GetExternalKeyFileName(
  [in]  string VolumeKeyProtectorID,
  [out] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="01329-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="01329-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01329-108">*Волумекэйпротекторид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01329-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01329-109">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="01329-109">Type: **string**</span></span>

<span data-ttu-id="01329-110">Уникальный строковый идентификатор, используемый для управления предохранителем ключа зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="01329-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="01329-111">*Имя файла* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="01329-111">*FileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01329-112">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="01329-112">Type: **string**</span></span>

<span data-ttu-id="01329-113">Строка, указывающая имя с расширением, но без пути к файлу для файла, содержащего внешний ключ.</span><span class="sxs-lookup"><span data-stu-id="01329-113">A string that specifies the name with extension but without the file path, of the file that contains the external key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01329-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01329-114">Return value</span></span>

<span data-ttu-id="01329-115">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01329-115">Type: **uint32**</span></span>

<span data-ttu-id="01329-116">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="01329-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="01329-117">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="01329-117">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="01329-118">Описание</span><span class="sxs-lookup"><span data-stu-id="01329-118">Description</span></span>                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="01329-119"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="01329-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="01329-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="01329-120">The method was successful.</span></span><br/>                                                                                                                                  |
| <dl> <span data-ttu-id="01329-121"><dt>**Д \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="01329-121"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="01329-122">Параметр *волумекэйпротекторид* не ссылается на предохранитель ключа типа "внешний ключ", "TPM, ПИН-код и ключ запуска", "TPM и ключ запуска".</span><span class="sxs-lookup"><span data-stu-id="01329-122">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span><br/> |
| <dl> <span data-ttu-id="01329-123"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="01329-123"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="01329-124">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="01329-124">The volume is locked.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="01329-125"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="01329-125"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="01329-126">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="01329-126">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="01329-127">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="01329-127">Add a key protector to enable BitLocker.</span></span> <br/>                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="01329-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01329-128">Remarks</span></span>

<span data-ttu-id="01329-129">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="01329-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="01329-130">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="01329-130">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="01329-131">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="01329-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="01329-132">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="01329-132">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="01329-133">Требования</span><span class="sxs-lookup"><span data-stu-id="01329-133">Requirements</span></span>



| <span data-ttu-id="01329-134">Требование</span><span class="sxs-lookup"><span data-stu-id="01329-134">Requirement</span></span> | <span data-ttu-id="01329-135">Значение</span><span class="sxs-lookup"><span data-stu-id="01329-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01329-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01329-136">Minimum supported client</span></span><br/> | <span data-ttu-id="01329-137">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="01329-137">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="01329-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01329-138">Minimum supported server</span></span><br/> | <span data-ttu-id="01329-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="01329-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="01329-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="01329-140">Namespace</span></span><br/>                | <span data-ttu-id="01329-141">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="01329-141">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="01329-142">MOF</span><span class="sxs-lookup"><span data-stu-id="01329-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01329-143"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01329-143"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01329-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01329-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01329-145">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="01329-145">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="01329-146">**савикстерналкэйтофиле**</span><span class="sxs-lookup"><span data-stu-id="01329-146">**SaveExternalKeyToFile**</span></span>](saveexternalkeytofile-win32-encryptablevolume.md)
</dt> </dl>

 

 
