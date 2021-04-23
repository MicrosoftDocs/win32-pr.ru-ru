---
title: Создание защищенных файлов
description: Создание защищенных файлов
ms.assetid: 5237e797-72ec-402e-81ec-ab379747e464
keywords:
- Windows Media Format SDK, создание защищенных файлов
- Windows Media Format SDK, защищенные файлы
- Расширенный формат систем (ASF), создание защищенных файлов
- ASF (Расширенный системный формат), создание защищенных файлов
- Расширенный формат систем (ASF), защищенные файлы
- ASF (Расширенный системный формат), защищенные файлы
- Расширенный системный формат (ASF), Вмстубдрм. lib
- ASF (Расширенный системный формат), Вмстубдрм. lib
- Вмстубдрм. lib, создание защищенных файлов
- Вмстубдрм. lib, защищенные файлы
- Управление цифровыми правами (DRM), Вмстубдрм. lib
- DRM (Управление цифровыми правами), Вмстубдрм. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160a14d96da924bdb2a307bc804514a1ec3de083
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336311"
---
# <a name="creating-protected-files"></a><span data-ttu-id="50d98-115">Создание защищенных файлов</span><span class="sxs-lookup"><span data-stu-id="50d98-115">Creating Protected Files</span></span>

<span data-ttu-id="50d98-116">Чтобы создать защищенные цифровые файлы мультимедиа с помощью DRM версии 1 или DRM версии 7 и более поздних, свяжите с файлом Вмстубдрм. lib, полученным от Майкрософт, и создайте объект модуля записи.</span><span class="sxs-lookup"><span data-stu-id="50d98-116">To create protected digital media files using either DRM version 1 or DRM versions 7 and later, link to the WMStubDRM.lib file that you obtained from Microsoft, and create the writer object.</span></span> <span data-ttu-id="50d98-117">Для защиты версии 1 используйте интерфейс [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) , чтобы задать атрибуты DRM, которые нужно применить.</span><span class="sxs-lookup"><span data-stu-id="50d98-117">For version 1 protection, use the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface to set the DRM attributes you want to apply.</span></span> <span data-ttu-id="50d98-118">В версиях 7 и более поздних используйте методы интерфейса [**ивмдрмвритер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) .</span><span class="sxs-lookup"><span data-stu-id="50d98-118">For versions 7 and later, use the [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) interface methods.</span></span>

<span data-ttu-id="50d98-119">В следующих разделах подробно описано, как защитить файлы.</span><span class="sxs-lookup"><span data-stu-id="50d98-119">The following topics describe in detail how to protect files.</span></span>

-   [<span data-ttu-id="50d98-120">Защита файлов с помощью DRM версии 1</span><span class="sxs-lookup"><span data-stu-id="50d98-120">Protecting Files with DRM Version 1</span></span>](protecting-files-with-drm-version-1.md)
-   [<span data-ttu-id="50d98-121">Защита файлов с помощью DRM версии 7 или более поздней</span><span class="sxs-lookup"><span data-stu-id="50d98-121">Protecting Files with DRM Version 7 or Later</span></span>](protecting-files-with-drm-version-7-or-later.md)

> [!Note]  
> <span data-ttu-id="50d98-122">DRM не поддерживает версию этого пакета SDK на базе x64.</span><span class="sxs-lookup"><span data-stu-id="50d98-122">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="50d98-123">См. также</span><span class="sxs-lookup"><span data-stu-id="50d98-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50d98-124">**Список атрибутов DRM**</span><span class="sxs-lookup"><span data-stu-id="50d98-124">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="50d98-125">**Свойства DRM**</span><span class="sxs-lookup"><span data-stu-id="50d98-125">**DRM Properties**</span></span>](drm-properties.md)
</dt> <dt>

[<span data-ttu-id="50d98-126">**Версии DRM**</span><span class="sxs-lookup"><span data-stu-id="50d98-126">**DRM Versions**</span></span>](drm-versions.md)
</dt> <dt>

[<span data-ttu-id="50d98-127">**Включение поддержки DRM**</span><span class="sxs-lookup"><span data-stu-id="50d98-127">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="50d98-128">**Получение требуемой библиотеки DRM**</span><span class="sxs-lookup"><span data-stu-id="50d98-128">**Obtaining the Required DRM Library**</span></span>](obtaining-the-required-drm-library.md)
</dt> <dt>

[<span data-ttu-id="50d98-129">**Чтение защищенных файлов**</span><span class="sxs-lookup"><span data-stu-id="50d98-129">**Reading Protected Files**</span></span>](reading-protected-files.md)
</dt> </dl>

 

 




