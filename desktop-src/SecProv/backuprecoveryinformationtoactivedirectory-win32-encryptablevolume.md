---
description: Создает резервную копию данных восстановления в Active Directory.
ms.assetid: 664562b3-5679-4185-8bbc-5d5350494707
title: Метод Баккупрековеринформатионтоактиведиректори класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.BackupRecoveryInformationToActiveDirectory
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a04901139aa46f42e06eaea1c91af0e3bac202e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684572"
---
# <a name="backuprecoveryinformationtoactivedirectory-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="9174c-103">Метод Баккупрековеринформатионтоактиведиректори \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="9174c-103">BackupRecoveryInformationToActiveDirectory method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="9174c-104">Метод **баккупрековеринформатионтоактиведиректори** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) создает резервные копии данных восстановления в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9174c-104">The **BackupRecoveryInformationToActiveDirectory** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class backs up recovery data to Active Directory.</span></span> <span data-ttu-id="9174c-105">Этот метод требует наличия на томе средства защиты числового пароля.</span><span class="sxs-lookup"><span data-stu-id="9174c-105">This method requires a numerical password protector to be present on the volume.</span></span> <span data-ttu-id="9174c-106">Групповая политика также необходимо настроить для включения резервного копирования сведений о восстановлении в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9174c-106">Group Policy must also be configured to enable backup of recovery information to Active Directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="9174c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9174c-107">Syntax</span></span>


```mof
uint32 BackupRecoveryInformationToActiveDirectory(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="9174c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9174c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9174c-109">*Волумекэйпротекторид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9174c-109">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9174c-110">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="9174c-110">Type: **string**</span></span>

<span data-ttu-id="9174c-111">Уникальный строковый идентификатор, используемый для управления предохранителем ключа зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="9174c-111">A unique string identifier used to manage an encrypted volume key protector.</span></span> <span data-ttu-id="9174c-112">Предохранитель ключа должен быть числовым предохранителем пароля.</span><span class="sxs-lookup"><span data-stu-id="9174c-112">This key protector must be a numerical password protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9174c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9174c-113">Return value</span></span>

<span data-ttu-id="9174c-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9174c-114">Type: **uint32**</span></span>

<span data-ttu-id="9174c-115">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="9174c-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="9174c-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="9174c-116">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="9174c-117">Описание</span><span class="sxs-lookup"><span data-stu-id="9174c-117">Description</span></span>                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9174c-118"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="9174c-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="9174c-119">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="9174c-119">The method was successful.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="9174c-120"><dt>**С \_ FALSE**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="9174c-120"><dt>**S\_FALSE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                                         | <span data-ttu-id="9174c-121">Групповая политика не позволяет Active Directory хранения сведений о восстановлении.</span><span class="sxs-lookup"><span data-stu-id="9174c-121">Group Policy does not permit the storage of recovery information to Active Directory.</span></span><br/>                         |
| <dl> <span data-ttu-id="9174c-122"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="9174c-122"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="9174c-123">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="9174c-123">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="9174c-124">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9174c-124">Add a key protector to enable BitLocker.</span></span> <br/>                             |
| <dl> <span data-ttu-id="9174c-125"><dt>**ФВЕ \_ \_Недопустимый \_ \_ тип предохранителя**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="9174c-125"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl> | <span data-ttu-id="9174c-126">Указанный предохранитель ключа не является ключом числового предохранителя ключа.</span><span class="sxs-lookup"><span data-stu-id="9174c-126">The specified key protector is not a numerical key protector.</span></span> <span data-ttu-id="9174c-127">Необходимо ввести средство защиты числового пароля.</span><span class="sxs-lookup"><span data-stu-id="9174c-127">You must enter a numerical password protector.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="9174c-128">Требования</span><span class="sxs-lookup"><span data-stu-id="9174c-128">Requirements</span></span>



| <span data-ttu-id="9174c-129">Требование</span><span class="sxs-lookup"><span data-stu-id="9174c-129">Requirement</span></span> | <span data-ttu-id="9174c-130">Значение</span><span class="sxs-lookup"><span data-stu-id="9174c-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9174c-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9174c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9174c-132">Windows 7 Корпоративная, \[ только классические приложения Windows 7 Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="9174c-132">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9174c-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9174c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9174c-134">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9174c-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9174c-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9174c-135">Namespace</span></span><br/>                | <span data-ttu-id="9174c-136">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="9174c-136">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="9174c-137">MOF</span><span class="sxs-lookup"><span data-stu-id="9174c-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9174c-138"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9174c-138"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9174c-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9174c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9174c-140">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="9174c-140">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




