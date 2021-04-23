---
title: Полный код для простой обложки
description: Полный код для простой обложки
ms.assetid: ece437d2-1a11-4096-8b3b-db2b4def8248
keywords:
- Создание обложек, примеры кода
- Обложки проигрывателя Windows Media, примеры кода
- обложки, примеры кода
- файлы определения обложки, примеры кода
- Создание обложек, примеры
- Обложки проигрывателя Windows Media, примеры
- обложки, примеры
- файлы определения обложки, примеры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3682e6143c751d1c72cd8799f849fef7c9c27adb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888679"
---
# <a name="complete-code-for-simple-skin"></a><span data-ttu-id="f515e-111">Полный код для простой обложки</span><span class="sxs-lookup"><span data-stu-id="f515e-111">Complete Code for Simple Skin</span></span>

<span data-ttu-id="f515e-112">Ниже приведен полный код для первого примера обложки:</span><span class="sxs-lookup"><span data-stu-id="f515e-112">Here is the complete code for the first sample skin:</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick="JScript: player.URL='https://proseware.com/laure.wma';" />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick = "JScript: view.close(); " />
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



<span data-ttu-id="f515e-113">Теперь все части объединены.</span><span class="sxs-lookup"><span data-stu-id="f515e-113">Now you have all the pieces put together.</span></span>

<span data-ttu-id="f515e-114">Создайте сжатый файл с расширением ZIP.</span><span class="sxs-lookup"><span data-stu-id="f515e-114">Create a compressed file with a .zip file name extension.</span></span> <span data-ttu-id="f515e-115">Этот сжатый файл содержит файл определения обложки, растровые изображения и любые цифровые файлы мультимедиа, которые необходимо включить.</span><span class="sxs-lookup"><span data-stu-id="f515e-115">This compressed file contains your skin definition file, bitmaps, and any digital media files you want to include.</span></span> <span data-ttu-id="f515e-116">Переименуйте файл, чтобы он был иметь расширение WMZ.</span><span class="sxs-lookup"><span data-stu-id="f515e-116">Rename the file so that it has a .wmz file name extension.</span></span> <span data-ttu-id="f515e-117">Затем дважды щелкните сжатую обложку, чтобы начать играть.</span><span class="sxs-lookup"><span data-stu-id="f515e-117">Then double-clicking your compressed skin will start it playing.</span></span>

<span data-ttu-id="f515e-118">Аналогичные работающие простые обложки можно увидеть в разделе Samples пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="f515e-118">You can see a similar working simple skin in the samples section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f515e-119">См. также</span><span class="sxs-lookup"><span data-stu-id="f515e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f515e-120">**Создание файла определения обложки**</span><span class="sxs-lookup"><span data-stu-id="f515e-120">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




