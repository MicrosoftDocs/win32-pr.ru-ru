---
title: Файлы изображений
description: Файлы изображений
ms.assetid: 93893610-de8d-4b9a-b23d-75ddb3e1e557
keywords:
- Обложки проигрывателя Windows Media, графические файлы
- обложки, файлы Art
- файлы для обложек, изображений
- графические файлы для обложки, о
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a246ac411a3dfe2c5bab529ddcccce5596434617
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691366"
---
# <a name="art-files"></a><span data-ttu-id="fdb00-107">Файлы изображений</span><span class="sxs-lookup"><span data-stu-id="fdb00-107">Art Files</span></span>

<span data-ttu-id="fdb00-108">Для обложки необходимо создать один или несколько графических файлов.</span><span class="sxs-lookup"><span data-stu-id="fdb00-108">You must create one or more art files for your skin.</span></span> <span data-ttu-id="fdb00-109">Без рисунка у пользователя не будет ничего взглянуть на.</span><span class="sxs-lookup"><span data-stu-id="fdb00-109">Without art, the user will have nothing to look at.</span></span> <span data-ttu-id="fdb00-110">Можно создать невидимую обложку, но никто не увидит ее.</span><span class="sxs-lookup"><span data-stu-id="fdb00-110">You could create an invisible skin, but no one would see it!</span></span> <span data-ttu-id="fdb00-111">И даже затем придется создавать файлы изображений для размещения невидимых изображений, так как для файла определения обложки требуются графические файлы для конкретных элементов.</span><span class="sxs-lookup"><span data-stu-id="fdb00-111">And even then, you would still have to create art files to hold your invisible images, because the skin definition file requires art files for specific elements.</span></span>

<span data-ttu-id="fdb00-112">Существует три способа использования иллюстрации в обложках: основные образы, изображения сопоставления и альтернативные изображения.</span><span class="sxs-lookup"><span data-stu-id="fdb00-112">There are three uses for art in skins: primary images, mapping images, and alternate images.</span></span>

## <a name="primary-images"></a><span data-ttu-id="fdb00-113">Основные образы</span><span class="sxs-lookup"><span data-stu-id="fdb00-113">Primary Images</span></span>

<span data-ttu-id="fdb00-114">Необходимо создать основной образ для обложки.</span><span class="sxs-lookup"><span data-stu-id="fdb00-114">You must create a primary image for your skin.</span></span> <span data-ttu-id="fdb00-115">Это то, что пользователи увидят при установке обложки.</span><span class="sxs-lookup"><span data-stu-id="fdb00-115">This is what the users will see when they install your skin.</span></span> <span data-ttu-id="fdb00-116">Основной образ состоит из одного или нескольких образов, созданных конкретными элементами управления обложки.</span><span class="sxs-lookup"><span data-stu-id="fdb00-116">The primary image is composed of one or more images that are created by specific skin controls.</span></span>

<span data-ttu-id="fdb00-117">При наличии нескольких элементов управления необходимо указать z-порядок, который определяет, какие элементы управления отображаются перед другими элементами управления.</span><span class="sxs-lookup"><span data-stu-id="fdb00-117">If you have more than one control, you must specify the z-order, which defines which controls are displayed in front of other controls.</span></span> <span data-ttu-id="fdb00-118">Каждый элемент **представления** будет иметь фоновое изображение, в которое можно добавить другие изображения элементов в, что позволит создать первичный составной образ.</span><span class="sxs-lookup"><span data-stu-id="fdb00-118">Each **View** element will have a background image that you can add other element images to, allowing you to create a primary composite image.</span></span>

<span data-ttu-id="fdb00-119">Кроме того, могут иметься дополнительные образы, например скользящий лоток, который не отображается при первом отображении обложки, но отображается, когда пользователь выполняет какое-либо действие.</span><span class="sxs-lookup"><span data-stu-id="fdb00-119">You also may have secondary images, such as a sliding tray, that do not display when your skin first appears, but that show up when the user takes some action.</span></span> <span data-ttu-id="fdb00-120">Они следуют тем же правилам, что и основные образы, в том, что они создаются с помощью набора элементов управления.</span><span class="sxs-lookup"><span data-stu-id="fdb00-120">These follow the same rules as primary images, in that they are created with a set of controls.</span></span>

## <a name="mapping-images"></a><span data-ttu-id="fdb00-121">Сопоставление изображений</span><span class="sxs-lookup"><span data-stu-id="fdb00-121">Mapping Images</span></span>

<span data-ttu-id="fdb00-122">Одной из самых эффективных функций обложек проигрывателя Windows Media является возможность использовать сопоставление изображений для активации событий для обложки.</span><span class="sxs-lookup"><span data-stu-id="fdb00-122">One of the most powerful features of Windows Media Player skins is that you can use image mapping to trigger events for your skin.</span></span> <span data-ttu-id="fdb00-123">Карты изображений — это файлы, содержащие специальные образы.</span><span class="sxs-lookup"><span data-stu-id="fdb00-123">Image maps are files that contain special images.</span></span> <span data-ttu-id="fdb00-124">Однако изображения в файле отображения изображений не предназначены для просмотра пользователем, но используются проигрывателем Windows Media для выполнения действий, когда пользователь щелкает обложку.</span><span class="sxs-lookup"><span data-stu-id="fdb00-124">The images in an image map file, however, are not meant to be viewed by the user, but are used by Windows Media Player to take action when the user clicks on your skin.</span></span>

<span data-ttu-id="fdb00-125">Различным элементам управления требуются различные типы карт изображений.</span><span class="sxs-lookup"><span data-stu-id="fdb00-125">Different controls need different kinds of image maps.</span></span> <span data-ttu-id="fdb00-126">Например, если цветная часть изображения соответствует определенному красному значению, а пользователь щелкает соответствующую область основного изображения, то кнопка будет срабатывать на событие.</span><span class="sxs-lookup"><span data-stu-id="fdb00-126">For example, if you color part of an image map a specific red value, and the user clicks on the corresponding area of your primary image, a button will fire an event.</span></span> <span data-ttu-id="fdb00-127">Цвет используется для определения событий, которые вызываются щелчком в определенной области обложки.</span><span class="sxs-lookup"><span data-stu-id="fdb00-127">Color is used to define which events are triggered by clicking in a particular area of the skin.</span></span>

## <a name="alternate-images"></a><span data-ttu-id="fdb00-128">Альтернативные образы</span><span class="sxs-lookup"><span data-stu-id="fdb00-128">Alternate Images</span></span>

<span data-ttu-id="fdb00-129">Кроме того, можно настроить отображение альтернативных изображений, когда пользователь выполняет какие-либо действия.</span><span class="sxs-lookup"><span data-stu-id="fdb00-129">You can also set up alternate images to display when a user does something.</span></span> <span data-ttu-id="fdb00-130">Например, можно создать альтернативное изображение кнопки, которое будет отображаться только при наведении указателя мыши на кнопку.</span><span class="sxs-lookup"><span data-stu-id="fdb00-130">For example, you can create an alternate image of a button that will be displayed only when the mouse hovers over the button.</span></span> <span data-ttu-id="fdb00-131">Это хороший способ предоставить пользователям сведения о том, что они могут делать, а также предоставляет возможность легко обнаруживаемого пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fdb00-131">This is a good way to let users know what they can do, and also allows for a highly discoverable user interface.</span></span> <span data-ttu-id="fdb00-132">При тщательном использовании всплывающих подсказок и изображений для наведения можно создавать необычные пользовательские интерфейсы, которые по-прежнему предоставляют пользователю Отзывы о доступных параметрах.</span><span class="sxs-lookup"><span data-stu-id="fdb00-132">By using ToolTips and hover images carefully, you can create unusual user interfaces that still give the user feedback about what options are available.</span></span>

<span data-ttu-id="fdb00-133">В следующих разделах содержатся дополнительные сведения о графических файлах.</span><span class="sxs-lookup"><span data-stu-id="fdb00-133">The following sections provide more information about art files:</span></span>

-   [<span data-ttu-id="fdb00-134">Основные образы</span><span class="sxs-lookup"><span data-stu-id="fdb00-134">Primary Images</span></span>](primary-images.md)
-   [<span data-ttu-id="fdb00-135">Сопоставление изображений</span><span class="sxs-lookup"><span data-stu-id="fdb00-135">Mapping Images</span></span>](mapping-images.md)
-   [<span data-ttu-id="fdb00-136">Альтернативные образы</span><span class="sxs-lookup"><span data-stu-id="fdb00-136">Alternate Images</span></span>](alternate-images.md)
-   [<span data-ttu-id="fdb00-137">Форматы файлов изображений</span><span class="sxs-lookup"><span data-stu-id="fdb00-137">Art File Formats</span></span>](art-file-formats.md)
-   [<span data-ttu-id="fdb00-138">Пример простой иллюстрации</span><span class="sxs-lookup"><span data-stu-id="fdb00-138">Simple Art Example</span></span>](simple-art-example.md)

## <a name="related-topics"></a><span data-ttu-id="fdb00-139">См. также</span><span class="sxs-lookup"><span data-stu-id="fdb00-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdb00-140">**Файлы обложки**</span><span class="sxs-lookup"><span data-stu-id="fdb00-140">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 




