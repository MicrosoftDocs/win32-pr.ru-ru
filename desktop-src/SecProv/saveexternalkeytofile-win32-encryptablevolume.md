---
description: Записывает внешний ключ, связанный с указанным предохранителем ключа тома, в системный, скрытый файл, который доступен только для чтения в указанной папке.
ms.assetid: 8d928f85-b392-4119-aebb-f16021eb5c6a
title: Метод Савикстерналкэйтофиле класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SaveExternalKeyToFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 879536940ff36a005e1936dffcd7821fff585a65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663800"
---
# <a name="saveexternalkeytofile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="4abf6-103">Метод Савикстерналкэйтофиле \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="4abf6-103">SaveExternalKeyToFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="4abf6-104">Метод **савикстерналкэйтофиле** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) записывает внешний ключ, связанный с указанным предохранителем ключа тома, в системный, скрытый файл, который доступен только для чтения в указанной папке.</span><span class="sxs-lookup"><span data-stu-id="4abf6-104">The **SaveExternalKeyToFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class writes the external key associated with the specified volume key protector to a system, hidden, read-only file in the specified folder.</span></span>

<span data-ttu-id="4abf6-105">Этот метод применим только для предохранителей ключа типа "внешний ключ" или "TPM и ключ запуска".</span><span class="sxs-lookup"><span data-stu-id="4abf6-105">This method is only applicable for key protectors of the type "External Key" or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="4abf6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4abf6-106">Syntax</span></span>


```mof
uint32 SaveExternalKeyToFile(
  [in] string VolumeKeyProtectorID,
  [in] string Path
);
```



## <a name="parameters"></a><span data-ttu-id="4abf6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4abf6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4abf6-108">*Волумекэйпротекторид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4abf6-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4abf6-109">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="4abf6-109">Type: **string**</span></span>

<span data-ttu-id="4abf6-110">Уникальный строковый идентификатор, используемый для управления предохранителем ключа зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="4abf6-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="4abf6-111">*Путь* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4abf6-111">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4abf6-112">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="4abf6-112">Type: **string**</span></span>

<span data-ttu-id="4abf6-113">Строка, содержащая том или расположение папки, в которой должен быть сохранен внешний ключ, связанный с указанным предохранителем ключа.</span><span class="sxs-lookup"><span data-stu-id="4abf6-113">A string that contains the volume or folder location where the external key associated with the specified key protector is to be saved.</span></span> <span data-ttu-id="4abf6-114">Этот путь не включает в себя имя файла, который является внутренним и может изменяться от версии к версии.</span><span class="sxs-lookup"><span data-stu-id="4abf6-114">This path does not include the name of the file, which is internal and may change from version to version.</span></span> <span data-ttu-id="4abf6-115">Чтобы получить имя файла, используйте **жетекстерналкэйфиленаме** .</span><span class="sxs-lookup"><span data-stu-id="4abf6-115">Use **GetExternalKeyFileName** to get the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4abf6-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4abf6-116">Return value</span></span>

<span data-ttu-id="4abf6-117">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4abf6-117">Type: **uint32**</span></span>

<span data-ttu-id="4abf6-118">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="4abf6-118">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="4abf6-119">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="4abf6-119">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="4abf6-120">Описание</span><span class="sxs-lookup"><span data-stu-id="4abf6-120">Description</span></span>                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4abf6-121"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="4abf6-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="4abf6-122">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="4abf6-122">The method was successful.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="4abf6-123"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="4abf6-123"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>  | <span data-ttu-id="4abf6-124">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="4abf6-124">The volume is locked.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="4abf6-125"><dt>**Д \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="4abf6-125"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>           | <span data-ttu-id="4abf6-126">Параметр *волумекэйпротекторид* не ссылается на предохранитель ключа типа "внешний ключ" или "TPM и ключ запуска".</span><span class="sxs-lookup"><span data-stu-id="4abf6-126">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "External Key" or "TPM And Startup Key".</span></span><br/>            |
| <dl> <span data-ttu-id="4abf6-127"><dt>**Ошибка при \_ ПУТЬ \_ не \_ найден**</dt> <dt>2147942403 (0x80070003)</dt></span><span class="sxs-lookup"><span data-stu-id="4abf6-127"><dt>**ERROR\_PATH\_NOT\_FOUND**</dt> <dt>2147942403 (0x80070003)</dt></span></span> </dl> | <span data-ttu-id="4abf6-128">Параметр *пути* не ссылается на допустимое расположение.</span><span class="sxs-lookup"><span data-stu-id="4abf6-128">The *Path* parameter does not refer to a valid location.</span></span><br/> <span data-ttu-id="4abf6-129">Убедитесь, что имя файла не включено в параметр *path* .</span><span class="sxs-lookup"><span data-stu-id="4abf6-129">Ensure that the file name is not included in the *Path* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="4abf6-130"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="4abf6-130"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>  | <span data-ttu-id="4abf6-131">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="4abf6-131">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="4abf6-132">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4abf6-132">Add a key protector to enable BitLocker.</span></span> <br/>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="4abf6-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4abf6-133">Remarks</span></span>

<span data-ttu-id="4abf6-134">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="4abf6-134">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4abf6-135">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4abf6-135">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="4abf6-136">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="4abf6-136">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4abf6-137">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="4abf6-137">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4abf6-138">Требования</span><span class="sxs-lookup"><span data-stu-id="4abf6-138">Requirements</span></span>



| <span data-ttu-id="4abf6-139">Требование</span><span class="sxs-lookup"><span data-stu-id="4abf6-139">Requirement</span></span> | <span data-ttu-id="4abf6-140">Значение</span><span class="sxs-lookup"><span data-stu-id="4abf6-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4abf6-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4abf6-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4abf6-142">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="4abf6-142">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4abf6-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4abf6-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4abf6-144">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4abf6-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4abf6-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4abf6-145">Namespace</span></span><br/>                | <span data-ttu-id="4abf6-146">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="4abf6-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="4abf6-147">MOF</span><span class="sxs-lookup"><span data-stu-id="4abf6-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4abf6-148"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4abf6-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4abf6-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4abf6-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4abf6-150">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="4abf6-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
