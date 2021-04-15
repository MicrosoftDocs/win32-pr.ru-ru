---
description: Отключает или приостанавливает все предохранители ключей, связанные с этим томом.
ms.assetid: 19eed858-a116-4ec8-937a-2eea7aadbdc6
title: Метод Дисаблекэйпротекторс класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1de392c50f6665d793883582e2679cd502efbe37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683476"
---
# <a name="disablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="742d1-103">Метод Дисаблекэйпротекторс \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="742d1-103">DisableKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="742d1-104">Метод **дисаблекэйпротекторс** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) отключает или приостанавливает все предохранители ключа, связанные с этим томом.</span><span class="sxs-lookup"><span data-stu-id="742d1-104">The **DisableKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class disables or suspends all key protectors associated with this volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="742d1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="742d1-105">Syntax</span></span>


```mof
uint32 DisableKeyProtectors(
  [in, optional] uint32 DisableCount
);
```



## <a name="parameters"></a><span data-ttu-id="742d1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="742d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="742d1-107">*Дисаблекаунт* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="742d1-107">*DisableCount* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="742d1-108">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="742d1-108">Type: **uint32**</span></span>

<span data-ttu-id="742d1-109">Целое число, указывающее количество перезагрузок, для которых предохранители ключа будут отключены.</span><span class="sxs-lookup"><span data-stu-id="742d1-109">Integer that specifies the number of reboots for which the key protectors will be disabled.</span></span> <span data-ttu-id="742d1-110">Этот параметр доступен только на томах ОС.</span><span class="sxs-lookup"><span data-stu-id="742d1-110">This parameter is only available on OS volumes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="742d1-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="742d1-111">Return value</span></span>

<span data-ttu-id="742d1-112">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="742d1-112">Type: **uint32**</span></span>

<span data-ttu-id="742d1-113">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="742d1-113">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="742d1-114">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="742d1-114">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="742d1-115">Описание</span><span class="sxs-lookup"><span data-stu-id="742d1-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="742d1-116"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="742d1-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="742d1-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="742d1-117">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="742d1-118"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="742d1-118"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="742d1-119">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="742d1-119">The volume is locked.</span></span><br/>      |



 

## <a name="security-considerations"></a><span data-ttu-id="742d1-120">Соображения безопасности</span><span class="sxs-lookup"><span data-stu-id="742d1-120">Security Considerations</span></span>

<span data-ttu-id="742d1-121">Этот метод предоставляет ключ шифрования тома в открытом состоянии на жестком диске, отключив защиту тома.</span><span class="sxs-lookup"><span data-stu-id="742d1-121">This method exposes the volume's encryption key in the clear on the hard disk, turning off any volume protection.</span></span> <span data-ttu-id="742d1-122">Мы советуем использовать пароль или ключ шифрования в виде открытого текста.</span><span class="sxs-lookup"><span data-stu-id="742d1-122">We recommend against having any password or encryption key in plaintext.</span></span>

## <a name="remarks"></a><span data-ttu-id="742d1-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="742d1-123">Remarks</span></span>

<span data-ttu-id="742d1-124">Новые предохранители ключа можно добавлять, даже если предохранители ключей отключены или приостановлены.</span><span class="sxs-lookup"><span data-stu-id="742d1-124">New key protectors can be added even when key protectors are disabled or suspended.</span></span> <span data-ttu-id="742d1-125">Эти предохранители ключа останутся отключенными, если не будет вызван [**енаблекэйпротекторс**](enablekeyprotectors-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="742d1-125">These key protectors will remain disabled unless [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) is called.</span></span>

<span data-ttu-id="742d1-126">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="742d1-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="742d1-127">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="742d1-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="742d1-128">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="742d1-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="742d1-129">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="742d1-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="742d1-130">Требования</span><span class="sxs-lookup"><span data-stu-id="742d1-130">Requirements</span></span>



| <span data-ttu-id="742d1-131">Требование</span><span class="sxs-lookup"><span data-stu-id="742d1-131">Requirement</span></span> | <span data-ttu-id="742d1-132">Значение</span><span class="sxs-lookup"><span data-stu-id="742d1-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="742d1-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="742d1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="742d1-134">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="742d1-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="742d1-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="742d1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="742d1-136">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="742d1-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="742d1-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="742d1-137">Namespace</span></span><br/>                | <span data-ttu-id="742d1-138">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="742d1-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="742d1-139">MOF</span><span class="sxs-lookup"><span data-stu-id="742d1-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="742d1-140"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="742d1-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="742d1-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="742d1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="742d1-142">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="742d1-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="742d1-143">**енаблекэйпротекторс**</span><span class="sxs-lookup"><span data-stu-id="742d1-143">**EnableKeyProtectors**</span></span>](enablekeyprotectors-win32-encryptablevolume.md)
</dt> </dl>

 

 
