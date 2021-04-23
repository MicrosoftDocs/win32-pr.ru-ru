---
title: Требования к отображению портативных проигрывателей в проводнике Windows
description: Требования к отображению портативных проигрывателей в проводнике Windows
ms.assetid: 94227ed8-56e7-4366-9c38-9b5dbf907e16
keywords:
- Диспетчер устройств Windows Media, портативные аудио проигрыватели
- Диспетчер устройств, Portable Audio Players
- Программное обеспеченное, Портативное аудио Player
- поставщики услуг, Portable Audio Players
- Создание поставщиков услуг, переносимые аудио проигрыватели
- портативные аудио проигрыватели
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a163bf04f4185bc1325aa12ea6acddd43191529
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691242"
---
# <a name="requirements-for-portable-audio-players-to-appear-in-windows-explorer"></a><span data-ttu-id="e5858-109">Требования к отображению портативных проигрывателей в проводнике Windows</span><span class="sxs-lookup"><span data-stu-id="e5858-109">Requirements for Portable Audio Players to Appear in Windows Explorer</span></span>

<span data-ttu-id="e5858-110">Расширение пространства имен для оболочки Portable Audio Player предоставляет пользователям Windows единообразный способ управления звуковыми устройствами, управляемыми диспетчер устройств Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e5858-110">The portable audio player shell namespace extension provides Windows users with a consistent way to manage audio devices that are managed by Windows Media Device Manager.</span></span> <span data-ttu-id="e5858-111">Если вы разрабатываете компоненты поставщика услуг и драйверов в соответствии со следующими рекомендациями, устройство будет отображаться в пространстве имен оболочки.</span><span class="sxs-lookup"><span data-stu-id="e5858-111">If you author your service provider and driver components according to the following guidelines, your device will show up in the shell namespace.</span></span> <span data-ttu-id="e5858-112">Пользователи смогут единообразно взаимодействовать с содержимым устройства в проводнике Windows для выполнения основных операций, таких как копирование, удаление и переименование.</span><span class="sxs-lookup"><span data-stu-id="e5858-112">Users will be able to interact with the contents of your device in a consistent manner in Windows Explorer to perform basic operations such as copy, delete, and rename.</span></span>

<span data-ttu-id="e5858-113">Следующие требования к оболочке для поставщиков услуг и компонентов драйверов предназначены для дополнения общих руководств по диспетчер устройств Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e5858-113">The following shell requirements for service provider and driver components are intended to supplement the general Windows Media Device Manager guidelines.</span></span>

<span data-ttu-id="e5858-114">Возможности устройства</span><span class="sxs-lookup"><span data-stu-id="e5858-114">Device Capabilities</span></span>

<span data-ttu-id="e5858-115">Поставщики услуг Windows Media диспетчер устройств должны быть явными в поддерживаемых ими возможностях.</span><span class="sxs-lookup"><span data-stu-id="e5858-115">Windows Media Device Manager service providers should be explicit in their supported capabilities.</span></span> <span data-ttu-id="e5858-116">Если вызов не поддерживается, должен возвращаться код ошибки.</span><span class="sxs-lookup"><span data-stu-id="e5858-116">If a call is not supported, an error code must be returned.</span></span> <span data-ttu-id="e5858-117">Соответствующие поля должны быть установлены для присутствия или отсутствия возможностей, возвращаемых из следующих функций:</span><span class="sxs-lookup"><span data-stu-id="e5858-117">The appropriate fields must be set for the presence or absence of capabilities on return from the following functions:</span></span>

-   [<span data-ttu-id="e5858-118">**Возможности Имдспсторажеглобалс:: Capabilities**</span><span class="sxs-lookup"><span data-stu-id="e5858-118">**IMDSPStorageGlobals::GetCapabilities**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getcapabilities)
-   [<span data-ttu-id="e5858-119">**Имдспстораже:: OutAttribute**</span><span class="sxs-lookup"><span data-stu-id="e5858-119">**IMDSPStorage::GetAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
-   [<span data-ttu-id="e5858-120">**Имдспдевице:: Жетформатсуппорт**</span><span class="sxs-lookup"><span data-stu-id="e5858-120">**IMDSPDevice::GetFormatSupport**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)

<span data-ttu-id="e5858-121">Поставщики услуг должны поддерживать следующие возможности, совместимые с оболочкой:</span><span class="sxs-lookup"><span data-stu-id="e5858-121">Service providers must support the following capabilities to be compatible with the shell:</span></span>

-   <span data-ttu-id="e5858-122">Копирование на устройство (с поддержкой обратных вызовов Cancel и Progress)</span><span class="sxs-lookup"><span data-stu-id="e5858-122">Copy to device (with support for cancel and progress callbacks)</span></span>
-   <span data-ttu-id="e5858-123">Удаление файла с устройства (с поддержкой обратных вызовов Cancel и Progress)</span><span class="sxs-lookup"><span data-stu-id="e5858-123">Delete file from device (with support for cancel and progress callbacks)</span></span>
-   <span data-ttu-id="e5858-124">Переименовать файл на устройстве</span><span class="sxs-lookup"><span data-stu-id="e5858-124">Rename file on device</span></span>
-   <span data-ttu-id="e5858-125">Отчет о пространстве (общий объем, свободное место, неиспользуемое пространство)</span><span class="sxs-lookup"><span data-stu-id="e5858-125">Space reporting (total space, free space, unusable space)</span></span>
-   <span data-ttu-id="e5858-126">Самонастраивающийся (см. раздел [Включение PnP для устройств](enabling-pnp-for-devices.md))</span><span class="sxs-lookup"><span data-stu-id="e5858-126">Plug and Play (see [Enabling PnP for Devices](enabling-pnp-for-devices.md))</span></span>
-   <span data-ttu-id="e5858-127">Формат (желательно с поддержкой для обратных вызовов Cancel и Progress)</span><span class="sxs-lookup"><span data-stu-id="e5858-127">Format (preferably with support for cancel and progress callbacks)</span></span>

<span data-ttu-id="e5858-128">Если метаданные поддерживаются, для отдельных файлов должны поддерживаться следующие поля.</span><span class="sxs-lookup"><span data-stu-id="e5858-128">If metadata is supported, the following fields must be supported for individual files.</span></span> <span data-ttu-id="e5858-129">Если данные недоступны, поле должно быть инициализировано как пустая строка:</span><span class="sxs-lookup"><span data-stu-id="e5858-129">If no data is available, the field should be initialized as an empty string:</span></span>



| <span data-ttu-id="e5858-130">Поле</span><span class="sxs-lookup"><span data-stu-id="e5858-130">Field</span></span>        | <span data-ttu-id="e5858-131">Константа (определяется в ВМДМ. IDL)</span><span class="sxs-lookup"><span data-stu-id="e5858-131">Constant (defined in WMDM.idl)</span></span> | <span data-ttu-id="e5858-132">Тег Metadata</span><span class="sxs-lookup"><span data-stu-id="e5858-132">Metadata tag</span></span>    |
|--------------|--------------------------------|-----------------|
| <span data-ttu-id="e5858-133">Название песни</span><span class="sxs-lookup"><span data-stu-id="e5858-133">Song Title</span></span>   | <span data-ttu-id="e5858-134">g \_ всзвмдмтитле</span><span class="sxs-lookup"><span data-stu-id="e5858-134">g\_wszWMDMTitle</span></span>                | <span data-ttu-id="e5858-135">ВМДМ/заголовок</span><span class="sxs-lookup"><span data-stu-id="e5858-135">WMDM/Title</span></span>      |
| <span data-ttu-id="e5858-136">Номер записи</span><span class="sxs-lookup"><span data-stu-id="e5858-136">Track Number</span></span> | <span data-ttu-id="e5858-137">g \_ всзвмдмтракк</span><span class="sxs-lookup"><span data-stu-id="e5858-137">g\_wszWMDMTrack</span></span>                | <span data-ttu-id="e5858-138">ВМДМ/Track</span><span class="sxs-lookup"><span data-stu-id="e5858-138">WMDM/Track</span></span>      |
| <span data-ttu-id="e5858-139">Исполнител</span><span class="sxs-lookup"><span data-stu-id="e5858-139">Artist</span></span>       | <span data-ttu-id="e5858-140">g \_ всзвмдмаусор</span><span class="sxs-lookup"><span data-stu-id="e5858-140">g\_wszWMDMAuthor</span></span>               | <span data-ttu-id="e5858-141">ВМДМ/автор</span><span class="sxs-lookup"><span data-stu-id="e5858-141">WMDM/Author</span></span>     |
| <span data-ttu-id="e5858-142">Музыкальных</span><span class="sxs-lookup"><span data-stu-id="e5858-142">Album</span></span>        | <span data-ttu-id="e5858-143">g \_ всзвмдмалбумтитле</span><span class="sxs-lookup"><span data-stu-id="e5858-143">g\_wszWMDMAlbumTitle</span></span>           | <span data-ttu-id="e5858-144">ВМДМ/Албумтитле</span><span class="sxs-lookup"><span data-stu-id="e5858-144">WMDM/AlbumTitle</span></span> |
| <span data-ttu-id="e5858-145">Year;</span><span class="sxs-lookup"><span data-stu-id="e5858-145">Year</span></span>         | <span data-ttu-id="e5858-146">g \_ всзвмдмеар</span><span class="sxs-lookup"><span data-stu-id="e5858-146">g\_wszWMDMYear</span></span>                 | <span data-ttu-id="e5858-147">ВМДМ в год</span><span class="sxs-lookup"><span data-stu-id="e5858-147">WMDM/Year</span></span>       |
| <span data-ttu-id="e5858-148">Genre</span><span class="sxs-lookup"><span data-stu-id="e5858-148">Genre</span></span>        | <span data-ttu-id="e5858-149">g \_ всзвмдмженре</span><span class="sxs-lookup"><span data-stu-id="e5858-149">g\_wszWMDMGenre</span></span>                | <span data-ttu-id="e5858-150">ВМДМ/жанр</span><span class="sxs-lookup"><span data-stu-id="e5858-150">WMDM/Genre</span></span>      |



 

<span data-ttu-id="e5858-151">Параллелизм</span><span class="sxs-lookup"><span data-stu-id="e5858-151">Concurrency</span></span>

<span data-ttu-id="e5858-152">Драйверы режима ядра для Windows Media диспетчер устройств должны быть надежными при обработке параллельного доступа.</span><span class="sxs-lookup"><span data-stu-id="e5858-152">Kernel mode drivers for Windows Media Device Manager need to be robust in handling concurrent access.</span></span> <span data-ttu-id="e5858-153">Например, пользователь может одновременно получить доступ к устройству через оболочку или проигрыватель мультимедиа или просто через несколько окон в оболочке.</span><span class="sxs-lookup"><span data-stu-id="e5858-153">For example, a user can be concurrently accessing the device through both the shell and media player or simply through multiple windows in the shell.</span></span> <span data-ttu-id="e5858-154">В рамках обработки параллелизма драйверы не должны считаться, только потому что поставщик услуг загружен, что устройство используется.</span><span class="sxs-lookup"><span data-stu-id="e5858-154">As part of handling concurrency, drivers should not assume, just because the service provider is loaded, that the device is in use.</span></span> <span data-ttu-id="e5858-155">Вместо этого они должны реализовать механизм блокировки для сериализации доступа к устройству по мере необходимости для отдельных операций.</span><span class="sxs-lookup"><span data-stu-id="e5858-155">Instead, they should implement a locking mechanism to serialize access to the device as needed for individual operations.</span></span>

<span data-ttu-id="e5858-156">Пользовательский интерфейс</span><span class="sxs-lookup"><span data-stu-id="e5858-156">UI</span></span>

<span data-ttu-id="e5858-157">Поставщики услуг для диспетчер устройств Windows Media не должны отображать пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="e5858-157">Service providers for Windows Media Device Manager should not show any user interface.</span></span> <span data-ttu-id="e5858-158">Все ошибки должны возвращаться из вызовов методов в качестве конкретных кодов ошибок Windows Media диспетчер устройств всякий раз, когда это возможно.</span><span class="sxs-lookup"><span data-stu-id="e5858-158">Any errors should be returned from method calls as specific Windows Media Device Manager error codes whenever possible.</span></span>

<span data-ttu-id="e5858-159">Включение в оболочке</span><span class="sxs-lookup"><span data-stu-id="e5858-159">Enabling in the Shell</span></span>

<span data-ttu-id="e5858-160">Если пакет отвечает всем требованиям оболочки, можно включить отображение устройства в оболочке, задав для параметра *шовиншелл* значение 1 в параметрах устройства.</span><span class="sxs-lookup"><span data-stu-id="e5858-160">If your package meets all of the shell requirements, you can enable your device to be shown in the shell by setting the *ShowInShell* value to 1 under the device parameters.</span></span> <span data-ttu-id="e5858-161">Дополнительные сведения см. в разделе [Параметры устройства](device-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e5858-161">For more information, see [Device Parameters](device-parameters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5858-162">См. также</span><span class="sxs-lookup"><span data-stu-id="e5858-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5858-163">**Создание поставщика услуг**</span><span class="sxs-lookup"><span data-stu-id="e5858-163">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




