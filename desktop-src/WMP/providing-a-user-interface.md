---
title: Предоставление пользовательского интерфейса
description: Предоставление пользовательского интерфейса
ms.assetid: 43a0cfea-4f35-4c4a-97f5-a3787b597dc5
keywords:
- Подключаемые модули проигрывателя Windows Media, страницы свойств
- подключаемые модули, страницы свойств
- подключаемые модули обработки цифровых сигналов, страницы свойств
- Подключаемые модули DSP, страницы свойств
- подключаемые модули обработки цифровых сигналов, Пользовательский интерфейс
- Подключаемые модули DSP, Пользовательский интерфейс
- страницы свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d708d1256faf7096d15a7596a9635a33173d22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258823"
---
# <a name="providing-a-user-interface"></a><span data-ttu-id="e8a17-110">Предоставление пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="e8a17-110">Providing a User Interface</span></span>

<span data-ttu-id="e8a17-111">Подключаемые модули DSP могут предоставить страницу свойств для создания пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e8a17-111">DSP plug-ins can provide a property page to create a user interface.</span></span> <span data-ttu-id="e8a17-112">Для этого подключаемый модуль должен содержать объект страницы свойств, предоставляющий реализацию интерфейса **ипропертипаже** .</span><span class="sxs-lookup"><span data-stu-id="e8a17-112">To do this, the plug-in must include a property page object that provides an implementation of an **IPropertyPage** interface.</span></span> <span data-ttu-id="e8a17-113">Подключаемый объект DSP должен реализовывать **испеЦифипропертипажес::** GetObject, что позволяет проигрывателю Windows Media находить и определять правильную страницу свойств для подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="e8a17-113">The DSP plug-in object must implement **ISpecifyPropertyPages::GetPages**, which allows Windows Media Player to locate and identify the correct property page for the plug-in.</span></span>

<span data-ttu-id="e8a17-114">**Отображение изображения состояния**</span><span class="sxs-lookup"><span data-stu-id="e8a17-114">**Displaying a Status Graphic**</span></span>

<span data-ttu-id="e8a17-115">Подключаемые модули DSP могут отображать небольшое изображение или ряд графических изображений в области состояния проигрывателя Windows Media, чтобы уведомить пользователя о том, что подключаемый модуль активен.</span><span class="sxs-lookup"><span data-stu-id="e8a17-115">DSP plug-ins can display a small graphic, or series of graphics, in the Windows Media Player status area to notify the user that a plug-in is active.</span></span> <span data-ttu-id="e8a17-116">Для поддержки этой функции подключаемый модуль должен реализовать интерфейс **ипропертибаг** .</span><span class="sxs-lookup"><span data-stu-id="e8a17-116">To support this feature, the plug-in must implement the **IPropertyBag** interface.</span></span> <span data-ttu-id="e8a17-117">Проигрыватель Windows Media вызывает **ипропертибаг:: Read**, предоставляя указатель на имя запрошенного свойства "иконстреамс", которое учитывает регистр, и указатель на структуру **Variant** , которая получает данные для графика.</span><span class="sxs-lookup"><span data-stu-id="e8a17-117">Windows Media Player calls **IPropertyBag::Read**, providing a pointer to the requested property name "IconStreams", which is case-sensitive, and a pointer to a **VARIANT** structure that receives the data for the graphic.</span></span> <span data-ttu-id="e8a17-118">Подключаемый модуль создает объект **IStream** (или SafeArray объектов **IStream** , если имеется несколько изображений), затем загружает графические данные, включая сведения о заголовке, в поток, а затем возвращает указатель на объект **IStream** , используя элемент **пунквал** структуры **Variant** .</span><span class="sxs-lookup"><span data-stu-id="e8a17-118">The plug-in creates an **IStream** object (or a SAFEARRAY of **IStream** objects if there are multiple graphics), then loads the graphic data, including header information, into the stream, and then returns a pointer to the **IStream** object using the **punkVal** member of the **VARIANT** structure.</span></span> <span data-ttu-id="e8a17-119">Если подключаемый модуль предоставляет только один рисунок, он указывает элемент **VT** в структуре **Variant** как VT \_ Unknown.</span><span class="sxs-lookup"><span data-stu-id="e8a17-119">If the plug-in supplies only one graphic, it specifies the **vt** member of the **VARIANT** structure as VT\_UNKNOWN.</span></span> <span data-ttu-id="e8a17-120">Если подключаемый модуль предоставляет несколько графических объектов **IStream** , использующих SAFEARRAY, он задает элемент **VT** в структуре **Variant** в качестве \_ массива VT.</span><span class="sxs-lookup"><span data-stu-id="e8a17-120">If the plug-in supplies multiple graphic **IStream** objects using a SAFEARRAY, it specifies the **vt** member of the **VARIANT** structure as VT\_ARRAY.</span></span>

<span data-ttu-id="e8a17-121">Графика может храниться в различных форматах файлов, включая:</span><span class="sxs-lookup"><span data-stu-id="e8a17-121">Graphics can be stored in a variety of file formats, including:</span></span>

<span data-ttu-id="e8a17-122">**BMP**</span><span class="sxs-lookup"><span data-stu-id="e8a17-122">**BMP**</span></span>

<span data-ttu-id="e8a17-123">Изображения точечных рисунков Microsoft Windows несжаты.</span><span class="sxs-lookup"><span data-stu-id="e8a17-123">Microsoft Windows Bitmap images are uncompressed.</span></span>

<span data-ttu-id="e8a17-124">**JPEG**</span><span class="sxs-lookup"><span data-stu-id="e8a17-124">**JPEG**</span></span>

<span data-ttu-id="e8a17-125">Сжатый формат изображения, обычно используемый для веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="e8a17-125">Compressed image format commonly used for webpages.</span></span> <span data-ttu-id="e8a17-126">Файлы формата JPEG обычно имеют расширение JPG.</span><span class="sxs-lookup"><span data-stu-id="e8a17-126">JPEG format files usually have .jpg file name extensions.</span></span>

<span data-ttu-id="e8a17-127">**GIF**</span><span class="sxs-lookup"><span data-stu-id="e8a17-127">**GIF**</span></span>

<span data-ttu-id="e8a17-128">Сжатый формат изображения, обычно используемый для веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="e8a17-128">Compressed image format commonly used for webpages.</span></span>

<span data-ttu-id="e8a17-129">**ФАЙЛЕ**</span><span class="sxs-lookup"><span data-stu-id="e8a17-129">**PNG**</span></span>

<span data-ttu-id="e8a17-130">Сжатый формат изображения, обычно используемый для веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="e8a17-130">Compressed image format commonly used for webpages.</span></span>

<span data-ttu-id="e8a17-131">Максимальное количество измерений для графических элементов DSP составляет 38 пикселей в ширину и 14 пикселей в высоком масштабе.</span><span class="sxs-lookup"><span data-stu-id="e8a17-131">The maximum dimensions for DSP plug-in graphics are 38 pixels wide and 14 pixels high.</span></span>

<span data-ttu-id="e8a17-132">Байтовый поток **IStream** , содержащий изображение состояния, должен включать сведения о заголовке.</span><span class="sxs-lookup"><span data-stu-id="e8a17-132">The **IStream** byte stream containing the status graphic must include header information.</span></span> <span data-ttu-id="e8a17-133">Без сведений о заголовке проигрыватель Windows Media не может правильно определить тип графика, поэтому не будет загружать изображение.</span><span class="sxs-lookup"><span data-stu-id="e8a17-133">Without header information, Windows Media Player cannot properly identify the type of graphic and therefore will not load the image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8a17-134">См. также</span><span class="sxs-lookup"><span data-stu-id="e8a17-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8a17-135">**Обзор подключаемого модуля DSP**</span><span class="sxs-lookup"><span data-stu-id="e8a17-135">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




