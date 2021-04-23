---
description: Задает указанную строку идентификатора в метаданных тома.
ms.assetid: 21355669-2052-4e7a-9c9d-aaa67533dd5e
title: Метод Сетидентификатионфиелд класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SetIdentificationField
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e8405be7aef91571bd3bd5d7dcb97214dcdfdb4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912808"
---
# <a name="setidentificationfield-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="73c24-103">Метод Сетидентификатионфиелд \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="73c24-103">SetIdentificationField method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="73c24-104">Метод **сетидентификатионфиелд** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) устанавливает указанную строку идентификатора в метаданных тома.</span><span class="sxs-lookup"><span data-stu-id="73c24-104">The **SetIdentificationField** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class sets the specified identifier string in the volume's metadata.</span></span>

## <a name="syntax"></a><span data-ttu-id="73c24-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73c24-105">Syntax</span></span>


```mof
uint32 SetIdentificationField(
  [in, optional] string IdentificationField
);
```



## <a name="parameters"></a><span data-ttu-id="73c24-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="73c24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73c24-107">*Идентификатионфиелд* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="73c24-107">*IdentificationField* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="73c24-108">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="73c24-108">Type: **string**</span></span>

<span data-ttu-id="73c24-109">Строка, указывающая поле идентификации, назначенное тому.</span><span class="sxs-lookup"><span data-stu-id="73c24-109">A string that specifies the identification field that is assigned to the volume.</span></span> <span data-ttu-id="73c24-110">Если необязательная строка отсутствует, используются значения набора реестра.</span><span class="sxs-lookup"><span data-stu-id="73c24-110">If the optional string is not present, the registry set values are used.</span></span> <span data-ttu-id="73c24-111">Если строка имеется и не пуста, используется указанное значение.</span><span class="sxs-lookup"><span data-stu-id="73c24-111">If the string is present and not empty, the specified value is used.</span></span> <span data-ttu-id="73c24-112">Параметр *идентификатионфиелд* не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="73c24-112">The *IdentificationField* parameter is not case-sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73c24-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73c24-113">Return value</span></span>

<span data-ttu-id="73c24-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73c24-114">Type: **uint32**</span></span>

<span data-ttu-id="73c24-115">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="73c24-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="73c24-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="73c24-116">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="73c24-117">Описание</span><span class="sxs-lookup"><span data-stu-id="73c24-117">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="73c24-118"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="73c24-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="73c24-119">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="73c24-119">The method was successful.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="73c24-120"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="73c24-120"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="73c24-121">Этот диск заблокирован шифрование диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="73c24-121">This drive is locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="73c24-122">Необходимо разблокировать этот том с панели управления.</span><span class="sxs-lookup"><span data-stu-id="73c24-122">You must unlock this volume from Control Panel.</span></span> <br/> |
| <dl> <span data-ttu-id="73c24-123"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="73c24-123"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="73c24-124">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="73c24-124">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="73c24-125">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="73c24-125">Add a key protector to enable BitLocker.</span></span> <br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="73c24-126">Требования</span><span class="sxs-lookup"><span data-stu-id="73c24-126">Requirements</span></span>



| <span data-ttu-id="73c24-127">Требование</span><span class="sxs-lookup"><span data-stu-id="73c24-127">Requirement</span></span> | <span data-ttu-id="73c24-128">Значение</span><span class="sxs-lookup"><span data-stu-id="73c24-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73c24-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73c24-129">Minimum supported client</span></span><br/> | <span data-ttu-id="73c24-130">Windows 7 Корпоративная, \[ только классические приложения Windows 7 Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="73c24-130">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="73c24-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73c24-131">Minimum supported server</span></span><br/> | <span data-ttu-id="73c24-132">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="73c24-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="73c24-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="73c24-133">Namespace</span></span><br/>                | <span data-ttu-id="73c24-134">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="73c24-134">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="73c24-135">MOF</span><span class="sxs-lookup"><span data-stu-id="73c24-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73c24-136"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73c24-136"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73c24-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73c24-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73c24-138">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="73c24-138">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




