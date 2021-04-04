---
description: Пример Вмрплайер
ms.assetid: 7fc893a6-afa5-4ada-9295-29122b43b21e
title: Пример Вмрплайер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2214d94628a90daf0dd543f4e3a7f0166f4968a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898166"
---
# <a name="vmrplayer-sample"></a><span data-ttu-id="bac0b-103">Пример Вмрплайер</span><span class="sxs-lookup"><span data-stu-id="bac0b-103">VMRPlayer Sample</span></span>

## <a name="description"></a><span data-ttu-id="bac0b-104">Описание</span><span class="sxs-lookup"><span data-stu-id="bac0b-104">Description</span></span>

<span data-ttu-id="bac0b-105">В этом примере фильтр с изображением прорисовки 9 (VMR-9) используется для альфа Blend одного или двух работающих видео и статического изображения.</span><span class="sxs-lookup"><span data-stu-id="bac0b-105">This sample uses the Video Mixing Renderer 9 (VMR-9) filter to alpha blend one or two running videos and a static image.</span></span>

## <a name="usage"></a><span data-ttu-id="bac0b-106">Использование</span><span class="sxs-lookup"><span data-stu-id="bac0b-106">Usage</span></span>

<span data-ttu-id="bac0b-107">Чтобы открыть первое видео, выберите в меню **файл** пункт **Открыть основной поток** .</span><span class="sxs-lookup"><span data-stu-id="bac0b-107">To open the first video, choose **Open Primary Stream** from the **File** menu.</span></span> <span data-ttu-id="bac0b-108">Чтобы открыть второе видео, выберите **Открыть вторичный поток** в меню **файл** (сначала необходимо открыть основной поток).</span><span class="sxs-lookup"><span data-stu-id="bac0b-108">To open a second video, choose **Open Secondary Stream** from the **File** menu (you must open the primary stream first).</span></span> <span data-ttu-id="bac0b-109">Чтобы воспроизвести видео, нажмите кнопку **Воспроизведение** .</span><span class="sxs-lookup"><span data-stu-id="bac0b-109">To play the video, click the **Play** button.</span></span>

<span data-ttu-id="bac0b-110">Можно задать расположение, размер и альфа-значения видео, выбрав **основной поток** или **поток Секондард** в меню **Свойства VMR** .</span><span class="sxs-lookup"><span data-stu-id="bac0b-110">You can set the position, size, and alpha values of the videos by selecting **Primary Stream** or **Secondard Stream** from the **VMR Properties** menu.</span></span>

<span data-ttu-id="bac0b-111">Чтобы добавить статическое растровое изображение в видео, выберите **статический образ приложения** в меню **Свойства VMR** и щелкните поле **отображаемое изображение приложения** .</span><span class="sxs-lookup"><span data-stu-id="bac0b-111">To add a static bitmap over the video, choose **Static App Image** from the **VMR Properties** menu and click the **Display App Image** box.</span></span> <span data-ttu-id="bac0b-112">Вы можете использовать то же диалоговое окно для управления положением, размером и альфа-значением точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="bac0b-112">You can use the same dialog to control the position, size, and alpha value of the bitmap.</span></span>

<span data-ttu-id="bac0b-113">Чтобы записать изображение в смешанном видео, выберите пункт **записать растровое изображение** в меню **Свойства VMR** .</span><span class="sxs-lookup"><span data-stu-id="bac0b-113">To capture the blended video image, choose **Capture Bitmap Image** from the **VMR Properties** menu.</span></span>

<span data-ttu-id="bac0b-114">Кроме того, можно указать основной поток образа из командной строки:</span><span class="sxs-lookup"><span data-stu-id="bac0b-114">You can also specify the primary image stream from the command line:</span></span>

<span data-ttu-id="bac0b-115">**Вмрплайер** **/p** *имя файла*</span><span class="sxs-lookup"><span data-stu-id="bac0b-115">**VMRPlayer** **/P** *filename*</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="bac0b-116">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="bac0b-116">Downloading the Sample</span></span>

<span data-ttu-id="bac0b-117">Чтобы скачать примеры пакета SDK для DirectShow, установите последнюю версию [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bac0b-117">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bac0b-118">См. также</span><span class="sxs-lookup"><span data-stu-id="bac0b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bac0b-119">Примеры DirectShow</span><span class="sxs-lookup"><span data-stu-id="bac0b-119">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



