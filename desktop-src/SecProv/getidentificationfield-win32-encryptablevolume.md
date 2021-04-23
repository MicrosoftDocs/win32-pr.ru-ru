---
description: Возвращает строку идентификатора, доступную в метаданных тома.
ms.assetid: 0573cbcd-6fb1-4648-bb06-4433796f6bb5
title: Метод Жетидентификатионфиелд класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetIdentificationField
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: bb70f76d9556df5bed70639471eb7a0f3afaaecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144407"
---
# <a name="getidentificationfield-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="33248-103">Метод Жетидентификатионфиелд \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="33248-103">GetIdentificationField method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="33248-104">Метод **жетидентификатионфиелд** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) возвращает строку идентификатора, доступную в метаданных тома.</span><span class="sxs-lookup"><span data-stu-id="33248-104">The **GetIdentificationField** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the identifier string available in the volume's metadata.</span></span>

## <a name="syntax"></a><span data-ttu-id="33248-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33248-105">Syntax</span></span>


```mof
uint32 GetIdentificationField(
  [out] string IdentificationField
);
```



## <a name="parameters"></a><span data-ttu-id="33248-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="33248-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33248-107">*Идентификатионфиелд* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="33248-107">*IdentificationField* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33248-108">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="33248-108">Type: **string**</span></span>

<span data-ttu-id="33248-109">Строка, указывающая поле идентификации, назначенное тому.</span><span class="sxs-lookup"><span data-stu-id="33248-109">A string that specifies the identification field that is assigned to the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33248-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="33248-110">Return value</span></span>

<span data-ttu-id="33248-111">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33248-111">Type: **uint32**</span></span>

<span data-ttu-id="33248-112">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="33248-112">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="33248-113">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="33248-113">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="33248-114">Описание</span><span class="sxs-lookup"><span data-stu-id="33248-114">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="33248-115"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="33248-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="33248-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="33248-116">The method was successful.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="33248-117"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="33248-117"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="33248-118">Этот диск заблокирован шифрование диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="33248-118">This drive is locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="33248-119">Необходимо разблокировать этот том с панели управления.</span><span class="sxs-lookup"><span data-stu-id="33248-119">You must unlock this volume from Control Panel.</span></span> <br/> |
| <dl> <span data-ttu-id="33248-120"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="33248-120"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="33248-121">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="33248-121">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="33248-122">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="33248-122">Add a key protector to enable BitLocker.</span></span> <br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="33248-123">Требования</span><span class="sxs-lookup"><span data-stu-id="33248-123">Requirements</span></span>



| <span data-ttu-id="33248-124">Требование</span><span class="sxs-lookup"><span data-stu-id="33248-124">Requirement</span></span> | <span data-ttu-id="33248-125">Значение</span><span class="sxs-lookup"><span data-stu-id="33248-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33248-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33248-126">Minimum supported client</span></span><br/> | <span data-ttu-id="33248-127">Windows 7 Корпоративная, \[ только классические приложения Windows 7 Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="33248-127">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="33248-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33248-128">Minimum supported server</span></span><br/> | <span data-ttu-id="33248-129">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="33248-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="33248-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="33248-130">Namespace</span></span><br/>                | <span data-ttu-id="33248-131">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="33248-131">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="33248-132">MOF</span><span class="sxs-lookup"><span data-stu-id="33248-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33248-133"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33248-133"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33248-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33248-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33248-135">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="33248-135">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




