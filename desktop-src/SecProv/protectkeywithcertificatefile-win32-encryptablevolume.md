---
description: Метод Протекткэйвисцертификатефиле класса Win32_EncryptableVolume — проверяет идентификатор объекта (OID) расширенного использования ключа (EKU) предоставленного сертификата.
ms.assetid: cc716524-f976-4d75-84f3-693e277030e6
title: Метод Протекткэйвисцертификатефиле класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d61a0bd0d31c14f13edd9ef610e8f6d3ed20f037
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110571"
---
# <a name="protectkeywithcertificatefile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="457c4-103">Метод Протекткэйвисцертификатефиле \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="457c4-103">ProtectKeyWithCertificateFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="457c4-104">Метод **протекткэйвисцертификатефиле** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) проверяет [*идентификатор объекта*](../secgloss/o-gly.md) (OID) расширенного использования ключа (EKU) предоставленного сертификата.</span><span class="sxs-lookup"><span data-stu-id="457c4-104">The **ProtectKeyWithCertificateFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class validates the Enhanced Key Usage (EKU) [*object identifier*](../secgloss/o-gly.md) (OID) of the provided certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="457c4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="457c4-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithCertificateFile(
  [in, optional] string FriendlyName,
  [in]           string FileName,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="457c4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="457c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="457c4-107">*FriendlyName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="457c4-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="457c4-108">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="457c4-108">Type: **string**</span></span>

<span data-ttu-id="457c4-109">Строка, указывающая назначенный пользователем строковый идентификатор для предохранителя ключа.</span><span class="sxs-lookup"><span data-stu-id="457c4-109">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="457c4-110">Если этот параметр не указан, параметр *FriendlyName* создается с использованием имени субъекта в сертификате.</span><span class="sxs-lookup"><span data-stu-id="457c4-110">If this parameter is not specified, the *FriendlyName* parameter is created by using the Subject Name in the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="457c4-111">*Имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="457c4-111">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="457c4-112">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="457c4-112">Type: **string**</span></span>

<span data-ttu-id="457c4-113">Строка, указывающая расположение и имя CER-файла, используемого для включения BitLocker.</span><span class="sxs-lookup"><span data-stu-id="457c4-113">A string that specifies the location and name of the .cer file used to enable BitLocker.</span></span> <span data-ttu-id="457c4-114">Сертификат шифрования должен быть экспортирован в формате CER ([*distinguished Encoding Rules*](../secgloss/d-gly.md) (Der) Binary [*x. 509*](../secgloss/x-gly.md) или Base-64 Encoded x. 509).</span><span class="sxs-lookup"><span data-stu-id="457c4-114">An encryption certificate must be exported in .cer format ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER)-encoded binary [*X.509*](../secgloss/x-gly.md) or Base-64 encoded X.509).</span></span> <span data-ttu-id="457c4-115">Сертификат шифрования может быть создан из PKI Майкрософт, стороннего PKI или самозаверяющего.</span><span class="sxs-lookup"><span data-stu-id="457c4-115">The encryption certificate may be generated from Microsoft PKI, third-party PKI, or self-signed.</span></span>

</dd> <dt>

<span data-ttu-id="457c4-116">*Волумекэйпротекторид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="457c4-116">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="457c4-117">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="457c4-117">Type: **string**</span></span>

<span data-ttu-id="457c4-118">Строка, однозначно определяющая созданный предохранитель ключа, который может использоваться для управления предохранителем ключа.</span><span class="sxs-lookup"><span data-stu-id="457c4-118">A string that uniquely identifies the created key protector that can be used to manage this key protector.</span></span>

<span data-ttu-id="457c4-119">Если диск поддерживает аппаратное шифрование, а BitLocker не использует нестандартное владение, для строки идентификатора задается значение "BitLocker", а предохранитель ключа записывается в метаданные диапазона.</span><span class="sxs-lookup"><span data-stu-id="457c4-119">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="457c4-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="457c4-120">Return value</span></span>

<span data-ttu-id="457c4-121">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="457c4-121">Type: **uint32**</span></span>

<span data-ttu-id="457c4-122">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="457c4-122">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="457c4-123">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="457c4-123">Return code/value</span></span>                                                                                                                                                                                           | <span data-ttu-id="457c4-124">Описание</span><span class="sxs-lookup"><span data-stu-id="457c4-124">Description</span></span>                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="457c4-125"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="457c4-125"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                           | <span data-ttu-id="457c4-126">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="457c4-126">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="457c4-127"><dt>**ФВЕ \_ E \_ без \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt></span><span class="sxs-lookup"><span data-stu-id="457c4-127"><dt>**FVE\_E\_NON\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl>                     | <span data-ttu-id="457c4-128">Атрибут EKU указанного сертификата не позволяет использовать его для шифрование диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="457c4-128">The EKU attribute of the specified certificate does not permit it to be used for BitLocker Drive Encryption.</span></span> <span data-ttu-id="457c4-129">BitLocker не требует, чтобы сертификат имел атрибут EKU, но если он настроен, он должен быть установлен в идентификатор OID, соответствующий идентификатору объекта, настроенного для BitLocker.</span><span class="sxs-lookup"><span data-stu-id="457c4-129">BitLocker does not require that a certificate have an EKU attribute, but if one is configured, it must be set to an OID that matches the OID configured for BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="457c4-130"><dt>**ФВЕ \_ \_ \_ Сертификат пользователя политики \_ \_ не \_ разрешен**</dt> <dt>2150695026 (0x80310072)</dt></span><span class="sxs-lookup"><span data-stu-id="457c4-130"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_NOT\_ALLOWED**</dt> <dt>2150695026 (0x80310072)</dt></span></span> </dl> | <span data-ttu-id="457c4-131">Групповая политика не позволяет использовать сертификаты пользователей, например смарт-карты, с BitLocker.</span><span class="sxs-lookup"><span data-stu-id="457c4-131">Group Policy does not permit user certificates, such as smart cards, to be used with BitLocker.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="457c4-132"><dt>**ФВЕ \_ \_ \_ Сертификат пользователя политики \_ \_ должен \_ иметь \_ оборудование HW**</dt> <dt>2150695028 (0x80310074)</dt></span><span class="sxs-lookup"><span data-stu-id="457c4-132"><dt>**FVE\_E\_POLICY\_USER\_CERT\_MUST\_BE\_HW**</dt> <dt>2150695028 (0x80310074)</dt></span></span> </dl>        | <span data-ttu-id="457c4-133">Для групповая политика необходимо предоставить смарт-карту для использования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="457c4-133">Group Policy requires that you supply a smart card to use BitLocker.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="457c4-134"><dt>**ФВЕ \_ E. \_ политика \_ запрещает \_ селфсигнед**</dt> <dt>2150695046 (0x80310086)</dt></span><span class="sxs-lookup"><span data-stu-id="457c4-134"><dt>**FVE\_E\_POLICY\_PROHIBITS\_SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span></span> </dl>           | <span data-ttu-id="457c4-135">Групповая политика не позволяет использовать самозаверяющие сертификаты.</span><span class="sxs-lookup"><span data-stu-id="457c4-135">Group Policy does not permit the use of self-signed certificates.</span></span><br/>                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="457c4-136"><dt>**Ошибка при \_ ФАЙЛ \_ не \_ найден**</dt> <dt>0000000002 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="457c4-136"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt> <dt>0000000002 (0x2)</dt></span></span> </dl>                                | <span data-ttu-id="457c4-137">Системе не удается найти указанный файл.</span><span class="sxs-lookup"><span data-stu-id="457c4-137">The system cannot find the specified file.</span></span><br/>                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="457c4-138">Remarks</span><span class="sxs-lookup"><span data-stu-id="457c4-138">Remarks</span></span>

<span data-ttu-id="457c4-139">Если OID не совпадает с идентификатором, связанным с контроллером службы в реестре, этот метод завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="457c4-139">If the OID does not match the one associated with the service controller in the registry, this method fails.</span></span> <span data-ttu-id="457c4-140">Это не дает пользователю вручную настраивать предохранители агента восстановления данных (DRA) на томе.</span><span class="sxs-lookup"><span data-stu-id="457c4-140">This prevents the user from setting data recovery agent (DRA) protectors manually on the volume.</span></span> <span data-ttu-id="457c4-141">Службы агентов DRA должны быть установлены только службой.</span><span class="sxs-lookup"><span data-stu-id="457c4-141">DRAs are only to be set by the service.</span></span>

## <a name="requirements"></a><span data-ttu-id="457c4-142">Требования</span><span class="sxs-lookup"><span data-stu-id="457c4-142">Requirements</span></span>



| <span data-ttu-id="457c4-143">Требование</span><span class="sxs-lookup"><span data-stu-id="457c4-143">Requirement</span></span> | <span data-ttu-id="457c4-144">Значение</span><span class="sxs-lookup"><span data-stu-id="457c4-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="457c4-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="457c4-145">Minimum supported client</span></span><br/> | <span data-ttu-id="457c4-146">Windows 7 Корпоративная, \[ только классические приложения Windows 7 Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="457c4-146">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="457c4-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="457c4-147">Minimum supported server</span></span><br/> | <span data-ttu-id="457c4-148">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="457c4-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="457c4-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="457c4-149">Namespace</span></span><br/>                | <span data-ttu-id="457c4-150">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="457c4-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="457c4-151">MOF</span><span class="sxs-lookup"><span data-stu-id="457c4-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="457c4-152"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="457c4-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="457c4-153">См. также</span><span class="sxs-lookup"><span data-stu-id="457c4-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="457c4-154">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="457c4-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
