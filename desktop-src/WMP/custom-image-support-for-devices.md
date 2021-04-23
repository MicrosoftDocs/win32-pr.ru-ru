---
title: Поддержка пользовательских образов для устройств
description: Поддержка пользовательских образов для устройств
ms.assetid: 0ccc327c-e953-4348-9802-705331b574ac
keywords:
- Проигрыватель Windows Media, поддержка пользовательского изображения для устройств
- Проигрыватель Windows Media, поддержка изображений для устройств
- Поддержка пользовательских образов устройств
- Поддержка пользовательских образов для устройств
- Поддержка изображений для устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ffdf318df39935e844cc84919bb4d6e50cc259a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691590"
---
# <a name="custom-image-support-for-devices"></a><span data-ttu-id="4debd-108">Поддержка пользовательских образов для устройств</span><span class="sxs-lookup"><span data-stu-id="4debd-108">Custom Image Support for Devices</span></span>

> [!Note]  
> <span data-ttu-id="4debd-109">В этом разделе документируется функция проигрывателя Windows Media 10, доступная при использовании операционной системы Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4debd-109">This section documents a feature of Windows Media Player 10 that is available when using the Windows XP operating system.</span></span> <span data-ttu-id="4debd-110">В последующих версиях он может быть недоступен.</span><span class="sxs-lookup"><span data-stu-id="4debd-110">It may be unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4debd-111">Производители устройств могут предоставить два специальных файла изображений для настройки способа представления устройства в пользовательском интерфейсе проигрывателя Windows Media 10.</span><span class="sxs-lookup"><span data-stu-id="4debd-111">Device manufacturers can provide two special image files to customize the way a device is represented in the Windows Media Player 10 user interface.</span></span> <span data-ttu-id="4debd-112">Эти два файла:</span><span class="sxs-lookup"><span data-stu-id="4debd-112">These two files are:</span></span>

-   <span data-ttu-id="4debd-113">Девикон.</span><span class="sxs-lookup"><span data-stu-id="4debd-113">DevIcon.fil.</span></span> <span data-ttu-id="4debd-114">Файл форматирования значка Windows, представляющий оборудование устройства.</span><span class="sxs-lookup"><span data-stu-id="4debd-114">A Windows icon format file that represents the device hardware.</span></span> <span data-ttu-id="4debd-115">Это изображение отображается в проигрывателе Windows Media 10 в любом месте. значок используется для представления устройства, например списка устройств в функции **синхронизации** .</span><span class="sxs-lookup"><span data-stu-id="4debd-115">This image displays in Windows Media Player 10 anywhere an icon is used to represent a device, such as the device list in the **Sync** feature.</span></span>
-   <span data-ttu-id="4debd-116">Девлого.</span><span class="sxs-lookup"><span data-stu-id="4debd-116">DevLogo.fil.</span></span> <span data-ttu-id="4debd-117">Файл форматирования PNG, представляющий корпоративный логотип изготовителя устройства.</span><span class="sxs-lookup"><span data-stu-id="4debd-117">A PNG format file that represents the corporate logo of the device manufacturer.</span></span> <span data-ttu-id="4debd-118">Этот образ отображается в универсальной корпоративной фирменной символике проигрывателя Windows Media 10, например в диалоговом окне " **Настройка устройства** ".</span><span class="sxs-lookup"><span data-stu-id="4debd-118">This image displays in Windows Media Player 10 anywhere corporate branding is used, such as the **Device Setup** dialog box.</span></span>

## <a name="general-guidelines-for-images"></a><span data-ttu-id="4debd-119">Общие рекомендации по образам</span><span class="sxs-lookup"><span data-stu-id="4debd-119">General Guidelines for Images</span></span>

<span data-ttu-id="4debd-120">Следующие рекомендации относятся к поддержке пользовательских образов в целом.</span><span class="sxs-lookup"><span data-stu-id="4debd-120">The following guidelines apply to custom image support in general:</span></span>

-   <span data-ttu-id="4debd-121">Эта возможность является необязательной.</span><span class="sxs-lookup"><span data-stu-id="4debd-121">This feature is optional.</span></span> <span data-ttu-id="4debd-122">Устройства, не поставляют образы, будут представлены образами по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4debd-122">Devices that do not supply images will be represented by default images.</span></span>
-   <span data-ttu-id="4debd-123">Эта функция поддерживается только для устройств с поддержкой MTP.</span><span class="sxs-lookup"><span data-stu-id="4debd-123">This feature is supported for MTP-enabled devices only.</span></span>
-   <span data-ttu-id="4debd-124">Чтобы предотвратить внесение изменений в файлы, рекомендуется хранить файлы изображений в встроенном по или на защищенном носителе, а не в файлах, созданных пользователем.</span><span class="sxs-lookup"><span data-stu-id="4debd-124">To prevent changes to the files, it is recommended that the image files be stored in firmware or a protected storage medium, not with user-created files.</span></span>
-   <span data-ttu-id="4debd-125">Файлы не следует возвращать в Windows Media диспетчер устройств клиенты, которые перечисляют корневое хранилище устройства.</span><span class="sxs-lookup"><span data-stu-id="4debd-125">The files should not be returned to Windows Media Device Manager clients that enumerate the root storage of the device.</span></span> <span data-ttu-id="4debd-126">Кроме того, не следует удалять, перемещать или переименовывать файлы.</span><span class="sxs-lookup"><span data-stu-id="4debd-126">Also, deleting, moving, or renaming the files should fail.</span></span>
-   <span data-ttu-id="4debd-127">Если устройство поддерживает несколько носителей, устройство должно вернуть файлы образа в ответ на запросы открытия файлов с любого носителя.</span><span class="sxs-lookup"><span data-stu-id="4debd-127">If the device provides more than one storage medium, the device should return the image files in response to file open requests from any medium.</span></span> <span data-ttu-id="4debd-128">На каждом носителе могут возвращаться различные значки устройств.</span><span class="sxs-lookup"><span data-stu-id="4debd-128">Different device icons may be returned from each storage medium.</span></span>
-   <span data-ttu-id="4debd-129">Для клиентов, использующих Windows Media диспетчер устройств 1,2, эти образы имеют приоритет над свойствами значков, предоставляемыми механизмами установки Windows, такими как свойства узла устройства.</span><span class="sxs-lookup"><span data-stu-id="4debd-129">For Windows Media Device Manager 1.2-enabled clients, these images will take precedence over icon properties supplied by Windows setup mechanisms, such as device node properties.</span></span>
-   <span data-ttu-id="4debd-130">Изображения не должны содержать сведения, требующие локализации.</span><span class="sxs-lookup"><span data-stu-id="4debd-130">The images must not contain any information that requires localization.</span></span>
-   <span data-ttu-id="4debd-131">Для устройств с несколькими функциями только функции воспроизведения музыки в Windows XP будут использовать эти образы.</span><span class="sxs-lookup"><span data-stu-id="4debd-131">For multi-function devices, only the music playback features of Windows XP will use these images.</span></span>

## <a name="creating-the-device-icon-image"></a><span data-ttu-id="4debd-132">Создание изображения значка устройства</span><span class="sxs-lookup"><span data-stu-id="4debd-132">Creating the Device Icon Image</span></span>

<span data-ttu-id="4debd-133">Файл изображения значка устройства Девикон. Files должен содержать файл в формате значка Windows.</span><span class="sxs-lookup"><span data-stu-id="4debd-133">The device icon image file, DevIcon.fil, must contain a file in Windows icon format.</span></span> <span data-ttu-id="4debd-134">Значки статей MSDN [в Win32](/previous-versions/ms997538(v=msdn.10)) описывают, как создать такой файл.</span><span class="sxs-lookup"><span data-stu-id="4debd-134">The MSDN article [Icons in Win32](/previous-versions/ms997538(v=msdn.10)) describes how to create such a file.</span></span> <span data-ttu-id="4debd-135">В статье MSDN [Создание значков Windows XP](/previous-versions/ms997636(v=msdn.10)) приводятся рекомендации по стилю для значков Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4debd-135">The MSDN article [Creating Windows XP Icons](/previous-versions/ms997636(v=msdn.10)) provides style guidelines for Windows XP icons.</span></span> <span data-ttu-id="4debd-136">Файл изображения значка устройства включает двенадцать изображений в один файл, предоставляя четыре разных размера с тремя разными глубинами цвета.</span><span class="sxs-lookup"><span data-stu-id="4debd-136">The device icon image file incorporates twelve images in a single file by providing four different sizes with three different color depths each.</span></span>

<span data-ttu-id="4debd-137">Обратите особое внимание на следующие рекомендации.</span><span class="sxs-lookup"><span data-stu-id="4debd-137">Be certain to pay particular attention to the following guidelines:</span></span>

-   <span data-ttu-id="4debd-138">Рекомендуемые размеры (в пикселях): 16x16, 32x32, 48x48 и 256x256.</span><span class="sxs-lookup"><span data-stu-id="4debd-138">Recommended sizes (in pixels) are 16x16, 32x32, 48x48, and 256x256.</span></span>
-   <span data-ttu-id="4debd-139">Рекомендуемые глубины цвета — 24 бита с 8-разрядным альфа каналом, 8-разрядная с 1-разрядной прозрачностью и 4-разрядная с однобитовой прозрачностью.</span><span class="sxs-lookup"><span data-stu-id="4debd-139">Recommended color depths are 24-bit with 8-bit alpha channel, 8-bit with 1-bit transparency, and 4-bit with 1-bit transparency.</span></span>
-   <span data-ttu-id="4debd-140">Используйте угол перспективы и рекомендации по теневой тени, описанные в статьях MSDN, упомянутых ранее.</span><span class="sxs-lookup"><span data-stu-id="4debd-140">Use the perspective angle and drop shadow recommendations described in the MSDN articles mentioned previously.</span></span>

<span data-ttu-id="4debd-141">После создания файла значка просто переименуйте его в Девикон. Files.</span><span class="sxs-lookup"><span data-stu-id="4debd-141">Once you have created the icon file, simply rename it DevIcon.fil.</span></span>

## <a name="creating-the-corporate-logo-image"></a><span data-ttu-id="4debd-142">Создание изображения корпоративного логотипа</span><span class="sxs-lookup"><span data-stu-id="4debd-142">Creating the Corporate Logo Image</span></span>

<span data-ttu-id="4debd-143">Файл изображения корпоративного логотипа Девлого. Files должен содержать файл в формате PNG.</span><span class="sxs-lookup"><span data-stu-id="4debd-143">The corporate logo image file, DevLogo.fil, must contain a file in PNG format.</span></span> <span data-ttu-id="4debd-144">При создании образа следуйте приведенным ниже рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="4debd-144">Use the following guidelines when creating the image:</span></span>

-   <span data-ttu-id="4debd-145">Максимальные размеры изображения — 150x32 Пиксели.</span><span class="sxs-lookup"><span data-stu-id="4debd-145">The maximum dimensions for the image are 150x32 pixels.</span></span>
-   <span data-ttu-id="4debd-146">Изображение должно поддерживать альфа-смешение, чтобы обеспечить плавный переход между пользовательским интерфейсом проигрывателя Windows Media 10 и логотипом.</span><span class="sxs-lookup"><span data-stu-id="4debd-146">The image should support alpha blending to enable a smooth transition between the Windows Media Player 10 user interface and the logo.</span></span>

<span data-ttu-id="4debd-147">Создав файл эмблемы Организации, просто переименуйте его в Девлого. Files.</span><span class="sxs-lookup"><span data-stu-id="4debd-147">Once you have created the corporate logo file, simply rename it DevLogo.fil.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4debd-148">См. также</span><span class="sxs-lookup"><span data-stu-id="4debd-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4debd-149">**Проигрыватель Windows Media**</span><span class="sxs-lookup"><span data-stu-id="4debd-149">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 