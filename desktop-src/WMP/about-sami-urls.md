---
title: Об URL-адресах SAMI
description: Об URL-адресах SAMI
ms.assetid: 6898a0d5-cfd0-4ba5-8cd1-907cf110667c
keywords:
- Проигрыватель Windows Media, синхронизированный доступный медиа-обмен (SAMI)
- Объектная модель проигрывателя Windows Media, синхронизированный доступный обмен мультимедийными данными (SAMI)
- Объектная модель, синхронизированный доступный медиа-обмен (SAMI)
- Проигрыватель Windows Media Mobile, синхронизированный доступный мультимедийный обмен (SAMI)
- Элемент управления ActiveX проигрывателя Windows Media, синхронизированный доступный мультимедийный обмен (SAMI)
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, синхронизированный доступный мультимедийный обмен (SAMI)
- Элемент управления ActiveX, синхронизированный доступный медиа-обмен (SAMI)
- Синхронизированный доступный мультимедийный обмен (SAMI), файлы
- SAMI (синхронизированный доступный медиа-обмен), файлы
- Синхронизированный доступный мультимедийный обмен (SAMI), URL-адреса
- SAMI (синхронизированный доступный мультимедийный обмен), URL-адреса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a41e70d0239b9bdac7d12f9a2dd2f75be15b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253089"
---
# <a name="about-sami-urls"></a><span data-ttu-id="a89c1-114">Об URL-адресах SAMI</span><span class="sxs-lookup"><span data-stu-id="a89c1-114">About SAMI URLs</span></span>

<span data-ttu-id="a89c1-115">Файлы SAMI можно связать с цифровыми файлами мультимедиа с помощью одного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="a89c1-115">SAMI files can be associated with digital media files by using a single URL.</span></span> <span data-ttu-id="a89c1-116">Это достигается с помощью параметра URL-адреса *Sami* .</span><span class="sxs-lookup"><span data-stu-id="a89c1-116">This is accomplished by using *the sami* URL parameter.</span></span> <span data-ttu-id="a89c1-117">Параметру URL предшествует базовый URL-адрес и?</span><span class="sxs-lookup"><span data-stu-id="a89c1-117">The URL parameter is preceded by the base URL and a ?</span></span> <span data-ttu-id="a89c1-118">.</span><span class="sxs-lookup"><span data-stu-id="a89c1-118">character.</span></span> <span data-ttu-id="a89c1-119">URL-адрес с параметром *Sami* следует за следующим синтаксисом:</span><span class="sxs-lookup"><span data-stu-id="a89c1-119">A URL with a *sami* parameter follows this syntax:</span></span>

<span data-ttu-id="a89c1-120">*URL-адрес*? *саамский* = *каптионсурл*.</span><span class="sxs-lookup"><span data-stu-id="a89c1-120">*URL*?*sami*=*captionsURL*.</span></span>

<span data-ttu-id="a89c1-121">Значение параметра URL-адреса соответствует имени параметра и знаку равенства, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="a89c1-121">The value of the URL parameter follows the parameter name and an equals sign, as in the following example:</span></span>


```C++
https://proseware.com/samitest.wma?sami=https://acc.proseware.com/test.smi

```



<span data-ttu-id="a89c1-122">Этот синтаксис URL-адреса обычно используется в гиперссылке или метафайле Windows Media для прямой связи с расположением файла мультимедиа и файла SAMI.</span><span class="sxs-lookup"><span data-stu-id="a89c1-122">This URL syntax is commonly used in a hyperlink or a Windows Media metafile to link directly to the locations of both the digital media file and the SAMI file.</span></span> <span data-ttu-id="a89c1-123">Когда пользователь щелкает гиперссылку, проигрыватель Windows Media запускается в полноэкранном режиме и воспроизводит мультимедийное содержимое.</span><span class="sxs-lookup"><span data-stu-id="a89c1-123">When the user clicks on the hyperlink, Windows Media Player launches in full mode and plays the digital media content.</span></span>

<span data-ttu-id="a89c1-124">Если параметр URL-адреса *Sami* не указан, проигрыватель Windows Media выполнит поиск файла Sami, расположенного в том же расположении, что и файл цифрового мультимедиа, с тем же именем, кроме расширения имени файла, которое должно быть. SMI.</span><span class="sxs-lookup"><span data-stu-id="a89c1-124">If the *sami* URL parameter is not specified, Windows Media Player will look for a SAMI file that is in the same location as the digital media file and that has the same file name except for the file name extension, which must be .smi.</span></span> <span data-ttu-id="a89c1-125">Если такой файл существует, он будет открыт автоматически, если в проигрывателе был включен режим отображения субтитров.</span><span class="sxs-lookup"><span data-stu-id="a89c1-125">If such a file is present, it will be opened automatically if caption display has been enabled in the Player.</span></span>

<span data-ttu-id="a89c1-126">Скрытые субтитры включаются в проигрывателе Windows Media. для этого в меню **Воспроизведение** выберите пункт **субтитры и субтитры**, а затем щелкните **элемент.**</span><span class="sxs-lookup"><span data-stu-id="a89c1-126">Closed captions are enabled in Windows Media Player by clicking the **Play** menu, then clicking **Captions and Subtitles**, and then clicking **On**.</span></span> <span data-ttu-id="a89c1-127">Если включены субтитры, то заголовки, содержащиеся в файле SAMI, будут отображаться во время воспроизведения элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a89c1-127">If closed captions are enabled, the captions contained in the SAMI file will display while the media item plays.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a89c1-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a89c1-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a89c1-129">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="a89c1-129">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




