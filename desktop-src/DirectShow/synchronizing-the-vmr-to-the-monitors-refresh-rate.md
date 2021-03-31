---
description: Синхронизация VMR с частотой обновления монитора
ms.assetid: 73e73821-fb08-488a-956e-ef33f6651a26
title: Синхронизация VMR с частотой обновления монитора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a9550e96e6a2e35c196048d38dd5b6e5b536d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272474"
---
# <a name="synchronizing-the-vmr-to-the-monitors-refresh-rate"></a><span data-ttu-id="4acfe-103">Синхронизация VMR с частотой обновления монитора</span><span class="sxs-lookup"><span data-stu-id="4acfe-103">Synchronizing the VMR to the Monitor's Refresh Rate</span></span>

<span data-ttu-id="4acfe-104">В редких случаях может потребоваться точно синхронизировать визуализацию видео с частотой обновления монитора, чтобы каждый раз при обновлении монитора выдавалась ровно одна новая рамка.</span><span class="sxs-lookup"><span data-stu-id="4acfe-104">In rare scenarios, you may wish to precisely synchronize video rendering with the monitor's refresh rate, so that exactly one new frame is presented each time the monitor refreshes.</span></span> <span data-ttu-id="4acfe-105">Самый надежный способ сделать это — создать пользовательский распределитель-объект, использующий операцию отражения вместо Блит операции для записи видеобитов на основную поверхность.</span><span class="sxs-lookup"><span data-stu-id="4acfe-105">The most reliable way to do this is to create a custom allocator-presenter that uses a flip operation instead of a blit operation to write the video bits into the primary surface.</span></span> <span data-ttu-id="4acfe-106">"Перелистывание" вызывается каждый раз, когда монитор обновляется, поэтому, если в потоке видео нет отметок времени, VMR будет отображаться как можно быстрее на основной поверхности, но поверхность будет блокировать поток до завершения операции отражения.</span><span class="sxs-lookup"><span data-stu-id="4acfe-106">"Flip" is called each time the monitor refreshes, so if your video stream contains no time stamps, the VMR will render as fast as possible to the primary surface, but the surface will block the stream until the Flip operation completes.</span></span> <span data-ttu-id="4acfe-107">Это означает, что если ЦП не перегружен, следующий кадр всегда будет ожидать на основной поверхности каждый раз при обновлении монитора.</span><span class="sxs-lookup"><span data-stu-id="4acfe-107">This means that, as long as the CPU is not overburdened, the next frame will always be waiting in the primary surface each time the monitor refreshes.</span></span> <span data-ttu-id="4acfe-108">Однако если выполняется какой-либо другой процесс, требующий интенсивного использования ЦП, это может привести к ограничению потока потоковой передачи DirectShow, чтобы он не мог доставить видеоматериалы достаточно быстро для основной поверхности.</span><span class="sxs-lookup"><span data-stu-id="4acfe-108">However, if some other CPU-intensive process is running, it could possibly starve your DirectShow streaming thread so that it cannot deliver video frames fast enough to the primary surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4acfe-109">См. также</span><span class="sxs-lookup"><span data-stu-id="4acfe-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4acfe-110">Режим воспроизведения VMR (пользовательский распределитель — выступающие)</span><span class="sxs-lookup"><span data-stu-id="4acfe-110">VMR Renderless Playback Mode (Custom Allocator-Presenters)</span></span>](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



