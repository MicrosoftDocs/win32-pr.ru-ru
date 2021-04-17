---
description: Извлекает отображаемое имя, используемое для распознавания данного предохранителя ключа.
ms.assetid: 2f310494-7873-4d05-836e-f09e5784571b
title: Метод Жеткэйпротекторфриендлинаме класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorFriendlyName
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 45da91d08aadda2d1a25254fe36d0d266b7c53d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684062"
---
# <a name="getkeyprotectorfriendlyname-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="73fd1-103">Метод Жеткэйпротекторфриендлинаме \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="73fd1-103">GetKeyProtectorFriendlyName method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="73fd1-104">Метод **жеткэйпротекторфриендлинаме** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) извлекает отображаемое имя, используемое для распознавания данного предохранителя ключа.</span><span class="sxs-lookup"><span data-stu-id="73fd1-104">The **GetKeyProtectorFriendlyName** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the display name used to identify a given key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="73fd1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73fd1-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorFriendlyName(
  [in]  string VolumeKeyProtectorID,
  [out] string FriendlyName
);
```



## <a name="parameters"></a><span data-ttu-id="73fd1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="73fd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73fd1-107">*Волумекэйпротекторид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="73fd1-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73fd1-108">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="73fd1-108">Type: **string**</span></span>

<span data-ttu-id="73fd1-109">Уникальный строковый идентификатор, используемый для управления предохранителем ключа зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="73fd1-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="73fd1-110">*FriendlyName* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="73fd1-110">*FriendlyName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73fd1-111">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="73fd1-111">Type: **string**</span></span>

<span data-ttu-id="73fd1-112">Строка, содержащая указанное пользователем имя, используемое для распознавания данного предохранителя ключа.</span><span class="sxs-lookup"><span data-stu-id="73fd1-112">A string that contains the user-specified name used to identify the given key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73fd1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73fd1-113">Return value</span></span>

<span data-ttu-id="73fd1-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73fd1-114">Type: **uint32**</span></span>

<span data-ttu-id="73fd1-115">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="73fd1-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="73fd1-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="73fd1-116">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="73fd1-117">Описание</span><span class="sxs-lookup"><span data-stu-id="73fd1-117">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="73fd1-118"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="73fd1-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="73fd1-119">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="73fd1-119">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="73fd1-120"><dt>**Д \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="73fd1-120"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="73fd1-121">Параметр *волумекэйпротекторид* не ссылается на допустимый предохранитель ключа.</span><span class="sxs-lookup"><span data-stu-id="73fd1-121">The *VolumeKeyProtectorID* parameter does not refer to a valid key protector.</span></span><br/>     |
| <dl> <span data-ttu-id="73fd1-122"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="73fd1-122"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="73fd1-123">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="73fd1-123">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="73fd1-124">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="73fd1-124">Add a key protector to enable BitLocker.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="73fd1-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73fd1-125">Remarks</span></span>

<span data-ttu-id="73fd1-126">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="73fd1-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="73fd1-127">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="73fd1-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="73fd1-128">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="73fd1-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="73fd1-129">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="73fd1-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="73fd1-130">Требования</span><span class="sxs-lookup"><span data-stu-id="73fd1-130">Requirements</span></span>



| <span data-ttu-id="73fd1-131">Требование</span><span class="sxs-lookup"><span data-stu-id="73fd1-131">Requirement</span></span> | <span data-ttu-id="73fd1-132">Значение</span><span class="sxs-lookup"><span data-stu-id="73fd1-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73fd1-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73fd1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="73fd1-134">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="73fd1-134">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="73fd1-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73fd1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="73fd1-136">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="73fd1-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="73fd1-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="73fd1-137">Namespace</span></span><br/>                | <span data-ttu-id="73fd1-138">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="73fd1-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="73fd1-139">MOF</span><span class="sxs-lookup"><span data-stu-id="73fd1-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73fd1-140"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73fd1-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73fd1-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73fd1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73fd1-142">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="73fd1-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
