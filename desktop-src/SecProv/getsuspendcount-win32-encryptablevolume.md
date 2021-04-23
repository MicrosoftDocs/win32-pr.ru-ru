---
description: Возвращает количество приостановок BitLocker.
ms.assetid: B8C87352-62BA-4E5D-A273-CE74F3E1A7A8
title: Метод Жетсуспендкаунт класса Win32_EncryptableVolume (Активдбг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetSuspendCount
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: eb28f019674f39946674399f8931fb63421ef982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684057"
---
# <a name="getsuspendcount-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="2cb71-103">Метод Жетсуспендкаунт \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="2cb71-103">GetSuspendCount method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="2cb71-104">Метод **жетсуспендкаунт** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) извлекает количество перезагрузок, прежде чем защита будет автоматически возобновлена.</span><span class="sxs-lookup"><span data-stu-id="2cb71-104">The **GetSuspendCount** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the number of reboots before protection will automatically be resumed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cb71-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2cb71-105">Syntax</span></span>


```mof
uint32 GetSuspendCount(
   uint32 SuspendCount
);
```



## <a name="parameters"></a><span data-ttu-id="2cb71-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2cb71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cb71-107">*суспендкаунт*</span><span class="sxs-lookup"><span data-stu-id="2cb71-107">*SuspendCount*</span></span> 
</dt> <dd>

<span data-ttu-id="2cb71-108">Целочисленное значение от 0 до 15.</span><span class="sxs-lookup"><span data-stu-id="2cb71-108">An integer value from 0 to 15.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cb71-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2cb71-109">Return value</span></span>

<span data-ttu-id="2cb71-110">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="2cb71-110">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="2cb71-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2cb71-111">Return code</span></span>                                                                                          | <span data-ttu-id="2cb71-112">Описание</span><span class="sxs-lookup"><span data-stu-id="2cb71-112">Description</span></span>                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2cb71-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2cb71-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="2cb71-114">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="2cb71-114">The method was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="2cb71-115"><dt>**Ошибка \_ не \_ поддерживается**</dt></span><span class="sxs-lookup"><span data-stu-id="2cb71-115"><dt>**ERROR\_NOT\_SUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="2cb71-116">Возвращается, если том не приостановлен или не является томом операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2cb71-116">Returned if the volume is not suspended or is not an OS volume.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2cb71-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2cb71-117">Remarks</span></span>

<span data-ttu-id="2cb71-118">Этот метод применяется только к тому операционной системы и только в том случае, если он фактически приостанавливается в момент времени.</span><span class="sxs-lookup"><span data-stu-id="2cb71-118">This method only applies to the OS volume, and only if it is actually suspended at the time.</span></span> <span data-ttu-id="2cb71-119">Если том не приостановлен или не является томом операционной системы, будет возвращена **Ошибка \_ не \_ поддерживается** .</span><span class="sxs-lookup"><span data-stu-id="2cb71-119">If the volume is not suspended or is not an OS volume, **ERROR\_NOT\_SUPPORTED** will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cb71-120">Требования</span><span class="sxs-lookup"><span data-stu-id="2cb71-120">Requirements</span></span>



| <span data-ttu-id="2cb71-121">Требование</span><span class="sxs-lookup"><span data-stu-id="2cb71-121">Requirement</span></span> | <span data-ttu-id="2cb71-122">Значение</span><span class="sxs-lookup"><span data-stu-id="2cb71-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cb71-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2cb71-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2cb71-124">Windows 8 Корпоративная, \[ только классические приложения Windows 8 Pro\]</span><span class="sxs-lookup"><span data-stu-id="2cb71-124">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2cb71-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2cb71-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2cb71-126">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2cb71-126">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2cb71-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2cb71-127">Namespace</span></span><br/>                | <span data-ttu-id="2cb71-128">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="2cb71-128">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="2cb71-129">Header</span><span class="sxs-lookup"><span data-stu-id="2cb71-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cb71-130"><dt>Активдбг. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cb71-130"><dt>Activdbg.h</dt></span></span> </dl>                   |
| <span data-ttu-id="2cb71-131">MOF</span><span class="sxs-lookup"><span data-stu-id="2cb71-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2cb71-132"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2cb71-132"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cb71-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2cb71-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cb71-134">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="2cb71-134">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




