---
description: Перечисляет все сертификаты в системе, соответствующие указанным критериям, и возвращает список отпечатков.
ms.assetid: 69522afe-9870-4ae9-8c69-cf8787913615
title: Метод Финдвалидцертификатес класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.FindValidCertificates
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 69612d860284f6a47dfa38c2aafc3e73f209c796
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347255"
---
# <a name="findvalidcertificates-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="fae7e-103">Метод Финдвалидцертификатес \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="fae7e-103">FindValidCertificates method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="fae7e-104">Метод **финдвалидцертификатес** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) перечисляет все сертификаты в системе, соответствующие указанным критериям, и возвращает список отпечатков.</span><span class="sxs-lookup"><span data-stu-id="fae7e-104">The **FindValidCertificates** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class enumerates all certificates on the system that match the indicated criteria and returns a list of thumbprints.</span></span> <span data-ttu-id="fae7e-105">Возвращаемый список содержит только сертификаты с допустимым [*идентификатором объекта*](../secgloss/o-gly.md) (OID).</span><span class="sxs-lookup"><span data-stu-id="fae7e-105">The returned list only contains certificates with a valid [*object identifier*](../secgloss/o-gly.md) (OID).</span></span> <span data-ttu-id="fae7e-106">OID может быть значением по умолчанию или его можно указать в групповая политика.</span><span class="sxs-lookup"><span data-stu-id="fae7e-106">The OID may be the default, or it may be specified in the Group Policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="fae7e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fae7e-107">Syntax</span></span>


```mof
uint32 FindValidCertificates(
  [out] string CertificateThumbprint[]
);
```



## <a name="parameters"></a><span data-ttu-id="fae7e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fae7e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fae7e-109">*CertificateThumbprint* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fae7e-109">*CertificateThumbprint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fae7e-110">Тип: **строка \[ \]**</span><span class="sxs-lookup"><span data-stu-id="fae7e-110">Type: **string\[\]**</span></span>

<span data-ttu-id="fae7e-111">Массив строк, содержащий список допустимых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="fae7e-111">An array of strings that contains the list of valid certificates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fae7e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fae7e-112">Return value</span></span>

<span data-ttu-id="fae7e-113">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fae7e-113">Type: **uint32**</span></span>

<span data-ttu-id="fae7e-114">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="fae7e-114">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="fae7e-115">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="fae7e-115">Return code/value</span></span>                                                                                                                                                                           | <span data-ttu-id="fae7e-116">Описание</span><span class="sxs-lookup"><span data-stu-id="fae7e-116">Description</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="fae7e-117"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="fae7e-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                           | <span data-ttu-id="fae7e-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="fae7e-118">The method was successful.</span></span><br/>                |
| <dl> <span data-ttu-id="fae7e-119"><dt>**ФВЕ \_ \_Недопустимый \_ \_ код BitLocker OID**</dt> <dt>2150695022 (0x8031006E)</dt></span><span class="sxs-lookup"><span data-stu-id="fae7e-119"><dt>**FVE\_E\_INVALID\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl> | <span data-ttu-id="fae7e-120">Недопустимый доступный OID BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fae7e-120">The available BitLocker OID is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fae7e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="fae7e-121">Requirements</span></span>



| <span data-ttu-id="fae7e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="fae7e-122">Requirement</span></span> | <span data-ttu-id="fae7e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="fae7e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fae7e-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fae7e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fae7e-125">Windows 7 Корпоративная, \[ только классические приложения Windows 7 Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="fae7e-125">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fae7e-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fae7e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fae7e-127">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="fae7e-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fae7e-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fae7e-128">Namespace</span></span><br/>                | <span data-ttu-id="fae7e-129">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="fae7e-129">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="fae7e-130">MOF</span><span class="sxs-lookup"><span data-stu-id="fae7e-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fae7e-131"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fae7e-131"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fae7e-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fae7e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fae7e-133">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="fae7e-133">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
