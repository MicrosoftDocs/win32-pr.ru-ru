---
title: Мастер печати фотографий
description: Мастер печати фотографий помогает пользователям печатать фотографии, предоставляя простой в использовании интерфейс мастера.
ms.assetid: 9cc2c7d4-a2aa-4abc-9c63-b091e044804f
keywords:
- Мастер печати фотографий
- Интерфейс IDropTarget, Мастер печати фотографий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 708f051f658739cebd08e4f8643e5dd7fc0c6f7f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412938"
---
# <a name="photo-printing-wizard"></a><span data-ttu-id="d3a6c-105">Мастер печати фотографий</span><span class="sxs-lookup"><span data-stu-id="d3a6c-105">Photo Printing Wizard</span></span>

<span data-ttu-id="d3a6c-106">Мастер печати фотографий помогает пользователям печатать фотографии, предоставляя простой в использовании интерфейс мастера.</span><span class="sxs-lookup"><span data-stu-id="d3a6c-106">The Photo Printing Wizard helps users print photos by providing an easy-to-use wizard interface.</span></span> <span data-ttu-id="d3a6c-107">Мастер позволяет пользователю указать размеры фотопечати и другие параметры печати, а затем отправить фотографии на принтер.</span><span class="sxs-lookup"><span data-stu-id="d3a6c-107">The wizard enables the user to specify photo print sizes and other print options, and then sends the photos to the printer.</span></span> <span data-ttu-id="d3a6c-108">Мастер разработан таким образом, чтобы его можно было вызывать программно любым приложением, которое хочет предоставить пользователям возможность печатать фотографии и задавать размеры и другие параметры печати.</span><span class="sxs-lookup"><span data-stu-id="d3a6c-108">The wizard is designed so that it can be invoked programmatically by any application that wants to offer users the ability to print photos and specify sizing and other print options.</span></span> <span data-ttu-id="d3a6c-109">Мастер печати фотографий доступен в Windows XP и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d3a6c-109">The Photo Printing Wizard is available on Windows XP and Windows Vista.</span></span>

-   [<span data-ttu-id="d3a6c-110">Функции, предоставляемые мастером печати фотографий</span><span class="sxs-lookup"><span data-stu-id="d3a6c-110">Features Provided by the Photo Print Wizard</span></span>](#features-provided-by-the-photo-print-wizard)
-   [<span data-ttu-id="d3a6c-111">Поддерживаемые форматы файлов фотографий</span><span class="sxs-lookup"><span data-stu-id="d3a6c-111">Supported Photo File Formats</span></span>](#supported-photo-file-formats)
-   [<span data-ttu-id="d3a6c-112">Программный запуск мастера печати фотографий</span><span class="sxs-lookup"><span data-stu-id="d3a6c-112">Programmatically Launching the Photo Print Wizard</span></span>](#programmatically-launching-the-photo-print-wizard)

## <a name="features-provided-by-the-photo-print-wizard"></a><span data-ttu-id="d3a6c-113">Функции, предоставляемые мастером печати фотографий</span><span class="sxs-lookup"><span data-stu-id="d3a6c-113">Features Provided by the Photo Print Wizard</span></span>

<span data-ttu-id="d3a6c-114">Мастер печати фотографий предлагает несколько вариантов, которые могут быть недоступны в общих диалоговых окнах принтера, таких как шаблоны нескольких макетов с точными размерами.</span><span class="sxs-lookup"><span data-stu-id="d3a6c-114">The Photo Printing Wizard offers several options that may not be available on common printer dialogs, such as multi-layout templates with accurate dimensions.</span></span> <span data-ttu-id="d3a6c-115">Шаблоны макета позволяют пользователям максимально эффективно использовать пространство, доступное на фотопринтерной бумаге.</span><span class="sxs-lookup"><span data-stu-id="d3a6c-115">The layout templates enable users to make the most efficient use of the space available on photographic printing paper.</span></span> <span data-ttu-id="d3a6c-116">Другие параметры, которые могут быть заданы или доступны через мастер фотопечати, включают:</span><span class="sxs-lookup"><span data-stu-id="d3a6c-116">Other options that can be specified or accessed through the Photo Print Wizard include:</span></span>

-   <span data-ttu-id="d3a6c-117">Выбор принтера из списка доступных принтеров или назначений виртуальной печати (например, для модуля записи XPS-документов Microsoft).</span><span class="sxs-lookup"><span data-stu-id="d3a6c-117">Selecting a printer from a list of available printers or virtual printing destinations (for example, Microsoft XPS Document Writer).</span></span> <span data-ttu-id="d3a6c-118">В Windows Vista могут быть доступны следующие варианты в зависимости от возможностей принтера или назначения виртуальной печати.</span><span class="sxs-lookup"><span data-stu-id="d3a6c-118">On Windows Vista, the following options may be available, depending on the capabilities of the printer or virtual printing destination:</span></span>
    -   <span data-ttu-id="d3a6c-119">Размер бумаги.</span><span class="sxs-lookup"><span data-stu-id="d3a6c-119">Paper size.</span></span> <span data-ttu-id="d3a6c-120">Например, «Letter», «Legal», «a3».</span><span class="sxs-lookup"><span data-stu-id="d3a6c-120">For example, "Letter", "Legal", "A3".</span></span>
    -   <span data-ttu-id="d3a6c-121">Качество печати с точки зрения поддерживаемых точек на дюйм (DPI).</span><span class="sxs-lookup"><span data-stu-id="d3a6c-121">Print quality, in terms of supported dots per inch (dpi) resolutions.</span></span>
    -   <span data-ttu-id="d3a6c-122">Тип бумаги.</span><span class="sxs-lookup"><span data-stu-id="d3a6c-122">Paper type.</span></span> <span data-ttu-id="d3a6c-123">Например, «Plain» или «глянцевая».</span><span class="sxs-lookup"><span data-stu-id="d3a6c-123">For example, "Plain" or "Glossy".</span></span>
-   <span data-ttu-id="d3a6c-124">Запуск параметров печати и свойств для конкретного принтера.</span><span class="sxs-lookup"><span data-stu-id="d3a6c-124">Launching the printing preferences and properties for a particular printer.</span></span>
-   <span data-ttu-id="d3a6c-125">Задание **копий каждого изображения** (в Windows Vista) или **количество раз для использования каждого** значения регулятора (в Windows XP).</span><span class="sxs-lookup"><span data-stu-id="d3a6c-125">Setting the **Copies of each picture** (on Windows Vista) or **Number of times to use each picture** (on Windows XP) spin box values.</span></span>
-   <span data-ttu-id="d3a6c-126">Указание шаблона макета для печати.</span><span class="sxs-lookup"><span data-stu-id="d3a6c-126">Specifying a print layout template.</span></span> <span data-ttu-id="d3a6c-127">Например, печать **полной страницы** или **печати бумажника**.</span><span class="sxs-lookup"><span data-stu-id="d3a6c-127">For example, **Full page photo** or **Wallet prints**.</span></span>
-   <span data-ttu-id="d3a6c-128">Выбор параметра **вписать изображение в кадр** (доступно только в Windows Vista).</span><span class="sxs-lookup"><span data-stu-id="d3a6c-128">Selecting the **Fit picture to frame** option (available on Windows Vista only).</span></span>
-   <span data-ttu-id="d3a6c-129">Предварительный просмотр распечатанной фотографии с указанными в данный момент параметрами.</span><span class="sxs-lookup"><span data-stu-id="d3a6c-129">Previewing the printed photo with the currently specified options.</span></span>
-   <span data-ttu-id="d3a6c-130">Акцесссинг дополнительные параметры печати, такие как **повышение резкости для управления печатью** и **цветом** (доступно только в Windows Vista).</span><span class="sxs-lookup"><span data-stu-id="d3a6c-130">Accesssing advanced print options, such as **Sharpen for printing** and **Color management** (available on Windows Vista only).</span></span>

<span data-ttu-id="d3a6c-131">Любое приложение может воспользоваться преимуществами функций и возможностей печати фотографий, предлагаемых мастером печати фотографий.</span><span class="sxs-lookup"><span data-stu-id="d3a6c-131">Any application can benefit from the features and photo printing capability offered by the Photo Printing Wizard.</span></span> <span data-ttu-id="d3a6c-132">Приложение может передавать печатаемые файлы.</span><span class="sxs-lookup"><span data-stu-id="d3a6c-132">An application can pass in the files to be printed.</span></span> <span data-ttu-id="d3a6c-133">Затем Мастер печати фотографий позаботится о подготовке файла к печати на основе параметров, указанных пользователем, и отправляет подготовленные файлы на принтер.</span><span class="sxs-lookup"><span data-stu-id="d3a6c-133">The Photo Printing Wizard then takes care of preparing the file for printing based on the options specified by the user and sends the prepared files to the printer.</span></span>

<span data-ttu-id="d3a6c-134">На следующем рисунке показан интерфейс мастера печати фотографий в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d3a6c-134">The following figure shows the Photo Printing Wizard interface on Windows Vista</span></span>

![Мастер печати фотографий в Windows Vista](images/ppw-vista.png)

<span data-ttu-id="d3a6c-136">На следующем рисунке показан интерфейс мастера печати фотографий в Windows XP</span><span class="sxs-lookup"><span data-stu-id="d3a6c-136">The following figure shows the Photo Printing Wizard interface on Windows XP</span></span>

![Мастер печати фотографий в Windows XP](images/ppw-xp.png)

## <a name="supported-photo-file-formats"></a><span data-ttu-id="d3a6c-138">Поддерживаемые форматы файлов фотографий</span><span class="sxs-lookup"><span data-stu-id="d3a6c-138">Supported Photo File Formats</span></span>

<span data-ttu-id="d3a6c-139">В Windows XP мастер фотопечати поддерживает все форматы графических файлов, поддерживаемые Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="d3a6c-139">On Windows XP, the Photo Print Wizard supports all graphics file formats that are supported by Windows GDI+.</span></span> <span data-ttu-id="d3a6c-140">В настоящее время эти форматы файлов включают:</span><span class="sxs-lookup"><span data-stu-id="d3a6c-140">Currently, these file formats include:</span></span>

-   <span data-ttu-id="d3a6c-141">Точечный рисунок (BMP)</span><span class="sxs-lookup"><span data-stu-id="d3a6c-141">Bitmap (BMP)</span></span>
-   <span data-ttu-id="d3a6c-142">GIF</span><span class="sxs-lookup"><span data-stu-id="d3a6c-142">Graphics Interchange Format (GIF)</span></span>
-   <span data-ttu-id="d3a6c-143">JPEG</span><span class="sxs-lookup"><span data-stu-id="d3a6c-143">Joint Photographic Experts Group (JPEG)</span></span>
-   <span data-ttu-id="d3a6c-144">Файл обмена изображениями (EXIF)</span><span class="sxs-lookup"><span data-stu-id="d3a6c-144">Exchangeable Image File (EXIF)</span></span>
-   <span data-ttu-id="d3a6c-145">PNG</span><span class="sxs-lookup"><span data-stu-id="d3a6c-145">Portable Network Graphics (PNG)</span></span>
-   <span data-ttu-id="d3a6c-146">TIFF</span><span class="sxs-lookup"><span data-stu-id="d3a6c-146">Tagged Image File Format (TIFF)</span></span>

<span data-ttu-id="d3a6c-147">Дополнительные сведения о форматах графических файлов, поддерживаемых GDI+, см. в разделе [Типы точечных рисунков](../gdiplus/-gdiplus-types-of-bitmaps-about.md).</span><span class="sxs-lookup"><span data-stu-id="d3a6c-147">For more information about graphics file formats supported by GDI+, see [Types of Bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md).</span></span>

<span data-ttu-id="d3a6c-148">В Windows Vista мастер фотопечати поддерживает любой формат файлов изображений, для которого установлен кодек компонента Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="d3a6c-148">On Windows Vista, the Photo Print Wizard supports any image file format for which a Windows Imaging Component (WIC) codec is installed.</span></span> <span data-ttu-id="d3a6c-149">Компонент WIC предоставляет несколько стандартных кодеков, в том числе:</span><span class="sxs-lookup"><span data-stu-id="d3a6c-149">WIC provides several standard codecs, including:</span></span>

-   <span data-ttu-id="d3a6c-150">Точечный рисунок (BMP)</span><span class="sxs-lookup"><span data-stu-id="d3a6c-150">Bitmap (BMP)</span></span>
-   <span data-ttu-id="d3a6c-151">GIF</span><span class="sxs-lookup"><span data-stu-id="d3a6c-151">GIF</span></span>
-   <span data-ttu-id="d3a6c-152">Формат значка (ICO)</span><span class="sxs-lookup"><span data-stu-id="d3a6c-152">Icon Format (ICO)</span></span>
-   <span data-ttu-id="d3a6c-153">JPEG</span><span class="sxs-lookup"><span data-stu-id="d3a6c-153">JPEG</span></span>
-   <span data-ttu-id="d3a6c-154">PNG</span><span class="sxs-lookup"><span data-stu-id="d3a6c-154">PNG</span></span>
-   <span data-ttu-id="d3a6c-155">TIFF</span><span class="sxs-lookup"><span data-stu-id="d3a6c-155">TIFF</span></span>
-   <span data-ttu-id="d3a6c-156">Формат фотографии Windows Media</span><span class="sxs-lookup"><span data-stu-id="d3a6c-156">Windows Media Photo format</span></span>

<span data-ttu-id="d3a6c-157">Дополнительные сведения о кодеках WIC и WIC см. в разделе [компонент Windows Imaging](https://msdn.microsoft.com/library/ms737408(VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="d3a6c-157">For more information about WIC and WIC codecs, see [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx)</span></span>

## <a name="programmatically-launching-the-photo-print-wizard"></a><span data-ttu-id="d3a6c-158">Программный запуск мастера печати фотографий</span><span class="sxs-lookup"><span data-stu-id="d3a6c-158">Programmatically Launching the Photo Print Wizard</span></span>

<span data-ttu-id="d3a6c-159">Чтобы вызвать мастер печати фотографий, вызовите интерфейс [интерфейс IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) со следующим идентификатором класса (CLSID):</span><span class="sxs-lookup"><span data-stu-id="d3a6c-159">To invoke the Photo Printing Wizard, call the [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface with the following class identifier (CLSID):</span></span>


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
```



<span data-ttu-id="d3a6c-160">Файлы, которые должны быть обработаны мастером печати фотографий, указываются в объекте [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="d3a6c-160">The files to be processed by the Photo Printing Wizard are specified in an [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) object.</span></span>

<span data-ttu-id="d3a6c-161">В следующем примере кода показано, как вызвать мастер печати фотографий.</span><span class="sxs-lookup"><span data-stu-id="d3a6c-161">The following code example demonstrates how to invoke the Photo Printing Wizard.</span></span>


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
            
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PrintPhotosDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



 

 