---
title: Защита файлов с помощью DRM версии 1
description: Защита файлов с помощью DRM версии 1
ms.assetid: 91de1c20-e926-4ff6-b0cd-e90fc9cbaad2
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
ms.openlocfilehash: 1d3e4d1ae9c0d3835c20f75b4e61c262a85a26f4
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104336652"
---
# <a name="protecting-files-with-drm-version-1"></a><span data-ttu-id="8693d-115">Защита файлов с помощью DRM версии 1</span><span class="sxs-lookup"><span data-stu-id="8693d-115">Protecting Files with DRM Version 1</span></span>

<span data-ttu-id="8693d-116">При применении этого типа защиты создается лицензия DRM версии 1, которая действительна только на компьютере, с которого был сделан запрос на лицензию.</span><span class="sxs-lookup"><span data-stu-id="8693d-116">When this kind of protection is applied, a DRM version 1 license is generated that is valid only on the machine from which the license request was made.</span></span> <span data-ttu-id="8693d-117">Поскольку начальное значение ключа или ключа не задано, невозможно создать переносимые лицензии для содержимого, защищенного с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="8693d-117">Because no key or key seed is set, there is no way to generate portable licenses for content protected using this technique.</span></span> <span data-ttu-id="8693d-118">Однако при использовании пакета SDK Windows Media Format 7,1 или более поздней версии лицензии могут быть восстановлены в службе миграции лицензий Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="8693d-118">However, when using the Windows Media Format SDK 7.1 or later, the licenses are recoverable at the Microsoft License Migration service.</span></span>

<span data-ttu-id="8693d-119">Чтобы защитить файлы ASF с помощью DRM версии 1, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8693d-119">To protect ASF files using DRM version 1, perform the following steps:</span></span>

1.  <span data-ttu-id="8693d-120">Свяжите файл Вмстубдрм. lib с проектом и при необходимости отменяйте связь вмвкоре. lib.</span><span class="sxs-lookup"><span data-stu-id="8693d-120">Link the WMStubDRM.lib file to your project and, if necessary, unlink wmvcore.lib.</span></span>
2.  <span data-ttu-id="8693d-121">Чтобы создать модуль записи, вызовите функцию [**вмкреатевритер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) .</span><span class="sxs-lookup"><span data-stu-id="8693d-121">Call the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function to create the writer.</span></span> <span data-ttu-id="8693d-122">Первый аргумент зарезервирован и должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="8693d-122">The first argument is reserved and must be set to **NULL**.</span></span>
3.  <span data-ttu-id="8693d-123">Задайте профиль для модуля записи, который следует использовать, вызвав [**ивмвритер:: сетпрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) или [**Ивмвритер:: сетпрофилебид**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid).</span><span class="sxs-lookup"><span data-stu-id="8693d-123">Set a profile for the writer to use by calling [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) or [**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid).</span></span> <span data-ttu-id="8693d-124">Перед установкой атрибутов DRM необходимо задать профиль в модуле записи.</span><span class="sxs-lookup"><span data-stu-id="8693d-124">You must set a profile in the writer before setting any DRM attributes.</span></span> <span data-ttu-id="8693d-125">DRM поддерживается только для профилей, использующих видеокодеки Windows Media Audio или Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8693d-125">DRM is supported only for profiles that use the Windows Media Audio or Windows Media Video codecs.</span></span>
4.  <span data-ttu-id="8693d-126">С помощью метода [**ивмхеадеринфо:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) задайте следующие свойства DRM.</span><span class="sxs-lookup"><span data-stu-id="8693d-126">Using the [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) method, set the following DRM properties.</span></span> <span data-ttu-id="8693d-127">Свойство **USE \_ DRM** указывает компоненту DRM защищать содержимое с помощью DRM версии 1.</span><span class="sxs-lookup"><span data-stu-id="8693d-127">The **Use\_DRM** property instructs the DRM components to protect the content using DRM version 1.</span></span> <span data-ttu-id="8693d-128">Свойство **\_ flags DRM** указывает права, которые должны быть добавлены в локальную лицензию, которая будет создана для содержимого.</span><span class="sxs-lookup"><span data-stu-id="8693d-128">The **DRM\_Flags** property specifies the rights to be included in the local license that will be created for the content.</span></span> <span data-ttu-id="8693d-129">Значение **\_ уровня DRM** также хранится в лицензии; оно указывает минимальный уровень, необходимый для доступа к содержимому.</span><span class="sxs-lookup"><span data-stu-id="8693d-129">The **DRM\_LEVEL** value is also stored in the license; it specifies the minimum level required to access the content.</span></span> <span data-ttu-id="8693d-130">150 — рекомендуемый уровень содержимого для DRM версии 1.</span><span class="sxs-lookup"><span data-stu-id="8693d-130">150 is the recommended level for DRM version 1 content.</span></span>

    | <span data-ttu-id="8693d-131">attribute</span><span class="sxs-lookup"><span data-stu-id="8693d-131">Attribute</span></span>      | <span data-ttu-id="8693d-132">Значение</span><span class="sxs-lookup"><span data-stu-id="8693d-132">Value</span></span>                                                                                       |
    |----------------|---------------------------------------------------------------------------------------------|
    | <span data-ttu-id="8693d-133">**Использование \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="8693d-133">**Use\_DRM**</span></span>   | <span data-ttu-id="8693d-134">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="8693d-134">**TRUE**</span></span>                                                                                    |
    | <span data-ttu-id="8693d-135">**\_Флаги DRM**</span><span class="sxs-lookup"><span data-stu-id="8693d-135">**DRM\_Flags**</span></span> | <span data-ttu-id="8693d-136">ВМТ \_ right \_ Воспроизведение \| ВМТ \_ права \_ копирования \_ на \_ \_ устройство без \_ SDMI \| ВМТ \_ право \_ Копировать \_ на \_ компакт-диск</span><span class="sxs-lookup"><span data-stu-id="8693d-136">WMT\_RIGHT\_PLAYBACK \| WMT\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE \| WMT\_RIGHT\_COPY\_TO\_CD</span></span> |
    | <span data-ttu-id="8693d-137">**\_уровень DRM**</span><span class="sxs-lookup"><span data-stu-id="8693d-137">**DRM\_LEVEL**</span></span> | <span data-ttu-id="8693d-138">150</span><span class="sxs-lookup"><span data-stu-id="8693d-138">150</span></span>                                                                                         |

    

     

<span data-ttu-id="8693d-139">В следующем примере кода показано, как создать модуль записи с поддержкой DRM для DRM версии 1 и задать свойства DRM.</span><span class="sxs-lookup"><span data-stu-id="8693d-139">The following example code shows how to create a DRM-enabled writer for DRM version 1 and set the DRM properties.</span></span> <span data-ttu-id="8693d-140">В целях уточнения пропущена проверка ошибок.</span><span class="sxs-lookup"><span data-stu-id="8693d-140">Error checking has been omitted for the sake of clarify.</span></span>


```C++
BOOL  fUseDRM    = TRUE;
// These are the rights we will apply to the file. See WMT_RIGHTS for
// the full set of possible rights.

DWORD dwDRMFlags = WMT_RIGHT_PLAYBACK | 
                   WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE | 
                   WMT_RIGHT_COPY_TO_CD;

// Set the minimum required DRM level low enough
// to allow older players to access the content.
DWORD dwDRMLevel = 150;

IWMDRMWriter*  pWMDRMWriter  = NULL;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a writer object.
hr = WMCreateWriter( NULL, &pWMDRMWriter);

// Obtain the IWMHeaderInfo interface.
hr = pWMDRMWriter -> QueryInterface(IID_IWMHeaderInfo, 
                                   (void**) &pWMHeaderInfo);

// Tell the SDK runtime to protect the file using DRM version 1.
hr= pWMHeaderInfo-> SetAttribute(0,
                                 g_wszWMUse_DRM,
                                 WMT_TYPE_BOOL,
                                 (BYTE*)&fUseDRM,
                                 sizeof(BOOL));

// Specify the rights that will be stored in the local license that is
// created automatically for the content.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Flags, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMFlags,
                                 sizeof(DWORD) );

// Set the DRM_Level attribute in the file's DRM header.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Level, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMLevel,
                                 sizeof(DWORD) );
```



 

 




