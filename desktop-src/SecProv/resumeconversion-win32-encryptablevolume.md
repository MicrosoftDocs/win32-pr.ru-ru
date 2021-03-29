---
description: Возобновляет шифрование или расшифровку тома.
ms.assetid: e37f3e32-5510-431e-9782-11908e65300d
title: Метод Ресумеконверсион класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ResumeConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: eafa700f86e51310096835e2f24b53a28e66f800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809275"
---
# <a name="resumeconversion-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="c9dd2-103">Метод Ресумеконверсион \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="c9dd2-103">ResumeConversion method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="c9dd2-104">Метод **ресумеконверсион** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) возобновляет шифрование или расшифровку тома.</span><span class="sxs-lookup"><span data-stu-id="c9dd2-104">The **ResumeConversion** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class resumes the encryption or decryption of a volume.</span></span>

> [!Note]  
> <span data-ttu-id="c9dd2-105">Если диск поддерживает шифрование оборудования, эта функция может возобновить только операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="c9dd2-105">If the disc supports hardware encryption, this function can resume a wiping operation only.</span></span> <span data-ttu-id="c9dd2-106">Дополнительные сведения см. в разделе [**паусеконверсион**](pauseconversion-win32-encryptablevolume.md).</span><span class="sxs-lookup"><span data-stu-id="c9dd2-106">For more information, see [**PauseConversion**](pauseconversion-win32-encryptablevolume.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c9dd2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9dd2-107">Syntax</span></span>


```mof
uint32 ResumeConversion();
```



## <a name="parameters"></a><span data-ttu-id="c9dd2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9dd2-108">Parameters</span></span>

<span data-ttu-id="c9dd2-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c9dd2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9dd2-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9dd2-110">Return value</span></span>

<span data-ttu-id="c9dd2-111">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9dd2-111">Type: **uint32**</span></span>

<span data-ttu-id="c9dd2-112">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="c9dd2-112">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="c9dd2-113">Если этот метод используется для полностью зашифрованного или полностью расшифрованного тома или если шифрование или расшифровка уже выполняется на томе, возвращается значение 0, предполагая, что другие ошибки не возникают.</span><span class="sxs-lookup"><span data-stu-id="c9dd2-113">If this method is used on a fully encrypted or fully decrypted volume, or if encryption/decryption is already in progress on the volume, 0 is returned assuming no other errors occur.</span></span>



| <span data-ttu-id="c9dd2-114">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="c9dd2-114">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="c9dd2-115">Описание</span><span class="sxs-lookup"><span data-stu-id="c9dd2-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="c9dd2-116"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c9dd2-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="c9dd2-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="c9dd2-117">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="c9dd2-118"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="c9dd2-118"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="c9dd2-119">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="c9dd2-119">The volume is locked.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="c9dd2-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9dd2-120">Remarks</span></span>

<span data-ttu-id="c9dd2-121">Если этот метод используется на томе с приостановленным шифрованием или расшифровкой, то при успешном выполнении этого метода [**жетконверсионстатус**](getconversionstatus-win32-encryptablevolume.md) указывает, что шифрование или расшифровка выполняется.</span><span class="sxs-lookup"><span data-stu-id="c9dd2-121">If this method is used on a volume with paused encryption/decryption, successfully running this method causes [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to indicate that encryption or decryption is in progress.</span></span>

<span data-ttu-id="c9dd2-122">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="c9dd2-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c9dd2-123">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="c9dd2-123">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="c9dd2-124">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="c9dd2-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c9dd2-125">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="c9dd2-125">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9dd2-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c9dd2-126">Requirements</span></span>



| <span data-ttu-id="c9dd2-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c9dd2-127">Requirement</span></span> | <span data-ttu-id="c9dd2-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c9dd2-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9dd2-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9dd2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c9dd2-130">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="c9dd2-130">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c9dd2-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9dd2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c9dd2-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c9dd2-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c9dd2-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c9dd2-133">Namespace</span></span><br/>                | <span data-ttu-id="c9dd2-134">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="c9dd2-134">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="c9dd2-135">MOF</span><span class="sxs-lookup"><span data-stu-id="c9dd2-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9dd2-136"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9dd2-136"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9dd2-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9dd2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9dd2-138">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="c9dd2-138">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
