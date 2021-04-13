---
title: Создание файла регионов
description: Создание файла регионов
ms.assetid: e901dfa1-1e06-4136-b877-64be03107f6f
keywords:
- Обложки мобильных приложений проигрывателя Windows Media, файлы регионов
- обложки, файлы регионов
- Создание обложек, файлов регионов
- Файлы регионов в обложках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bf3268b101255191bef4b3e4c4880e2bb846414
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328712"
---
# <a name="creating-the-region-file"></a><span data-ttu-id="cef0a-107">Создание файла регионов</span><span class="sxs-lookup"><span data-stu-id="cef0a-107">Creating the Region File</span></span>

<span data-ttu-id="cef0a-108">Вам потребуется создать файл области, который показывает, какие области реагируют на касания.</span><span class="sxs-lookup"><span data-stu-id="cef0a-108">You will want to create a Region file that shows what areas respond to taps.</span></span> <span data-ttu-id="cef0a-109">Можно просто скопировать базовые уровни каждого элемента в новый слой и окрасить их в соответствии с цветовыми номерами, которые будут использоваться в файле определения обложки.</span><span class="sxs-lookup"><span data-stu-id="cef0a-109">You can simply copy the base layers of each element to a new layer, and color them to correspond to the color numbers you will use in the skin definition file.</span></span> <span data-ttu-id="cef0a-110">Убедитесь, что изображения, создаваемые на этом слое, являются сплошными и никакие эффекты не применяются.</span><span class="sxs-lookup"><span data-stu-id="cef0a-110">Be sure that the images you create in this layer are solid and that no effects are applied.</span></span> <span data-ttu-id="cef0a-111">Вы, вероятно, захотите записать цветовые номера для каждого изображения.</span><span class="sxs-lookup"><span data-stu-id="cef0a-111">You will probably want to write down the color numbers for each image.</span></span> <span data-ttu-id="cef0a-112">Цветовые номера можно получить с помощью средства выбора цвета Photoshop.</span><span class="sxs-lookup"><span data-stu-id="cef0a-112">You can get the color numbers from the Photoshop Color Picker.</span></span> <span data-ttu-id="cef0a-113">Необходимо, чтобы число RGB было равно трем десятичным числам.</span><span class="sxs-lookup"><span data-stu-id="cef0a-113">You want the RGB numbers, which are three decimal numbers.</span></span> <span data-ttu-id="cef0a-114">Каждое число в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="cef0a-114">Each number ranges from 0 to 255.</span></span> <span data-ttu-id="cef0a-115">Например, сплошной красный цвет будет 255, 0, 0.</span><span class="sxs-lookup"><span data-stu-id="cef0a-115">For example, a solid red would be 255, 0, 0.</span></span>

> [!Note]  
> <span data-ttu-id="cef0a-116">Файлы регионов не используются в обложек проигрывателя Windows Media 10 для мобильных устройств, так как типы кнопок не поддерживаются в проигрывателе Windows Media 10 Mobile или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="cef0a-116">Region files are not used in Windows Media Player 10 Mobile skins because button types are not supported in Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="cef0a-117">На следующем рисунке изображен файл регионов.</span><span class="sxs-lookup"><span data-stu-id="cef0a-117">The following image is the Region file.</span></span>

![файл региона](images/ceswmreg.png)

<span data-ttu-id="cef0a-119">В этом файле есть только четыре изображения, так как кнопки Плайпаусе, «останов», «далее» и «назад» являются кнопками типа «курсор».</span><span class="sxs-lookup"><span data-stu-id="cef0a-119">There are only four images in this file because only the PlayPause, Stop, Next, and Prev buttons are hit-type buttons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cef0a-120">См. также</span><span class="sxs-lookup"><span data-stu-id="cef0a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cef0a-121">**Создание рисунка**</span><span class="sxs-lookup"><span data-stu-id="cef0a-121">**Creating the Art**</span></span>](creating-the-art.md)
</dt> </dl>

 

 




