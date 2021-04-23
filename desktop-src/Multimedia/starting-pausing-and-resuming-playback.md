---
title: Запуск, приостановка и возобновление воспроизведения
description: Запуск, приостановка и возобновление воспроизведения
ms.assetid: 4af92781-5461-4195-82f5-a9213a9bdbd7
keywords:
- Макрос МЦивндплай
- Макрос МЦивндпаусе
- Макрос МЦивндресуме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734a186b90b8d6701923d0ffa1f743cc8c5ae378
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104259043"
---
# <a name="starting-pausing-and-resuming-playback"></a><span data-ttu-id="0b124-106">Запуск, приостановка и возобновление воспроизведения</span><span class="sxs-lookup"><span data-stu-id="0b124-106">Starting, Pausing, and Resuming Playback</span></span>

<span data-ttu-id="0b124-107">[**МЦивндплай**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) — наиболее общий макрос воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0b124-107">[**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) is the most general playback macro.</span></span> <span data-ttu-id="0b124-108">Этот макрос позволяет воспроизвести файл или устройство с текущей позицией воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0b124-108">This macro lets you play a file or device from the current playback position.</span></span> <span data-ttu-id="0b124-109">Воспроизведение продолжится до конца содержимого, если оно не было прервано.</span><span class="sxs-lookup"><span data-stu-id="0b124-109">Playback continues through the end of the content unless it is interrupted.</span></span>

<span data-ttu-id="0b124-110">Вы можете временно прервать воспроизведение устройства с помощью макроса [**мЦивндпаусе**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) .</span><span class="sxs-lookup"><span data-stu-id="0b124-110">You can temporarily interrupt a device that is playing by using the [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) macro.</span></span> <span data-ttu-id="0b124-111">Чтобы возобновить воспроизведение с приостановленной позицией, используйте макрос [**мЦивндресуме**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) .</span><span class="sxs-lookup"><span data-stu-id="0b124-111">To resume playback from the paused position, use the [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) macro.</span></span> <span data-ttu-id="0b124-112">Некоторые устройства не поддерживают команды Pause и Resume.</span><span class="sxs-lookup"><span data-stu-id="0b124-112">Some devices do not support the pause and resume commands.</span></span> <span data-ttu-id="0b124-113">Эти устройства обычно сопоставляют **мЦивндпаусе** с макросом [**мЦивндстоп**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) , который останавливает воспроизведение или запись.</span><span class="sxs-lookup"><span data-stu-id="0b124-113">These devices usually map **MCIWndPause** to the [**MCIWndStop**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) macro, which stops playback or recording.</span></span> <span data-ttu-id="0b124-114">Вы можете перезапустить устройство, не поддерживающее приостановку или возобновление с помощью **мЦивндплай**, которое запускает воспроизведение с текущей позицией воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0b124-114">You can restart a device that does not support pause or resume by using **MCIWndPlay**, which starts playback from the current playback position.</span></span>

 

 




