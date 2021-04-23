---
title: Поток управления
description: Поток управления
ms.assetid: b91c0191-1908-4d62-96ce-927d09c70f9a
keywords:
- визуализации, выполнение программ
- Пользовательские визуализации, поток программы
- визуализации, поток управления
- Пользовательские визуализации, поток управления
- визуализации, события с превышением времени
- Пользовательские визуализации, события с превышением времени
- визуализации, функция Render
- Пользовательские визуализации, функция Render
- визуализации, функция Рендервиндов
- Пользовательские визуализации, функция Рендервиндов
- Функция Render, последовательность программы визуализации
- Функция Рендервиндов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca09760d958da045c4bbf60ae122a9d0ae4c71c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986236"
---
# <a name="flow-of-control"></a><span data-ttu-id="d96b5-115">Поток управления</span><span class="sxs-lookup"><span data-stu-id="d96b5-115">Flow of Control</span></span>

<span data-ttu-id="d96b5-116">Звуковые данные поступают в проигрыватель Windows Media постоянно через файл или поток.</span><span class="sxs-lookup"><span data-stu-id="d96b5-116">Audio data comes into Windows Media Player continuously through a file or a stream.</span></span> <span data-ttu-id="d96b5-117">Эти данные передаются в визуализацию.</span><span class="sxs-lookup"><span data-stu-id="d96b5-117">That data is passed to your visualization.</span></span> <span data-ttu-id="d96b5-118">Вы рисуете на определенной поверхности и передаете ее обратно в проигрыватель Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d96b5-118">You draw on a defined surface and pass that surface back to Windows Media Player.</span></span> <span data-ttu-id="d96b5-119">Этот обмен выполняется несколько раз в секунду, и пользователь получает привлекательную анимацию, которая переносит время на музыку.</span><span class="sxs-lookup"><span data-stu-id="d96b5-119">This interchange happens several times a second, and to the user, the result is a pleasing animation that moves in time to the music.</span></span>

<span data-ttu-id="d96b5-120">Ниже приведена конкретная последовательность последовательности программы визуализации:</span><span class="sxs-lookup"><span data-stu-id="d96b5-120">Here is the specific sequence of the visualization program flow:</span></span>

1.  <span data-ttu-id="d96b5-121">По истечении интервала проигрыватель Windows Media создает моментальный снимок воспроизводимого звука.</span><span class="sxs-lookup"><span data-stu-id="d96b5-121">At a timed interval, Windows Media Player takes a snapshot of the audio that is playing.</span></span>
2.  <span data-ttu-id="d96b5-122">Проигрыватель Windows Media предоставляет данные из этого снимка в визуализацию с помощью функции **Render** и функции **рендервиндовед** .</span><span class="sxs-lookup"><span data-stu-id="d96b5-122">Windows Media Player supplies the data from that snapshot to your visualization through the **Render** function and the **RenderWindowed** function.</span></span>
3.  <span data-ttu-id="d96b5-123">Необходимо написать код, который будет выполняться при вызове **Render** и **рендервиндовед** .</span><span class="sxs-lookup"><span data-stu-id="d96b5-123">You must write code that will run when **Render** and **RenderWindowed** is called.</span></span> <span data-ttu-id="d96b5-124">Код рисуется с помощью контекста устройства, определенного проигрывателем Windows Media при отрисовке без окна, или с помощью окна, создаваемого при отрисовке окна.</span><span class="sxs-lookup"><span data-stu-id="d96b5-124">Your code draws by using a device context defined by Windows Media Player when rendering windowless, or by using a window that you create when rendering windowed.</span></span>
4.  <span data-ttu-id="d96b5-125">В регионе, указанном в текущей обложке, проигрыватель Windows Media отображает, что нарисовано в коде.</span><span class="sxs-lookup"><span data-stu-id="d96b5-125">In a region specified by the current skin, Windows Media Player displays what your code drew.</span></span>
5.  <span data-ttu-id="d96b5-126">Этот процесс повторяется несколько раз в секунду, создавая графические анимации, которые отправляются по времени на музыку.</span><span class="sxs-lookup"><span data-stu-id="d96b5-126">This process repeats several times a second, creating graphical animations that are timed to the music.</span></span> <span data-ttu-id="d96b5-127">После прекращения воспроизведения музыки визуализация останавливается.</span><span class="sxs-lookup"><span data-stu-id="d96b5-127">When the music stops playing, the visualization stops.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d96b5-128">См. также</span><span class="sxs-lookup"><span data-stu-id="d96b5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d96b5-129">**Обзор для разработчиков**</span><span class="sxs-lookup"><span data-stu-id="d96b5-129">**Developer Overview**</span></span>](developer-overview.md)
</dt> </dl>

 

 




