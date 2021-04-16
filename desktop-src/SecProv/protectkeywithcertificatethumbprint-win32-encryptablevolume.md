---
description: Проверяет идентификатор объекта (OID) расширенного использования ключа (EKU) предоставленного сертификата.
ms.assetid: 7096cead-c44a-404c-b1e1-3e0ab27070f8
title: Метод Протекткэйвисцертификатесумбпринт класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e0b47aabccaacfb3ab81968b8a93037aad304f8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683920"
---
# <a name="protectkeywithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="167f8-103">Метод Протекткэйвисцертификатесумбпринт \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="167f8-103">ProtectKeyWithCertificateThumbprint method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="167f8-104">Метод **протекткэйвисцертификатесумбпринт** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) проверяет [*идентификатор объекта*](../secgloss/o-gly.md) (OID) расширенного использования ключа (EKU) предоставленного сертификата.</span><span class="sxs-lookup"><span data-stu-id="167f8-104">The **ProtectKeyWithCertificateThumbprint** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class validates the Enhanced Key Usage (EKU) [*object identifier*](../secgloss/o-gly.md) (OID) of the provided certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="167f8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="167f8-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithCertificateThumbprint(
  [in, optional] string FriendlyName,
  [in]           string CertThumbprint,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="167f8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="167f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="167f8-107">*FriendlyName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="167f8-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="167f8-108">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="167f8-108">Type: **string**</span></span>

<span data-ttu-id="167f8-109">Строка, указывающая назначенный пользователем строковый идентификатор для предохранителя ключа.</span><span class="sxs-lookup"><span data-stu-id="167f8-109">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="167f8-110">Если этот параметр не указан, параметр *FriendlyName* создается с использованием имени субъекта в сертификате.</span><span class="sxs-lookup"><span data-stu-id="167f8-110">If this parameter is not specified, the *FriendlyName* parameter is created by using the Subject Name in the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="167f8-111">*CertThumbprint* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="167f8-111">*CertThumbprint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="167f8-112">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="167f8-112">Type: **string**</span></span>

<span data-ttu-id="167f8-113">Строка, указывающая отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="167f8-113">A string that specifies the certificate thumbprint.</span></span>

</dd> <dt>

<span data-ttu-id="167f8-114">*Волумекэйпротекторид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="167f8-114">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="167f8-115">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="167f8-115">Type: **string**</span></span>

<span data-ttu-id="167f8-116">Строка, однозначно определяющая созданный предохранитель ключа, который может использоваться для управления предохранителем ключа.</span><span class="sxs-lookup"><span data-stu-id="167f8-116">A string that uniquely identifies the created key protector that can be used to manage this key protector.</span></span>

<span data-ttu-id="167f8-117">Если диск поддерживает аппаратное шифрование, а BitLocker не использует нестандартное владение, для строки идентификатора задается значение "BitLocker", а предохранитель ключа записывается в метаданные диапазона.</span><span class="sxs-lookup"><span data-stu-id="167f8-117">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="167f8-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="167f8-118">Return value</span></span>

<span data-ttu-id="167f8-119">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="167f8-119">Type: **uint32**</span></span>

<span data-ttu-id="167f8-120">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="167f8-120">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="167f8-121">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="167f8-121">Return code/value</span></span>                                                                                                                                                                                           | <span data-ttu-id="167f8-122">Описание</span><span class="sxs-lookup"><span data-stu-id="167f8-122">Description</span></span>                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="167f8-123"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="167f8-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                           | <span data-ttu-id="167f8-124">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="167f8-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="167f8-125"><dt>**Ошибка при \_ Недопустимые \_ данные**</dt> <dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="167f8-125"><dt>**ERROR\_INVALID\_DATA**</dt> <dt>13 (0xD)</dt></span></span> </dl>                                           | <span data-ttu-id="167f8-126">Недопустимые данные.</span><span class="sxs-lookup"><span data-stu-id="167f8-126">The data is not valid.</span></span><br/>                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="167f8-127"><dt>**ФВЕ \_ E \_ без \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt></span><span class="sxs-lookup"><span data-stu-id="167f8-127"><dt>**FVE\_E\_NON\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl>                     | <span data-ttu-id="167f8-128">Атрибут EKU указанного сертификата не позволяет использовать его для шифрование диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="167f8-128">The EKU attribute of the specified certificate does not permit it to be used for BitLocker Drive Encryption.</span></span> <span data-ttu-id="167f8-129">BitLocker не требует, чтобы сертификат имел атрибут EKU, но если он настроен, он должен быть установлен в идентификатор OID, соответствующий идентификатору объекта, настроенного для BitLocker.</span><span class="sxs-lookup"><span data-stu-id="167f8-129">BitLocker does not require that a certificate have an EKU attribute, but if one is configured, it must be set to an OID that matches the OID configured for BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="167f8-130"><dt>**ФВЕ \_ \_ \_ Сертификат пользователя политики \_ \_ не \_ разрешен**</dt> <dt>2150695026 (0x80310072)</dt></span><span class="sxs-lookup"><span data-stu-id="167f8-130"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_NOT\_ALLOWED**</dt> <dt>2150695026 (0x80310072)</dt></span></span> </dl> | <span data-ttu-id="167f8-131">Групповая политика не позволяет использовать сертификаты пользователей, например смарт-карты, с BitLocker.</span><span class="sxs-lookup"><span data-stu-id="167f8-131">Group Policy does not permit user certificates, such as smart cards, to be used with BitLocker.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="167f8-132"><dt>**ФВЕ \_ \_ \_ Сертификат пользователя политики \_ \_ должен \_ иметь \_ оборудование HW**</dt> <dt>2150695028 (0x80310074)</dt></span><span class="sxs-lookup"><span data-stu-id="167f8-132"><dt>**FVE\_E\_POLICY\_USER\_CERT\_MUST\_BE\_HW**</dt> <dt>2150695028 (0x80310074)</dt></span></span> </dl>        | <span data-ttu-id="167f8-133">Для групповая политика необходимо предоставить смарт-карту для использования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="167f8-133">Group Policy requires that you supply a smart card to use BitLocker.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="167f8-134"><dt>**ФВЕ \_ E. \_ политика \_ запрещает \_ селфсигнед**</dt> <dt>2150695046 (0x80310086)</dt></span><span class="sxs-lookup"><span data-stu-id="167f8-134"><dt>**FVE\_E\_POLICY\_PROHIBITS\_SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span></span> </dl>           | <span data-ttu-id="167f8-135">Групповая политика не позволяет использовать самозаверяющие сертификаты.</span><span class="sxs-lookup"><span data-stu-id="167f8-135">Group Policy does not permit the use of self-signed certificates.</span></span><br/>                                                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="167f8-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="167f8-136">Remarks</span></span>

<span data-ttu-id="167f8-137">Если OID не совпадает с идентификатором, связанным с контроллером службы в реестре, этот метод завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="167f8-137">If the OID does not match the one associated with the service controller in the registry, this method fails.</span></span> <span data-ttu-id="167f8-138">Это не дает пользователю вручную настраивать предохранители агента восстановления данных (DRA) на томе.</span><span class="sxs-lookup"><span data-stu-id="167f8-138">This prevents the user from setting data recovery agent (DRA) protectors manually on the volume.</span></span> <span data-ttu-id="167f8-139">Службы агентов DRA должны быть установлены только службой.</span><span class="sxs-lookup"><span data-stu-id="167f8-139">DRAs are only to be set by the service.</span></span>

## <a name="requirements"></a><span data-ttu-id="167f8-140">Требования</span><span class="sxs-lookup"><span data-stu-id="167f8-140">Requirements</span></span>



| <span data-ttu-id="167f8-141">Требование</span><span class="sxs-lookup"><span data-stu-id="167f8-141">Requirement</span></span> | <span data-ttu-id="167f8-142">Значение</span><span class="sxs-lookup"><span data-stu-id="167f8-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="167f8-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="167f8-143">Minimum supported client</span></span><br/> | <span data-ttu-id="167f8-144">Windows 7 Корпоративная, \[ только классические приложения Windows 7 Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="167f8-144">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="167f8-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="167f8-145">Minimum supported server</span></span><br/> | <span data-ttu-id="167f8-146">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="167f8-146">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="167f8-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="167f8-147">Namespace</span></span><br/>                | <span data-ttu-id="167f8-148">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="167f8-148">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="167f8-149">MOF</span><span class="sxs-lookup"><span data-stu-id="167f8-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="167f8-150"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="167f8-150"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="167f8-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="167f8-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="167f8-152">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="167f8-152">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
