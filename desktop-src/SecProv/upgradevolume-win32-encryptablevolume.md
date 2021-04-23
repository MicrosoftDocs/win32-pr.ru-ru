---
description: Обновляет том из формата Windows Vista до формата Windows 7.
ms.assetid: d6654e92-8176-471b-b8e5-815dd9512240
title: Метод Упградеволуме класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UpgradeVolume
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 6769e8a4a480becc5a5584826f60cdb85f8b90e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991017"
---
# <a name="upgradevolume-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="cac78-103">Метод Упградеволуме \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="cac78-103">UpgradeVolume method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="cac78-104">Метод **упградеволуме** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) обновляет том из формата Windows Vista до формата Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cac78-104">The **UpgradeVolume** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class upgrades a volume from the Windows Vista format to the Windows 7 format.</span></span> <span data-ttu-id="cac78-105">Это необратимая операция.</span><span class="sxs-lookup"><span data-stu-id="cac78-105">This is a nonreversible operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="cac78-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cac78-106">Syntax</span></span>


```mof
uint32 UpgradeVolume();
```



## <a name="parameters"></a><span data-ttu-id="cac78-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cac78-107">Parameters</span></span>

<span data-ttu-id="cac78-108">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="cac78-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cac78-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cac78-109">Return value</span></span>

<span data-ttu-id="cac78-110">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cac78-110">Type: **uint32**</span></span>

<span data-ttu-id="cac78-111">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="cac78-111">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="cac78-112">Если том уже разблокирован и другие ошибки не возникают, этот метод возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="cac78-112">If the volume is already unlocked and no other errors occur, this method returns zero.</span></span>



| <span data-ttu-id="cac78-113">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="cac78-113">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="cac78-114">Описание</span><span class="sxs-lookup"><span data-stu-id="cac78-114">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cac78-115"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="cac78-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="cac78-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="cac78-116">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="cac78-117"><dt>**Д \_ INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span><span class="sxs-lookup"><span data-stu-id="cac78-117"><dt>**E\_INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span></span> </dl>            | <span data-ttu-id="cac78-118">Один или несколько аргументов являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="cac78-118">One or more of the arguments are not valid.</span></span><br/>                                       |
| <dl> <span data-ttu-id="cac78-119"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="cac78-119"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="cac78-120">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="cac78-120">The volume is locked.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="cac78-121"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="cac78-121"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="cac78-122">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="cac78-122">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="cac78-123">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="cac78-123">Add a key protector to enable BitLocker.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="cac78-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cac78-124">Remarks</span></span>

<span data-ttu-id="cac78-125">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="cac78-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="cac78-126">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="cac78-126">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="cac78-127">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="cac78-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="cac78-128">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="cac78-128">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cac78-129">Требования</span><span class="sxs-lookup"><span data-stu-id="cac78-129">Requirements</span></span>



| <span data-ttu-id="cac78-130">Требование</span><span class="sxs-lookup"><span data-stu-id="cac78-130">Requirement</span></span> | <span data-ttu-id="cac78-131">Значение</span><span class="sxs-lookup"><span data-stu-id="cac78-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cac78-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cac78-132">Minimum supported client</span></span><br/> | <span data-ttu-id="cac78-133">Windows 7 Корпоративная, \[ только классические приложения Windows 7 Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="cac78-133">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cac78-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cac78-134">Minimum supported server</span></span><br/> | <span data-ttu-id="cac78-135">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="cac78-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cac78-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cac78-136">Namespace</span></span><br/>                | <span data-ttu-id="cac78-137">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="cac78-137">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="cac78-138">MOF</span><span class="sxs-lookup"><span data-stu-id="cac78-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cac78-139"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cac78-139"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cac78-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cac78-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cac78-141">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="cac78-141">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
