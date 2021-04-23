---
description: Метод Филесигнатуреинфо объекта Installer принимает путь к файлу и возвращает SAFEARRAY байтов, представляющих хэш-код или закодированный сертификат.
ms.assetid: ab34bc46-8a8f-4b48-a1d1-d824ff36a9cc
title: Метод Installer. Филесигнатуреинфо
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSignatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5dbb758118b7612aaef3f7cca744674bca1c768d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651607"
---
# <a name="installerfilesignatureinfo-method"></a><span data-ttu-id="2c85d-103">Метод Installer. Филесигнатуреинфо</span><span class="sxs-lookup"><span data-stu-id="2c85d-103">Installer.FileSignatureInfo method</span></span>

<span data-ttu-id="2c85d-104">Метод **филесигнатуреинфо** объекта [**Installer**](installer-object.md) принимает путь к файлу и возвращает SAFEARRAY байтов, представляющих хэш-код или закодированный сертификат.</span><span class="sxs-lookup"><span data-stu-id="2c85d-104">The **FileSignatureInfo** method of the [**Installer**](installer-object.md) object takes the path to a file and returns a SAFEARRAY of bytes that represent the hash or the encoded certificate.</span></span> <span data-ttu-id="2c85d-105">Затем значения можно использовать для заполнения таблиц [мсидигиталсигнатуре](msidigitalsignature-table.md), [мсипатчцертификате](msipatchcertificate-table.md)и [мсидигиталцертификате](msidigitalcertificate-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2c85d-105">The values can then be used to populate the [MsiDigitalSignature](msidigitalsignature-table.md), [MsiPatchCertificate](msipatchcertificate-table.md), and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables.</span></span>

<span data-ttu-id="2c85d-106">Дополнительные сведения см. в разделе [**тип данных SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span><span class="sxs-lookup"><span data-stu-id="2c85d-106">For more information, see the [**SAFEARRAY Data Type**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span>

## <a name="syntax"></a><span data-ttu-id="2c85d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c85d-107">Syntax</span></span>


```JScript
Installer.FileSignatureInfo(
  FilePath,
  Options,
  Format
)
```



## <a name="parameters"></a><span data-ttu-id="2c85d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c85d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c85d-109">*Равно*</span><span class="sxs-lookup"><span data-stu-id="2c85d-109">*FilePath*</span></span> 
</dt> <dd>

<span data-ttu-id="2c85d-110">Полный путь к файлу с цифровой подписью.</span><span class="sxs-lookup"><span data-stu-id="2c85d-110">Full path to a file that is digitally signed.</span></span>

<span data-ttu-id="2c85d-111">При заполнении таблиц [мсидигиталсигнатуре](msidigitalsignature-table.md) и [мсидигиталцертификате](msidigitalcertificate-table.md) *FilePath* указывает на CAB-файл с цифровой подписью.</span><span class="sxs-lookup"><span data-stu-id="2c85d-111">When populating the [MsiDigitalSignature](msidigitalsignature-table.md) and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables, *FilePath* points to a digitally signed cabinet.</span></span> <span data-ttu-id="2c85d-112">При заполнении таблиц [мсипатчцертификате](msipatchcertificate-table.md) и мсидигиталцертификате *FilePath* указывает на исправление с цифровой подписью.</span><span class="sxs-lookup"><span data-stu-id="2c85d-112">When populating the [MsiPatchCertificate](msipatchcertificate-table.md) and MsiDigitalCertificate tables, *FilePath* points to a digitally signed patch.</span></span>

</dd> <dt>

<span data-ttu-id="2c85d-113">*Параметры*</span><span class="sxs-lookup"><span data-stu-id="2c85d-113">*Options*</span></span> 
</dt> <dd>

<span data-ttu-id="2c85d-114">Специальные флаги регистра ошибок.</span><span class="sxs-lookup"><span data-stu-id="2c85d-114">Special error case flags.</span></span>



| <span data-ttu-id="2c85d-115">Flag</span><span class="sxs-lookup"><span data-stu-id="2c85d-115">Flag</span></span>                                                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="2c85d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2c85d-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiSignatureOptionInvalidHashFatal"></span><span id="msisignatureoptioninvalidhashfatal"></span><span id="MSISIGNATUREOPTIONINVALIDHASHFATAL"></span><dl> <span data-ttu-id="2c85d-117"><dt>**мсисигнатуреоптионинвалидхашфатал**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2c85d-117"><dt>**msiSignatureOptionInvalidHashFatal**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="2c85d-118">Если *параметр* with имеет значение Мсисигнатуреоптионинвалидхашфатал, **филесигнатуреинфо** всегда возвращает неустранимую ошибку для недопустимого хэша.</span><span class="sxs-lookup"><span data-stu-id="2c85d-118">With *Options* set to msiSignatureOptionInvalidHashFatal, **FileSignatureInfo** always returns a fatal error for an invalid hash.</span></span> <br/> <span data-ttu-id="2c85d-119">Если для *параметров* не задано значение мсисигнатуреоптионинвалидхашфатал, а параметр *Format* имеет значение мсисигнатуреинфоцертификате, **филесигнатуреинфо** не возвращает ошибку для недопустимого хэша.</span><span class="sxs-lookup"><span data-stu-id="2c85d-119">If *Options* is not set to msiSignatureOptionInvalidHashFatal and *Format* is set to msiSignatureInfoCertificate, **FileSignatureInfo** does not return an error for an invalid hash.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2c85d-120">*Формат*</span><span class="sxs-lookup"><span data-stu-id="2c85d-120">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="2c85d-121">Запрошенные сведения о подписи.</span><span class="sxs-lookup"><span data-stu-id="2c85d-121">The requested signature information.</span></span>



| <span data-ttu-id="2c85d-122">Flag</span><span class="sxs-lookup"><span data-stu-id="2c85d-122">Flag</span></span>                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="2c85d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2c85d-123">Meaning</span></span>                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="msiSignatureInfoCertificate"></span><span id="msisignatureinfocertificate"></span><span id="MSISIGNATUREINFOCERTIFICATE"></span><dl> <span data-ttu-id="2c85d-124"><dt>**мсисигнатуреинфоцертификате**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2c85d-124"><dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="2c85d-125">Возвращает SAFEARRAY байт, представляющих закодированный сертификат.</span><span class="sxs-lookup"><span data-stu-id="2c85d-125">Returns a SAFEARRAY of bytes that represent the encoded certificate.</span></span><br/> |
| <span id="msiSignatureInfoHash"></span><span id="msisignatureinfohash"></span><span id="MSISIGNATUREINFOHASH"></span><dl> <span data-ttu-id="2c85d-126"><dt>**мсисигнатуреинфохаш**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2c85d-126"><dt>**msiSignatureInfoHash**</dt> <dt>1</dt></span></span> </dl>                             | <span data-ttu-id="2c85d-127">Возвращает SAFEARRAY байтов, представляющих хэш.</span><span class="sxs-lookup"><span data-stu-id="2c85d-127">Returns a SAFEARRAY of bytes that represent the hash.</span></span><br/>                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c85d-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c85d-128">Return value</span></span>

<span data-ttu-id="2c85d-129">В случае успешного выполнения метод возвращает [массив SafeArray](/windows/win32/api/oaidl/ns-oaidl-safearray) байтов, который содержит хэш-или закодированный сертификат.</span><span class="sxs-lookup"><span data-stu-id="2c85d-129">If successful, the method returns a [SAFEARRAY](/windows/win32/api/oaidl/ns-oaidl-safearray) of bytes that contain either the hash or encoded certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c85d-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c85d-130">Remarks</span></span>

<span data-ttu-id="2c85d-131">Чтобы создать полностью проверенную установку с помощью автоматизации, используйте метод **филесигнатуреинфо** для заполнения таблиц [мсидигиталцертификате](msidigitalcertificate-table.md), [мсипатчцертификате](msipatchcertificate-table.md)и [мсидигиталсигнатуре](msidigitalsignature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2c85d-131">To author a fully verified signed installation by using automation, use the **FileSignatureInfo** method to populate the [MsiDigitalCertificate](msidigitalcertificate-table.md), [MsiPatchCertificate](msipatchcertificate-table.md), and [MsiDigitalSignature](msidigitalsignature-table.md) tables.</span></span> <span data-ttu-id="2c85d-132">Дополнительные сведения см. [в статье Создание полностью проверенной подписанной установки с помощью службы автоматизации](authoring-a-fully-verified-signed-installation-using-automation.md).</span><span class="sxs-lookup"><span data-stu-id="2c85d-132">For more information, see [Authoring a Fully Verified Signed Installation Using Automation](authoring-a-fully-verified-signed-installation-using-automation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c85d-133">Требования</span><span class="sxs-lookup"><span data-stu-id="2c85d-133">Requirements</span></span>



| <span data-ttu-id="2c85d-134">Требование</span><span class="sxs-lookup"><span data-stu-id="2c85d-134">Requirement</span></span> | <span data-ttu-id="2c85d-135">Значение</span><span class="sxs-lookup"><span data-stu-id="2c85d-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c85d-136">Версия</span><span class="sxs-lookup"><span data-stu-id="2c85d-136">Version</span></span><br/> | <span data-ttu-id="2c85d-137">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2c85d-137">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2c85d-138">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2c85d-138">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2c85d-139">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="2c85d-139">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="2c85d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="2c85d-140">DLL</span></span><br/>     | <dl> <span data-ttu-id="2c85d-141"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c85d-141"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="2c85d-142">IID</span><span class="sxs-lookup"><span data-stu-id="2c85d-142">IID</span></span><br/>     | <span data-ttu-id="2c85d-143">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2c85d-143">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="2c85d-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c85d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c85d-145">Создание полностью проверенной подписанной установки с помощью службы автоматизации</span><span class="sxs-lookup"><span data-stu-id="2c85d-145">Authoring a Fully Verified Signed Installation Using Automation</span></span>](authoring-a-fully-verified-signed-installation-using-automation.md)
</dt> <dt>

[<span data-ttu-id="2c85d-146">Цифровые подписи и установщик Windows</span><span class="sxs-lookup"><span data-stu-id="2c85d-146">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> <dt>

[<span data-ttu-id="2c85d-147">**мсижетфилесигнатуреинформатион**</span><span class="sxs-lookup"><span data-stu-id="2c85d-147">**MsiGetFileSignatureInformation**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> </dl>

 

 
