---
title: Создание и инициализация модуля записи DRM
description: Создание и инициализация модуля записи DRM
ms.assetid: ce0508e1-f69f-4e09-8c32-8c9dac48b5ec
keywords:
- Windows Media Format SDK, записи DRM
- Управление цифровыми правами (DRM), создание модулей записи DRM
- DRM (Управление цифровыми правами), создание модулей записи DRM
- Управление цифровыми правами (DRM), инициализация записи DRM
- DRM (Управление цифровыми правами), инициализация записи DRM
- Расширенные API клиента DRM, модули записи DRM
- Расширенные API клиента, записи DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ed40b7f9dd9c486b1ef22e5042261c5ce03d2f7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "105700969"
---
# <a name="creating-and-initializing-a-drm-writer"></a><span data-ttu-id="0ef21-110">Создание и инициализация модуля записи DRM</span><span class="sxs-lookup"><span data-stu-id="0ef21-110">Creating and Initializing a DRM Writer</span></span>

<span data-ttu-id="0ef21-111">Чтобы инициализировать объект модуля записи ASF для импорта зашифрованных примеров мультимедиа в Windows Media DRM, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0ef21-111">The following steps are required to initialize an ASF writer object for importing encrypted media samples in Windows Media DRM.</span></span>

1.  <span data-ttu-id="0ef21-112">Выполните шаги 1 – 4 [импорта лицензии и материала ключа](importing-license-and-key-material.md).</span><span class="sxs-lookup"><span data-stu-id="0ef21-112">Follow steps 1 to 4 of [Importing License and Key Material](importing-license-and-key-material.md).</span></span>
2.  <span data-ttu-id="0ef21-113">Создание и инициализация объекта модуля записи ASF с помощью соответствующего материала ключа DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0ef21-113">Create and initialize an ASF writer object using the appropriate Windows Media DRM key material.</span></span> <span data-ttu-id="0ef21-114">Дополнительные сведения см. в разделе [Включение поддержки DRM](enabling-drm-support.md).</span><span class="sxs-lookup"><span data-stu-id="0ef21-114">For more information, see [Enabling DRM Support](enabling-drm-support.md).</span></span>
3.  <span data-ttu-id="0ef21-115">Задайте каждый из следующих атрибутов, вызвав [**ивмдрмвритер:: сетдрматтрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute):</span><span class="sxs-lookup"><span data-stu-id="0ef21-115">Set each of the following attributes by calling [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute):</span></span>
    -   <span data-ttu-id="0ef21-116">\_ХЕАДЕРСИГНПРИВКЭЙ DRM</span><span class="sxs-lookup"><span data-stu-id="0ef21-116">DRM\_HeaderSignPrivKey</span></span>
    -   <span data-ttu-id="0ef21-117">\_V1LICENSEACQURL DRM</span><span class="sxs-lookup"><span data-stu-id="0ef21-117">DRM\_V1LicenseAcqURL</span></span>
    -   <span data-ttu-id="0ef21-118">\_KEYID DRM</span><span class="sxs-lookup"><span data-stu-id="0ef21-118">DRM\_KeyID</span></span>
    -   <span data-ttu-id="0ef21-119">\_ЛИЦЕНСЕАККУРЛ DRM</span><span class="sxs-lookup"><span data-stu-id="0ef21-119">DRM\_LicenseAcqURL</span></span>
4.  <span data-ttu-id="0ef21-120">Если на компьютере, на котором работает программное обеспечение, не установлена лицензированная версия диспетчера прав Windows Media, необходимо также задать следующие четыре атрибута:</span><span class="sxs-lookup"><span data-stu-id="0ef21-120">If a licensed version of Windows Media Rights Manager is not installed on the computer running your software, then the following four attributes must also be set:</span></span>
    -   <span data-ttu-id="0ef21-121">\_ЛАСИГНАТУРЕРУТЦЕРТ DRM</span><span class="sxs-lookup"><span data-stu-id="0ef21-121">DRM\_LASignatureRootCert</span></span>
    -   <span data-ttu-id="0ef21-122">\_ЛАСИГНАТУРЕЦЕРТ DRM</span><span class="sxs-lookup"><span data-stu-id="0ef21-122">DRM\_LASignatureCert</span></span>
    -   <span data-ttu-id="0ef21-123">\_ЛАСИГНАТУРЕЛИКСРВЦЕРТ DRM</span><span class="sxs-lookup"><span data-stu-id="0ef21-123">DRM\_LASignatureLicSrvCert</span></span>
    -   <span data-ttu-id="0ef21-124">\_ЛАСИГНАТУРЕПРИВКЭЙ DRM</span><span class="sxs-lookup"><span data-stu-id="0ef21-124">DRM\_LASignaturePrivKey</span></span>
    -   <span data-ttu-id="0ef21-125">Приложение для необходимых сертификатов шифрования можно выполнить, заполнив [соглашение о лицензировании Windows Media (вмла)](https://www.microsoft.com/licensing/default) в сети.</span><span class="sxs-lookup"><span data-stu-id="0ef21-125">Application for the necessary encryption certificates can be completed by filling out the [Windows Media Licensing Agreement (WMLA)](https://www.microsoft.com/licensing/default) online.</span></span>
5.  <span data-ttu-id="0ef21-126">Создайте ключ сеанса и заполните структуру [**\_ \_ \_ ключа сеанса импорта WMDRM**](wmdrm-import-session-key.md) .</span><span class="sxs-lookup"><span data-stu-id="0ef21-126">Create a session key and fill out a [**WMDRM\_IMPORT\_SESSION\_KEY**](wmdrm-import-session-key.md) structure.</span></span> <span data-ttu-id="0ef21-127">Ключ сеанса будет использоваться для шифрования ключа содержимого.</span><span class="sxs-lookup"><span data-stu-id="0ef21-127">The session key will be used for encrypting a content key.</span></span> <span data-ttu-id="0ef21-128">Пример см. в разделе [Пример создания ключа сеанса](create-session-key-example.md).</span><span class="sxs-lookup"><span data-stu-id="0ef21-128">For an example, see [Create Session Key Example](create-session-key-example.md).</span></span>
6.  <span data-ttu-id="0ef21-129">Создайте ключ содержимого на основе вектора инициализации случайных чисел RC4 и заполните [**структуру \_ \_ \_ ключа содержимого для импорта WMDRM**](wmdrm-import-content-key.md) .</span><span class="sxs-lookup"><span data-stu-id="0ef21-129">Create a content key from a random RC4 initialization vector, and fill out a [**WMDRM\_IMPORT\_CONTENT\_KEY**](wmdrm-import-content-key.md) structure.</span></span> <span data-ttu-id="0ef21-130">Ключ содержимого используется для шифрования образцов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0ef21-130">The content key is used for encrypting the media samples.</span></span> <span data-ttu-id="0ef21-131">Пример см. в разделе [Пример создания ключа содержимого](create-content-key-example.md).</span><span class="sxs-lookup"><span data-stu-id="0ef21-131">For an example, see [Create Content Key Example](create-content-key-example.md).</span></span>
7.  <span data-ttu-id="0ef21-132">Зашифруйте ключ содержимого с помощью ключа сеанса, используя шифрование RC4.</span><span class="sxs-lookup"><span data-stu-id="0ef21-132">Encrypt the content key with the session key, using RC4 encryption.</span></span>
8.  <span data-ttu-id="0ef21-133">Извлеките ключ коллекции сертификатов компьютера.</span><span class="sxs-lookup"><span data-stu-id="0ef21-133">Extract the machine certificate collection key.</span></span> <span data-ttu-id="0ef21-134">Например, см. [Пример получения сертификата компьютера](get-machine-certificate-example.md).</span><span class="sxs-lookup"><span data-stu-id="0ef21-134">For an example, see [Get Machine Certificate Example](get-machine-certificate-example.md).</span></span>
9.  <span data-ttu-id="0ef21-135">Зашифруйте ключ сеанса с помощью открытого ключа, извлеченного из сертификата.</span><span class="sxs-lookup"><span data-stu-id="0ef21-135">Encrypt the session key with the public key extracted from the certificate.</span></span>
10. <span data-ttu-id="0ef21-136">Заполните [**структуру \_ \_ \_ структуры инициализации для импорта WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .</span><span class="sxs-lookup"><span data-stu-id="0ef21-136">Fill out a [**WMDRM\_IMPORT\_INIT\_STRUCT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) structure.</span></span>
11. <span data-ttu-id="0ef21-137">Вызовите метод [**IWMDRMWriter3:: сетпротектстреамсамплес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) , чтобы УВЕДОМИТЬ пакет SDK о том, что образцы, поступающие из модуля записи, уже защищены и должны быть отправлены непосредственно клиенту DRM Windows Media для импорта.</span><span class="sxs-lookup"><span data-stu-id="0ef21-137">Call the [**IWMDRMWriter3::SetProtectStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) method to notify the SDK that samples coming into the writer are already protected and should be sent directly to the Windows Media DRM client for import.</span></span>
12. <span data-ttu-id="0ef21-138">Вызовите [**ивмвритер:: бегинвритинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="0ef21-138">Call [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

<span data-ttu-id="0ef21-139">Остальные шаги по созданию файла, защищенного с помощью DRM, описаны в руководстве по программированию Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="0ef21-139">The remaining steps for creating a DRM-protected file are documented in the Windows Media Format SDK Programming Guide.</span></span> <span data-ttu-id="0ef21-140">Дополнительные сведения см. в разделе [Создание защищенных файлов](creating-protected-files.md).</span><span class="sxs-lookup"><span data-stu-id="0ef21-140">For more information, see [Creating Protected Files](creating-protected-files.md).</span></span>

<span data-ttu-id="0ef21-141">Следующий шаг — выполнить итерацию каждого примера носителя, зашифровать его и передать в объект модуля записи.</span><span class="sxs-lookup"><span data-stu-id="0ef21-141">The next step is to iterate through each media sample, encrypt it, and pass it to the writer object.</span></span> <span data-ttu-id="0ef21-142">Дополнительные сведения см. в разделе [Примеры шифрования и импорта мультимедиа](encrypting-and-importing-media-samples.md).</span><span class="sxs-lookup"><span data-stu-id="0ef21-142">For more information, see the [Encrypting and Importing Media Samples](encrypting-and-importing-media-samples.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ef21-143">См. также</span><span class="sxs-lookup"><span data-stu-id="0ef21-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ef21-144">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="0ef21-144">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="0ef21-145">**Импорт DRM**</span><span class="sxs-lookup"><span data-stu-id="0ef21-145">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




