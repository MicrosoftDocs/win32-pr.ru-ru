---
description: Приостанавливает шифрование или расшифровку тома.
ms.assetid: 3c365299-f0e1-480e-ad96-c91bb4108bb2
title: Метод Паусеконверсион класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PauseConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1c9756da2339a6a3d8e87466651f61c8ff3f83a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683922"
---
# <a name="pauseconversion-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="40428-103">Метод Паусеконверсион \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="40428-103">PauseConversion method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="40428-104">Метод **паусеконверсион** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) приостанавливает шифрование или расшифровку тома.</span><span class="sxs-lookup"><span data-stu-id="40428-104">The **PauseConversion** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class pauses the encryption or decryption of a volume.</span></span>

> [!Note]  
> <span data-ttu-id="40428-105">Если диск поддерживает шифрование оборудования, эта функция может приостановить операцию очистки, но не может приостановить шифрование на основе оборудования.</span><span class="sxs-lookup"><span data-stu-id="40428-105">If the disc supports hardware encryption, this function can pause a wiping operation but cannot pause hardware-based encryption.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="40428-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40428-106">Syntax</span></span>


```mof
uint32 PauseConversion();
```



## <a name="parameters"></a><span data-ttu-id="40428-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="40428-107">Parameters</span></span>

<span data-ttu-id="40428-108">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="40428-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="40428-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="40428-109">Return value</span></span>

<span data-ttu-id="40428-110">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40428-110">Type: **uint32**</span></span>

<span data-ttu-id="40428-111">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="40428-111">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="40428-112">Если этот метод используется на полностью зашифрованном или полностью расшифрованном томе или если шифрование или расшифровка уже приостановлены на томе, возвращается значение 0, предполагая, что другие ошибки не возникают.</span><span class="sxs-lookup"><span data-stu-id="40428-112">If this method is used on a fully encrypted or fully decrypted volume, or if encryption/decryption is already paused on the volume, 0 is returned assuming no other errors occur.</span></span>



| <span data-ttu-id="40428-113">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="40428-113">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="40428-114">Описание</span><span class="sxs-lookup"><span data-stu-id="40428-114">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="40428-115"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="40428-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="40428-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="40428-116">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="40428-117"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="40428-117"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="40428-118">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="40428-118">The volume is locked.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="40428-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="40428-119">Remarks</span></span>

<span data-ttu-id="40428-120">Если этот метод используется на томе, на котором выполняется шифрование или расшифровка, успешное выполнение этого метода приводит к тому, что [**жетконверсионстатус**](getconversionstatus-win32-encryptablevolume.md) указывает, что шифрование или расшифровка приостанавливаются.</span><span class="sxs-lookup"><span data-stu-id="40428-120">If this method is used on a volume with encryption/decryption in progress, successfully running this method causes [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to indicate that encryption or decryption is paused.</span></span>

<span data-ttu-id="40428-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="40428-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="40428-122">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="40428-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="40428-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="40428-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="40428-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="40428-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="40428-125">Требования</span><span class="sxs-lookup"><span data-stu-id="40428-125">Requirements</span></span>



| <span data-ttu-id="40428-126">Требование</span><span class="sxs-lookup"><span data-stu-id="40428-126">Requirement</span></span> | <span data-ttu-id="40428-127">Значение</span><span class="sxs-lookup"><span data-stu-id="40428-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40428-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="40428-128">Minimum supported client</span></span><br/> | <span data-ttu-id="40428-129">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="40428-129">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="40428-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="40428-130">Minimum supported server</span></span><br/> | <span data-ttu-id="40428-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="40428-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="40428-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="40428-132">Namespace</span></span><br/>                | <span data-ttu-id="40428-133">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="40428-133">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="40428-134">MOF</span><span class="sxs-lookup"><span data-stu-id="40428-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40428-135"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40428-135"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40428-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40428-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40428-137">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="40428-137">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
