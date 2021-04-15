---
description: Определяет, расположен ли том на диске, поддерживающем или поддерживающем шифрование оборудования.
ms.assetid: C6007BC4-71CD-404A-A0E9-D9662906151F
title: Метод Жесардваринкриптионстатус класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareEncryptionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2f48bb7115d19779f437a849078238cee967f2d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682558"
---
# <a name="gethardwareencryptionstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="76564-103">Метод Жесардваринкриптионстатус \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="76564-103">GetHardwareEncryptionStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="76564-104">Метод **жесардваринкриптионстатус** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) определяет, расположен ли том на диске, поддерживающем или поддерживающем шифрование оборудования.</span><span class="sxs-lookup"><span data-stu-id="76564-104">The **GetHardwareEncryptionStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class determines whether the volume is located on a drive that supports or can support hardware encryption.</span></span>

## <a name="syntax"></a><span data-ttu-id="76564-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76564-105">Syntax</span></span>


```mof
uint32 GetHardwareEncryptionStatus(
  [out] uint32 HardwareEncryptionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="76564-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="76564-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76564-107">*Хардваринкриптионстатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="76564-107">*HardwareEncryptionStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76564-108">Указывает, может ли диск поддерживать шифрование оборудования.</span><span class="sxs-lookup"><span data-stu-id="76564-108">Specifies whether the drive can support hardware encryption.</span></span> <span data-ttu-id="76564-109">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="76564-109">This can be one of the following values.</span></span>



| <span data-ttu-id="76564-110">Значение</span><span class="sxs-lookup"><span data-stu-id="76564-110">Value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="76564-111">Значение</span><span class="sxs-lookup"><span data-stu-id="76564-111">Meaning</span></span>                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="Not_supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <span data-ttu-id="76564-112"><dt>**Не поддерживается**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="76564-112"><dt>**Not supported**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="76564-113">Аппаратное шифрование не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="76564-113">Hardware encryption is not supported.</span></span><br/>    |
| <span id="No_protection"></span><span id="no_protection"></span><span id="NO_PROTECTION"></span><dl> <span data-ttu-id="76564-114"><dt>**Нет защиты**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="76564-114"><dt>**No protection**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="76564-115">Шифрование диска не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="76564-115">Drive encryption is not supported.</span></span><br/>       |
| <span id="Uses_software"></span><span id="uses_software"></span><span id="USES_SOFTWARE"></span><dl> <span data-ttu-id="76564-116"><dt>**Использует программное обеспечение**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="76564-116"><dt>**Uses software**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="76564-117">Метод шифрования основан на программном обеспечении.</span><span class="sxs-lookup"><span data-stu-id="76564-117">The encryption method is software-based.</span></span><br/> |
| <span id="Uses_hardware"></span><span id="uses_hardware"></span><span id="USES_HARDWARE"></span><dl> <span data-ttu-id="76564-118"><dt>**Использует оборудование**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="76564-118"><dt>**Uses hardware**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="76564-119">Диск поддерживает аппаратное шифрование.</span><span class="sxs-lookup"><span data-stu-id="76564-119">The drive supports hardware encryption.</span></span><br/>  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76564-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76564-120">Return value</span></span>

<span data-ttu-id="76564-121">Эта функция возвращает ноль (0), если том совместим с аппаратным шифрованием BitLocker.</span><span class="sxs-lookup"><span data-stu-id="76564-121">This function returns zero (0) if the volume is compatible with BitLocker hardware encryption.</span></span> <span data-ttu-id="76564-122">В противном случае функция возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="76564-122">Otherwise, the function returns an error.</span></span>



| <span data-ttu-id="76564-123">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="76564-123">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="76564-124">Описание</span><span class="sxs-lookup"><span data-stu-id="76564-124">Description</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="76564-125"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="76564-125"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="76564-126">Том совместим с аппаратным шифрованием BitLocker.</span><span class="sxs-lookup"><span data-stu-id="76564-126">The volume is compatible with BitLocker hardware encryption.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="76564-127">Требования</span><span class="sxs-lookup"><span data-stu-id="76564-127">Requirements</span></span>



| <span data-ttu-id="76564-128">Требование</span><span class="sxs-lookup"><span data-stu-id="76564-128">Requirement</span></span> | <span data-ttu-id="76564-129">Значение</span><span class="sxs-lookup"><span data-stu-id="76564-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76564-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76564-130">Minimum supported client</span></span><br/> | <span data-ttu-id="76564-131">Windows 8 Корпоративная, \[ только классические приложения Windows 8 Pro\]</span><span class="sxs-lookup"><span data-stu-id="76564-131">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="76564-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76564-132">Minimum supported server</span></span><br/> | <span data-ttu-id="76564-133">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="76564-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="76564-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="76564-134">Namespace</span></span><br/>                | <span data-ttu-id="76564-135">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="76564-135">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="76564-136">MOF</span><span class="sxs-lookup"><span data-stu-id="76564-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76564-137"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="76564-137"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76564-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76564-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76564-139">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="76564-139">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




