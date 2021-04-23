---
title: Запись потоков изображений
description: Запись потоков изображений
ms.assetid: 3a017bdd-9723-4b7f-b5e1-22838c0ba4ff
keywords:
- Расширенный системный формат (ASF), написание потоков изображений
- ASF (Расширенный системный формат), запись потоков изображений
- Расширенный системный формат (ASF), потоки изображений
- ASF (Расширенный системный формат), потоки изображений
- потоки изображений, запись
- потоки, запись потоков изображений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60daa9b62701c172d127c4cff1fb6c301edf7d86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103987198"
---
# <a name="writing-image-streams"></a><span data-ttu-id="6717a-109">Запись потоков изображений</span><span class="sxs-lookup"><span data-stu-id="6717a-109">Writing Image Streams</span></span>

<span data-ttu-id="6717a-110">Входные данные для потока изображений должны быть битовыми изображениями в формате RGB.</span><span class="sxs-lookup"><span data-stu-id="6717a-110">The inputs for an image stream must be RGB-formatted bitmap images.</span></span> <span data-ttu-id="6717a-111">Модуль записи координирует сжатие входных образцов изображения, используя формат JPEG.</span><span class="sxs-lookup"><span data-stu-id="6717a-111">The writer coordinates the compression of input image samples using the JPEG format.</span></span> <span data-ttu-id="6717a-112">Перед началом записи файла, содержащего поток изображений, необходимо задать качество изображения для входных данных с помощью \_ параметра g всзжпегкомпрессионкуалити.</span><span class="sxs-lookup"><span data-stu-id="6717a-112">Before you begin writing a file containing an image stream, you must set an image quality for the input, using the g\_wszJPEGCompressionQuality setting.</span></span> <span data-ttu-id="6717a-113">Используйте [**IWMWriterAdvanced2:: сетинпутсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) , чтобы задать для свойства Quality значение **DWORD** в диапазоне от 1 до 100.</span><span class="sxs-lookup"><span data-stu-id="6717a-113">Use [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) to set the quality to a **DWORD** value ranging from 1 to 100.</span></span> <span data-ttu-id="6717a-114">Низкие значения представляют собой коэффициент высокой степени сжатия за счет высокого качества, а высокие значения дают высококачественные изображения, требующие больше пространства.</span><span class="sxs-lookup"><span data-stu-id="6717a-114">Low values represent a high compression ratio at the expense of quality, while high values produce high quality images that require more space.</span></span>

<span data-ttu-id="6717a-115">Потокам изображений часто требуются большие окна буфера, чем обычные видеопотоки.</span><span class="sxs-lookup"><span data-stu-id="6717a-115">Image streams often require larger buffer windows than ordinary video streams.</span></span> <span data-ttu-id="6717a-116">Точный требуемый размер зависит от типа изображения и качества изображения, среди прочих факторов.</span><span class="sxs-lookup"><span data-stu-id="6717a-116">The exact size required depends on the type of image and the image quality, among other factors.</span></span> <span data-ttu-id="6717a-117">Используйте пробную версию и ошибку, чтобы определить подходящий размер для образов, которые планируется обработать.</span><span class="sxs-lookup"><span data-stu-id="6717a-117">Use trial and error to determine the appropriate size for the images you intend to process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6717a-118">См. также</span><span class="sxs-lookup"><span data-stu-id="6717a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6717a-119">**Потоки изображений**</span><span class="sxs-lookup"><span data-stu-id="6717a-119">**Image Streams**</span></span>](image-streams.md)
</dt> <dt>

[<span data-ttu-id="6717a-120">**Установка параметров ввода**</span><span class="sxs-lookup"><span data-stu-id="6717a-120">**To Set Input Settings**</span></span>](to-set-input-settings.md)
</dt> <dt>

[<span data-ttu-id="6717a-121">**Запись файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="6717a-121">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




