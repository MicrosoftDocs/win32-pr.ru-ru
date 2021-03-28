---
description: Windows Vista предоставляет более широкие особенности использования файловых эскизов, чем предыдущие версии Windows.
title: Обработчики эскизов
ms.topic: article
ms.date: 07/02/2018
ms.assetid: ed9e17bb-aa28-4f8c-8b5a-9b57cab1c438
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d81accf59401a46dd6b5611e15a67eeec68d5d82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266164"
---
# <a name="thumbnail-handlers"></a><span data-ttu-id="e5745-103">Обработчики эскизов</span><span class="sxs-lookup"><span data-stu-id="e5745-103">Thumbnail Handlers</span></span>

<span data-ttu-id="e5745-104">Windows Vista предоставляет более широкие особенности использования файловых эскизов, чем предыдущие версии Windows.</span><span class="sxs-lookup"><span data-stu-id="e5745-104">Windows Vista makes greater use of file-specific thumbnail images than earlier versions of Windows.</span></span> <span data-ttu-id="e5745-105">Windows Vista использует их во всех представлениях, в диалоговых окнах и для любого типа файлов, который их предоставляет.</span><span class="sxs-lookup"><span data-stu-id="e5745-105">Windows Vista uses them in all views, in dialogs, and for any file type that provides them.</span></span> <span data-ttu-id="e5745-106">Другие приложения также могут использовать эскиз.</span><span class="sxs-lookup"><span data-stu-id="e5745-106">Other applications can consume your thumbnail as well.</span></span> <span data-ttu-id="e5745-107">Отображение эскиза также изменилось.</span><span class="sxs-lookup"><span data-stu-id="e5745-107">Thumbnail display has also changed.</span></span> <span data-ttu-id="e5745-108">Теперь доступен непрерывный спектр размеров, выбираемых пользователем, а не дискретные размеры, такие как значки и эскизы, предоставляемые в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e5745-108">Now, a continuous spectrum of user-selectable sizes is available rather than the discrete sizes such as Icons and Thumbnails provided in Windows XP.</span></span>

> [!Note]  
> <span data-ttu-id="e5745-109">Вы можете услышать эти эскизы, которые называются значками Live.</span><span class="sxs-lookup"><span data-stu-id="e5745-109">You might hear these thumbnails referred to as Live Icons.</span></span>

 

<span data-ttu-id="e5745-110">Эскизы в пользовательском интерфейсе Windows Vista часто используются в виде миниатюр с 32-разрядным разрешением и размером до 256x256 пикселей.</span><span class="sxs-lookup"><span data-stu-id="e5745-110">Thumbnails of 32-bit resolution and as large as 256x256 pixels are often used in Windows Vista UI.</span></span> <span data-ttu-id="e5745-111">Владельцы форматов файлов должны быть готовы к отображению эскизов с таким размером.</span><span class="sxs-lookup"><span data-stu-id="e5745-111">File format owners should be prepared to display their thumbnails at that size.</span></span> <span data-ttu-id="e5745-112">Они также должны предоставлять нестатические изображения для эскизов, отражающих содержимое конкретного файла.</span><span class="sxs-lookup"><span data-stu-id="e5745-112">They should also provide non-static images for their thumbnails that reflect the particular file's contents.</span></span> <span data-ttu-id="e5745-113">Например, эскиз текстового файла должен показывать миниатюрную версию документа, включая его текст.</span><span class="sxs-lookup"><span data-stu-id="e5745-113">For example, a text file's thumbnail should show a miniature version of the document, including its text.</span></span>

<span data-ttu-id="e5745-114">Интерфейс [**исумбнаилпровидер**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) был введен, чтобы сделать эскиз более простым и простым, чем раньше, когда вместо этого было бы использовано [**иекстрактимаже**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) .</span><span class="sxs-lookup"><span data-stu-id="e5745-114">The [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) interface has been introduced to make providing a thumbnail easier and more straightforward than in the past, when [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) would have been used instead.</span></span> <span data-ttu-id="e5745-115">Обратите внимание, что существующий код, использующий **иекстрактимаже** , все еще действует в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e5745-115">Note, that existing code that uses **IExtractImage** is still valid under Windows Vista.</span></span> <span data-ttu-id="e5745-116">Однако **иекстрактимаже** не поддерживается в области **сведений** .</span><span class="sxs-lookup"><span data-stu-id="e5745-116">However, **IExtractImage** is not supported in the **Details** pane.</span></span>

<span data-ttu-id="e5745-117">В этом разделе обсуждается следующее.</span><span class="sxs-lookup"><span data-stu-id="e5745-117">This topic discusses the following:</span></span>

-   [<span data-ttu-id="e5745-118">Эскизы процессов</span><span class="sxs-lookup"><span data-stu-id="e5745-118">Thumbnail Processes</span></span>](#thumbnail-processes)
-   [<span data-ttu-id="e5745-119">Кэш и размер эскиза</span><span class="sxs-lookup"><span data-stu-id="e5745-119">Thumbnail Cache and Sizing</span></span>](#thumbnail-cache-and-sizing)
-   [<span data-ttu-id="e5745-120">Наложение эскизов</span><span class="sxs-lookup"><span data-stu-id="e5745-120">Thumbnail Overlays</span></span>](#thumbnail-overlays)
-   [<span data-ttu-id="e5745-121">Украшения эскизов</span><span class="sxs-lookup"><span data-stu-id="e5745-121">Thumbnail Adornments</span></span>](#thumbnail-adornments)
-   [<span data-ttu-id="e5745-122">Регистрация обработчика эскизов</span><span class="sxs-lookup"><span data-stu-id="e5745-122">Registering Your Thumbnail Handler</span></span>](#registering-your-thumbnail-handler)
-   [<span data-ttu-id="e5745-123">См. также</span><span class="sxs-lookup"><span data-stu-id="e5745-123">Related topics</span></span>](#related-topics)

## <a name="thumbnail-processes"></a><span data-ttu-id="e5745-124">Эскизы процессов</span><span class="sxs-lookup"><span data-stu-id="e5745-124">Thumbnail Processes</span></span>

<span data-ttu-id="e5745-125">Обработчики, включая обработчики эскизов, по умолчанию выполняются в отдельном процессе.</span><span class="sxs-lookup"><span data-stu-id="e5745-125">Handlers, including thumbnail handlers, run by default in a separate process.</span></span> <span data-ttu-id="e5745-126">Можно принудительно запустить обработчик в процессе, передав значение **null** в качестве контекста привязки в вызове [**интерфейса IShellItem:: биндтохандлер**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) , как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="e5745-126">You can force the handler to run in-process by passing a **NULL** value as the bind context in a call to [**IShellItem::BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) as shown here:</span></span>


```
IShellItem::BindToHandler(NULL, BHID_ThumbnailHandler,..)
```



<span data-ttu-id="e5745-127">Можно также отказаться от выполнения процесса по умолчанию, задав в реестре запись Дисаблепроцессисолатион, как показано в этом примере.</span><span class="sxs-lookup"><span data-stu-id="e5745-127">You can also opt out of running out of process by default by setting the DisableProcessIsolation entry in the registry as shown in this example.</span></span> <span data-ttu-id="e5745-128">Идентификатор класса (CLSID) {E357FCCD-A995-4576-B01F-234630154E96} — это CLSID для реализаций [**исумбнаилпровидер**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) .</span><span class="sxs-lookup"><span data-stu-id="e5745-128">The class identifier (CLSID) {E357FCCD-A995-4576-B01F-234630154E96} is the CLSID for [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) implementations.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {E357FCCD-A995-4576-B01F-234630154E96}
         DisableProcessIsolation = 1
```

## <a name="thumbnail-cache-and-sizing"></a><span data-ttu-id="e5745-129">Кэш и размер эскиза</span><span class="sxs-lookup"><span data-stu-id="e5745-129">Thumbnail Cache and Sizing</span></span>

<span data-ttu-id="e5745-130">Когда нужен эскиз, Windows сначала проверяет кэш эскизов для изображения.</span><span class="sxs-lookup"><span data-stu-id="e5745-130">When a thumbnail is needed, Windows first checks the thumbnail cache for the image.</span></span> <span data-ttu-id="e5745-131">Средство извлечения эскизов вызывается, если изображение не найдено в кэше.</span><span class="sxs-lookup"><span data-stu-id="e5745-131">The thumbnail extractor is called if the image is not found in the cache.</span></span> <span data-ttu-id="e5745-132">Он также вызывается, когда время последнего изменения образа позже, чем у копии в кэше.</span><span class="sxs-lookup"><span data-stu-id="e5745-132">It is also called when the last modified time of the image is later than that of the copy in the cache.</span></span>

<span data-ttu-id="e5745-133">Эскизные изображения в этом кэше хранятся в наборе дискретных размеров.</span><span class="sxs-lookup"><span data-stu-id="e5745-133">The thumbnail images in this cache are stored in a set of discrete sizes.</span></span> <span data-ttu-id="e5745-134">Все размеры задаются в пикселях.</span><span class="sxs-lookup"><span data-stu-id="e5745-134">All sizes are given in pixels.</span></span>

-   <span data-ttu-id="e5745-135">32 x 32</span><span class="sxs-lookup"><span data-stu-id="e5745-135">32x32</span></span>
-   <span data-ttu-id="e5745-136">96x96</span><span class="sxs-lookup"><span data-stu-id="e5745-136">96x96</span></span>
-   <span data-ttu-id="e5745-137">256x256</span><span class="sxs-lookup"><span data-stu-id="e5745-137">256x256</span></span>
-   <span data-ttu-id="e5745-138">1024x1024</span><span class="sxs-lookup"><span data-stu-id="e5745-138">1024x1024</span></span>

> [!Note]  
> <span data-ttu-id="e5745-139">Эти значения могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="e5745-139">These values are subject to change.</span></span> <span data-ttu-id="e5745-140">В коде не следует рассчитывать, что любой определенный размер всегда будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="e5745-140">You code should not assume that any particular size will always be used.</span></span>

 

<span data-ttu-id="e5745-141">Если изображение не является квадратным, вы не должны добавлять его самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="e5745-141">If an image is not square, you should not pad it yourself.</span></span> <span data-ttu-id="e5745-142">Windows отвечает за соблюдение исходных пропорций и заполнение изображения до квадратного размера.</span><span class="sxs-lookup"><span data-stu-id="e5745-142">Windows is responsible for respecting the original aspect ratio and padding the image to a square size.</span></span>

<span data-ttu-id="e5745-143">При запросе изображения определенного размера, если не найдено точное соответствие, Windows Vista всегда извлекает следующее самое большое изображение и масштабирует его до требуемого размера.</span><span class="sxs-lookup"><span data-stu-id="e5745-143">When an image of a particular size is asked for, unless an exact match is found, Windows Vista always retrieves the next largest image and scales it down to the requested size.</span></span> <span data-ttu-id="e5745-144">Изображение никогда не масштабируется по размеру, как в предыдущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="e5745-144">An image is never scaled up in size as was the case in previous versions of Windows.</span></span>

<span data-ttu-id="e5745-145">В следующей таблице приведены некоторые примеры связи между запрошенным размером и доступным размером.</span><span class="sxs-lookup"><span data-stu-id="e5745-145">The following table gives some examples of the relationship between requested size and available size.</span></span>



| <span data-ttu-id="e5745-146">Максимальный размер предоставленного образа</span><span class="sxs-lookup"><span data-stu-id="e5745-146">Maximum Image Size You Provide</span></span> | <span data-ttu-id="e5745-147">Размер, запрошенный средством извлечения</span><span class="sxs-lookup"><span data-stu-id="e5745-147">Size Requested by the Extractor</span></span> | <span data-ttu-id="e5745-148">Вы предоставляете</span><span class="sxs-lookup"><span data-stu-id="e5745-148">You Provide</span></span>                                 |
|--------------------------------|---------------------------------|---------------------------------------------|
| <span data-ttu-id="e5745-149">156x120</span><span class="sxs-lookup"><span data-stu-id="e5745-149">156x120</span></span>                        | <span data-ttu-id="e5745-150">256x256</span><span class="sxs-lookup"><span data-stu-id="e5745-150">256x256</span></span>                         | <span data-ttu-id="e5745-151">156x120 (не раскладка, сохранение пропорций)</span><span class="sxs-lookup"><span data-stu-id="e5745-151">156x120 (Do not pad, maintain aspect ratio)</span></span> |
| <span data-ttu-id="e5745-152">2048x1024</span><span class="sxs-lookup"><span data-stu-id="e5745-152">2048x1024</span></span>                      | <span data-ttu-id="e5745-153">256x256</span><span class="sxs-lookup"><span data-stu-id="e5745-153">256x256</span></span>                         | <span data-ttu-id="e5745-154">256x128 (не раскладка, сохранение пропорций)</span><span class="sxs-lookup"><span data-stu-id="e5745-154">256x128 (Do not pad, maintain aspect ratio)</span></span> |



 

<span data-ttu-id="e5745-155">Точку отсечки можно объявить как часть идентификатора программы для связанного приложения в реестре.</span><span class="sxs-lookup"><span data-stu-id="e5745-155">You can declare a cutoff point as part of the program ID entry of the associated app in the registry.</span></span> <span data-ttu-id="e5745-156">Под этим размером эскизы не используются.</span><span class="sxs-lookup"><span data-stu-id="e5745-156">Below this size, thumbnails are not used.</span></span>

```
HKEY_CLASSES_ROOT
   .{ProgId}
      ThumbnailCutoff
```

<span data-ttu-id="e5745-157">Запись Сумбнаилкутофф является одним из этих значений REG \_ .</span><span class="sxs-lookup"><span data-stu-id="e5745-157">The ThumbnailCutoff entry is one of these REG\_DWORD values.</span></span>

| <span data-ttu-id="e5745-158">Значение</span><span class="sxs-lookup"><span data-stu-id="e5745-158">Value</span></span> | <span data-ttu-id="e5745-159">Cutoff</span><span class="sxs-lookup"><span data-stu-id="e5745-159">Cutoff</span></span> | <span data-ttu-id="e5745-160">С учетом Хигхдпи</span><span class="sxs-lookup"><span data-stu-id="e5745-160">HighDPI Sensitive</span></span> |
|-------|--------|-------------------|
| <span data-ttu-id="e5745-161">0</span><span class="sxs-lookup"><span data-stu-id="e5745-161">0</span></span>     | <span data-ttu-id="e5745-162">32 x 32</span><span class="sxs-lookup"><span data-stu-id="e5745-162">32x32</span></span>  | <span data-ttu-id="e5745-163">Да</span><span class="sxs-lookup"><span data-stu-id="e5745-163">Yes</span></span>               |
| <span data-ttu-id="e5745-164">1</span><span class="sxs-lookup"><span data-stu-id="e5745-164">1</span></span>     | <span data-ttu-id="e5745-165">16 x 16</span><span class="sxs-lookup"><span data-stu-id="e5745-165">16x16</span></span>  | <span data-ttu-id="e5745-166">Да</span><span class="sxs-lookup"><span data-stu-id="e5745-166">Yes</span></span>               |
| <span data-ttu-id="e5745-167">2</span><span class="sxs-lookup"><span data-stu-id="e5745-167">2</span></span>     | <span data-ttu-id="e5745-168">48x48</span><span class="sxs-lookup"><span data-stu-id="e5745-168">48x48</span></span>  | <span data-ttu-id="e5745-169">Да</span><span class="sxs-lookup"><span data-stu-id="e5745-169">Yes</span></span>               |
| <span data-ttu-id="e5745-170">3</span><span class="sxs-lookup"><span data-stu-id="e5745-170">3</span></span>     | <span data-ttu-id="e5745-171">16 x 16</span><span class="sxs-lookup"><span data-stu-id="e5745-171">16x16</span></span>  | <span data-ttu-id="e5745-172">Да</span><span class="sxs-lookup"><span data-stu-id="e5745-172">Yes</span></span>               |


<span data-ttu-id="e5745-173">Высокая точка на дюйм (DPI) означает, что размеры изображения в пикселях эскиза автоматически корректируются для более высокого DPI.</span><span class="sxs-lookup"><span data-stu-id="e5745-173">High dots per inch (dpi) sensitivity means that the pixel dimensions of the thumbnail automatically adjust for the greater dpi.</span></span> <span data-ttu-id="e5745-174">Например, изображение размером 32x32 в 96 dpi будет 40x40ным образом в 120 dpi.</span><span class="sxs-lookup"><span data-stu-id="e5745-174">For instance, a 32x32 image at 96 dpi would be a 40x40 image at 120 dpi.</span></span>

<span data-ttu-id="e5745-175">Если запись Сумбнаилкутофф не указана, по умолчанию используется значение 20x20 (без учета DPI).</span><span class="sxs-lookup"><span data-stu-id="e5745-175">If the ThumbnailCutoff entry is not specified, the default cutoff is 20x20 (not dpi-sensitive).</span></span>

## <a name="thumbnail-overlays"></a><span data-ttu-id="e5745-176">Наложение эскизов</span><span class="sxs-lookup"><span data-stu-id="e5745-176">Thumbnail Overlays</span></span>

<span data-ttu-id="e5745-177">Наложение эскизов — небольшое изображение, отображаемое в правом нижнем углу эскиза, предоставляет разработчикам возможность применять фирменную символику к эскизам.</span><span class="sxs-lookup"><span data-stu-id="e5745-177">Thumbnail overlays, a small image displayed over the lower right corner of the thumbnail, provide an opportunity for developers to apply brand identification to their thumbnails.</span></span> <span data-ttu-id="e5745-178">Перекрытия объявляются в реестре как часть идентификатора программы для связанного приложения, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="e5745-178">Overlays are declared in the registry as part of the program ID entry of the associated app, as shown here:</span></span>

```
HKEY_CLASSES_ROOT
   .{ProgId}
      TypeOverlay
```

<span data-ttu-id="e5745-179">Запись Типеоверлай содержит \_ значение reg SZ, интерпретируемое следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e5745-179">The TypeOverlay entry contains a REG\_SZ value interpreted as follows:</span></span>

-   <span data-ttu-id="e5745-180">Если значение является ссылкой на ресурс ( **ICO** -файл, внедренный в библиотеку DLL), например `ISVComponent.dll,-155` , этот образ используется в качестве наложения для файлов с этим расширением имени файла.</span><span class="sxs-lookup"><span data-stu-id="e5745-180">If the value is a resource reference (a **.ico** file embedded in the DLL) such as `ISVComponent.dll,-155`, that image is used as the overlay for files with that file name extension.</span></span> <span data-ttu-id="e5745-181">Обратите внимание, что в этом примере **155** является идентификатором ресурса, а если библиотека DLL отсутствует в стандартном пути (например, **C:/Windows/System32**), вместо имени библиотеки DLL требуется полный путь.</span><span class="sxs-lookup"><span data-stu-id="e5745-181">Note that in this example, **155** is the resouce ID, and if the DLL is not present in a standard path (such as **C:/Windows/System32**), the full path is required instead of just the DLL name.</span></span>
-   <span data-ttu-id="e5745-182">Если значение является пустой строкой, к изображению не применяется наложенный оверлей.</span><span class="sxs-lookup"><span data-stu-id="e5745-182">If the value is an empty string, no overlay is applied to the image.</span></span>
-   <span data-ttu-id="e5745-183">Если значение отсутствует, используется значок связанного приложения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e5745-183">If the value is not present, the default icon of the associated application is used.</span></span>

<span data-ttu-id="e5745-184">Перекрытия для эскизов должны предоставляться только с помощью этого механизма и применяться в Windows.</span><span class="sxs-lookup"><span data-stu-id="e5745-184">Overlays for your thumbnails should only be provided through this mechanism and applied by Windows.</span></span> <span data-ttu-id="e5745-185">Не применяйте перекрытия самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="e5745-185">Do not apply overlays yourself.</span></span>

## <a name="thumbnail-adornments"></a><span data-ttu-id="e5745-186">Украшения эскизов</span><span class="sxs-lookup"><span data-stu-id="e5745-186">Thumbnail Adornments</span></span>

<span data-ttu-id="e5745-187">Декоративные элементы, такие как тени, применяются к эскизам на основе выбранной темы пользователя.</span><span class="sxs-lookup"><span data-stu-id="e5745-187">Adornments such as drop shadows are applied to thumbnails based on the user's currently selected theme.</span></span> <span data-ttu-id="e5745-188">Элементы оформления обеспечиваются Windows; не создавайте их самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="e5745-188">Adornments are provided by Windows; do not create them yourself.</span></span> <span data-ttu-id="e5745-189">Windows может в любое время изменить внешний вид определенных оформлений, поэтому, если вы указали свое владение, вы рискуете не синхронизироваться с системой.</span><span class="sxs-lookup"><span data-stu-id="e5745-189">Windows could change the look of particular adornments at any time, so if you provided you own you would risk falling out of sync with the system.</span></span> <span data-ttu-id="e5745-190">Эскизы могут быть в начале или на месте.</span><span class="sxs-lookup"><span data-stu-id="e5745-190">Your thumbnails could wind up looking dated or out of place.</span></span>

<span data-ttu-id="e5745-191">Потенциальные декоративные элементы объявляются в реестре как часть идентификатора программы для соответствующего приложения, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="e5745-191">Potential adornments are declared in the registry as part of the program ID entry of the associated app, as shown here:</span></span>

```
HKEY_CLASSES_ROOT
   .{ProgId}
      Treatment
```

<span data-ttu-id="e5745-192">Запись лечения содержит одно из следующих значений REG \_ DWORD:</span><span class="sxs-lookup"><span data-stu-id="e5745-192">The Treatment entry contains one of these REG\_DWORD values:</span></span>



| <span data-ttu-id="e5745-193">Значение</span><span class="sxs-lookup"><span data-stu-id="e5745-193">Value</span></span> | <span data-ttu-id="e5745-194">Значение</span><span class="sxs-lookup"><span data-stu-id="e5745-194">Meaning</span></span>         |
|-------|-----------------|
| <span data-ttu-id="e5745-195">0</span><span class="sxs-lookup"><span data-stu-id="e5745-195">0</span></span>     | <span data-ttu-id="e5745-196">Нет оформления</span><span class="sxs-lookup"><span data-stu-id="e5745-196">No Adornment</span></span>    |
| <span data-ttu-id="e5745-197">1</span><span class="sxs-lookup"><span data-stu-id="e5745-197">1</span></span>     | <span data-ttu-id="e5745-198">Тень</span><span class="sxs-lookup"><span data-stu-id="e5745-198">Drop Shadow</span></span>     |
| <span data-ttu-id="e5745-199">2</span><span class="sxs-lookup"><span data-stu-id="e5745-199">2</span></span>     | <span data-ttu-id="e5745-200">Рамка фотографии</span><span class="sxs-lookup"><span data-stu-id="e5745-200">Photo Border</span></span>    |
| <span data-ttu-id="e5745-201">3</span><span class="sxs-lookup"><span data-stu-id="e5745-201">3</span></span>     | <span data-ttu-id="e5745-202">Видео Спроккетс</span><span class="sxs-lookup"><span data-stu-id="e5745-202">Video Sprockets</span></span> |


<span data-ttu-id="e5745-203">К изображениям по умолчанию применяется тень.</span><span class="sxs-lookup"><span data-stu-id="e5745-203">A drop shadow is applied to images by default.</span></span>

## <a name="registering-your-thumbnail-handler"></a><span data-ttu-id="e5745-204">Регистрация обработчика эскизов</span><span class="sxs-lookup"><span data-stu-id="e5745-204">Registering Your Thumbnail Handler</span></span>

<span data-ttu-id="e5745-205">Регистрация обработчика эскиза основана на стандартных сопоставлениях файлов.</span><span class="sxs-lookup"><span data-stu-id="e5745-205">Registration of a thumbnail handler is based on standard file associations.</span></span>

<span data-ttu-id="e5745-206">GUID для расширения оболочки обработчика эскизов — `E357FCCD-A995-4576-B01F-234630154E96` .</span><span class="sxs-lookup"><span data-stu-id="e5745-206">The GUID for the thumbnail handler Shell extension is `E357FCCD-A995-4576-B01F-234630154E96`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5745-207">См. также</span><span class="sxs-lookup"><span data-stu-id="e5745-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5745-208">**исумбнаилпровидер**</span><span class="sxs-lookup"><span data-stu-id="e5745-208">**IThumbnailProvider**</span></span>](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider)
</dt> <dt>

[<span data-ttu-id="e5745-209">Создание обработчиков эскизов</span><span class="sxs-lookup"><span data-stu-id="e5745-209">Building Thumbnail Handlers</span></span>](building-thumbnail-providers.md)
</dt> <dt>

[<span data-ttu-id="e5745-210">Рекомендации по обработке эскизов</span><span class="sxs-lookup"><span data-stu-id="e5745-210">Thumbnail Handler Guidelines</span></span>](thumbnail-provider-guidelines.md)
</dt> </dl>

 

 



