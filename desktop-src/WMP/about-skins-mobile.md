---
title: О обложках (мобильный)
description: Сведения об обложках для мобильных игроков. Обложка — это настраиваемый пользовательский интерфейс для проигрывателя Windows Media.
ms.assetid: 105c11ce-705b-4a0c-8982-d0f9dd9ae3ac
keywords:
- Проигрыватель Windows Media Mobile, обложки
- Обложки Windows Media Player для мобильных устройств, о
- Обложки Windows Media Player для мобильных устройств, создание
- обложки, проигрыватель Windows Media Mobile
- Создание обложек, проигрыватель Windows Media Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebdffdc4075456c6cb7ccf9d1940c5253c732cd3
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011227"
---
# <a name="about-skins-mobile"></a><span data-ttu-id="805a8-109">О обложках (мобильный)</span><span class="sxs-lookup"><span data-stu-id="805a8-109">About Skins (Mobile)</span></span>

<span data-ttu-id="805a8-110">Обложка — это настраиваемый пользовательский интерфейс для проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="805a8-110">A skin is a customized user interface to Windows Media Player.</span></span> <span data-ttu-id="805a8-111">Вы можете создавать собственные кнопки для запуска и окончания воспроизведения цифровых носителей, добавлять ползунки для изменения громкости и воспроизведения в элементе мультимедиа, а также предоставлять пользователю текстовую информацию, например имя песни.</span><span class="sxs-lookup"><span data-stu-id="805a8-111">You can create your own buttons to start and stop playback of digital media, add sliders to change volume and playback position in the media item, and provide the user with text information such as the name of a song.</span></span> <span data-ttu-id="805a8-112">Что лучше всего, можно добавить собственную иллюстрацию или использовать существующую иллюстрацию, чтобы создать уникальный внешний вид для обложки.</span><span class="sxs-lookup"><span data-stu-id="805a8-112">Best of all, you can add your own artwork or use existing art to create a unique appearance for your skin.</span></span>

<span data-ttu-id="805a8-113">Ниже приведены основные шаги по созданию обложки.</span><span class="sxs-lookup"><span data-stu-id="805a8-113">The basic steps in creating a skin are:</span></span>

1.  <span data-ttu-id="805a8-114">**Проектирование** пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="805a8-114">**Design** your user interface.</span></span> <span data-ttu-id="805a8-115">Определите, какие кнопки, текстовые поля и ползунки должны быть предоставлены пользователю, чтобы они могли управлять функциями, выбранными на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="805a8-115">Decide which buttons, text boxes, and trackbars you want to provide to the user so that they can control the functions you chose in step 1.</span></span> <span data-ttu-id="805a8-116">Вы можете запланировать свои идеи, чтобы увидеть, как они соответствуют размеру образа, с которым вы будете работать.</span><span class="sxs-lookup"><span data-stu-id="805a8-116">You may want to sketch out your ideas to see how they fit on the image size you will be working with.</span></span>
2.  <span data-ttu-id="805a8-117">**Создайте** рисунок, который будет отображаться для пользователя.</span><span class="sxs-lookup"><span data-stu-id="805a8-117">**Create** the art you want to show the user.</span></span> <span data-ttu-id="805a8-118">Это будет состоять из нескольких изображений, в которых отображаются фоновые изображения, другие изображения, которые вы хотите отобразить, и сопоставление изображений при использовании кнопок области.</span><span class="sxs-lookup"><span data-stu-id="805a8-118">This will consist of several images that show the background images, other images you may want to display, and mapping images if you use region buttons.</span></span>
3.  <span data-ttu-id="805a8-119">**Напишите** файл определения обложки, который будет связывать функции цифрового мультимедиа, Пользовательский интерфейс и изображения.</span><span class="sxs-lookup"><span data-stu-id="805a8-119">**Write** the skin definition file that will link together the digital media functions, user interface, and images.</span></span> <span data-ttu-id="805a8-120">Необходимо соблюдать определенные правила ввода текстовых данных в файл, но вы можете взглянуть на обложку по умолчанию в качестве инструкции.</span><span class="sxs-lookup"><span data-stu-id="805a8-120">You must follow certain rules for entering the text data into the file, but you can look at the default skin as a guide.</span></span>

<span data-ttu-id="805a8-121">Вам не нужно выполнять эти действия в указанном порядке, но хорошая структура будет относиться к отсчету всех возможностей и позаботиться обо всех деталях.</span><span class="sxs-lookup"><span data-stu-id="805a8-121">You do not need to follow these steps in the order given, but a good design will come from being aware of all the possibilities and taking care of all the details.</span></span>

<span data-ttu-id="805a8-122">В следующих разделах содержатся подробные сведения о обложках.</span><span class="sxs-lookup"><span data-stu-id="805a8-122">The following sections provide detailed information about skins.</span></span>



| <span data-ttu-id="805a8-123">Section</span><span class="sxs-lookup"><span data-stu-id="805a8-123">Section</span></span>                                                                                    | <span data-ttu-id="805a8-124">Описание</span><span class="sxs-lookup"><span data-stu-id="805a8-124">Description</span></span>                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="805a8-125">Сведения о совместимости</span><span class="sxs-lookup"><span data-stu-id="805a8-125">About Compatibility</span></span>](about-compatibility.md)                                             | <span data-ttu-id="805a8-126">Список различных версий проигрывателя Windows Media Mobile, требования к оборудованию, доступность проигрывателя Windows Media и функции обложки, появившиеся для каждой версии программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="805a8-126">Lists the different versions of Windows Media Player Mobile, the hardware requirements, availability of Windows Media Player, and the skin features introduced for each version of the software.</span></span> |
| [<span data-ttu-id="805a8-127">Мобильные функции проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="805a8-127">Windows Media Player Mobile Functionality</span></span>](windows-media-player-mobile-functionality.md) | <span data-ttu-id="805a8-128">Описывает функции, которые может поддерживать обложка.</span><span class="sxs-lookup"><span data-stu-id="805a8-128">Describes the features your skin can support.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="805a8-129">Элементы пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="805a8-129">User Interface Elements</span></span>](user-interface-elements.md)                                     | <span data-ttu-id="805a8-130">Описание элементов пользовательского интерфейса, которые можно создать для обложки, таких как кнопки, линейки и экраны видео.</span><span class="sxs-lookup"><span data-stu-id="805a8-130">Describes the user interface elements you can create for your skin, such as buttons, trackbars, and video displays.</span></span>                                                                              |
| [<span data-ttu-id="805a8-131">Файлы изображений</span><span class="sxs-lookup"><span data-stu-id="805a8-131">Art Files</span></span>](art-files-mobile.md)                                                          | <span data-ttu-id="805a8-132">Описание графических файлов, создаваемых для обложки.</span><span class="sxs-lookup"><span data-stu-id="805a8-132">Describes the art files you create for your skin.</span></span>                                                                                                                                                |
| [<span data-ttu-id="805a8-133">Файл определения обложки</span><span class="sxs-lookup"><span data-stu-id="805a8-133">Skin Definition File</span></span>](skin-definition-file-mobile.md)                                    | <span data-ttu-id="805a8-134">Описывает файл, который необходимо создать для описания обложки.</span><span class="sxs-lookup"><span data-stu-id="805a8-134">Describes the file you must create to describe your skin.</span></span>                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="805a8-135">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="805a8-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="805a8-136">**Обложки мобильных устройств проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="805a8-136">**Windows Media Player Mobile Skins**</span></span>](windows-media-player-mobile-skins.md)
</dt> </dl>

 

 




