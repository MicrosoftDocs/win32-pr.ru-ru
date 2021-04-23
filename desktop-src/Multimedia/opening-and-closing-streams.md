---
title: Открытие и закрытие потоков
description: Открытие и закрытие потоков
ms.assetid: 7dcaccbe-63d8-410a-ae00-16ce9e252ad0
keywords:
- Функция Авифилежетстреам
- Функция Авистреамрелеасе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4462e261f1480129c073b70ddc61f91a422c8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067690"
---
# <a name="opening-and-closing-streams"></a><span data-ttu-id="f853b-105">Открытие и закрытие потоков</span><span class="sxs-lookup"><span data-stu-id="f853b-105">Opening and Closing Streams</span></span>

<span data-ttu-id="f853b-106">Открытие потоков данных похоже на открытие файлов.</span><span class="sxs-lookup"><span data-stu-id="f853b-106">Opening data streams is similar to opening files.</span></span> <span data-ttu-id="f853b-107">Вы можете открыть поток с помощью функции [**авифилежетстреам**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) .</span><span class="sxs-lookup"><span data-stu-id="f853b-107">You can open a stream by using the [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) function.</span></span> <span data-ttu-id="f853b-108">Эта функция создает потоковый интерфейс, размещает в интерфейсе маркер потока и возвращает указатель на интерфейс.</span><span class="sxs-lookup"><span data-stu-id="f853b-108">This function creates a stream interface, places a handle of the stream in the interface, and returns a pointer to the interface.</span></span> <span data-ttu-id="f853b-109">**Авифилежетстреам** также поддерживает количество ссылок приложений, открывших поток, но не открыв его.</span><span class="sxs-lookup"><span data-stu-id="f853b-109">**AVIFileGetStream** also maintains a reference count of the applications that have opened a stream, but not of those that have closed it.</span></span>

<span data-ttu-id="f853b-110">Если требуется получить доступ к одному потоку в файле, можно открыть файл и поток с помощью функции [**авистреамопенфромфиле**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) .</span><span class="sxs-lookup"><span data-stu-id="f853b-110">If you want to access a single stream in a file, you can open the file and the stream by using the [**AVIStreamOpenFromFile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) function.</span></span> <span data-ttu-id="f853b-111">Эта функция сочетает операции и аргументы функции функций [**авифилеопен**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) и **авифилежетстреам** .</span><span class="sxs-lookup"><span data-stu-id="f853b-111">This function combines the operations and function arguments of the [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) and **AVIFileGetStream** functions.</span></span>

<span data-ttu-id="f853b-112">Для доступа к более чем одному потоку в файле используйте **авифилеопен** один раз, за которым следует несколько вызовов **авифилежетстреам**.</span><span class="sxs-lookup"><span data-stu-id="f853b-112">To access more than one stream in a file, use **AVIFileOpen** once followed by multiple calls to **AVIFileGetStream**.</span></span>

<span data-ttu-id="f853b-113">Можно увеличить счетчик ссылок в потоке с помощью функции [**авистреамаддреф**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) , чтобы оставить поток открытым при использовании функции, которая обычно закрывает поток.</span><span class="sxs-lookup"><span data-stu-id="f853b-113">You can increment the reference count of a stream by using the [**AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) function to keep a stream open when using a function that would normally close the stream.</span></span>

<span data-ttu-id="f853b-114">Вы можете закрыть поток с помощью функции [**авистреамрелеасе**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) .</span><span class="sxs-lookup"><span data-stu-id="f853b-114">You can close a stream by using the [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) function.</span></span> <span data-ttu-id="f853b-115">Эта функция уменьшает значение счетчика ссылок потока и закрывает его, когда счетчик ссылок достигает нуля.</span><span class="sxs-lookup"><span data-stu-id="f853b-115">This function decrements the reference count of the stream and closes it when the reference count reaches zero.</span></span> <span data-ttu-id="f853b-116">Приложения должны сбалансировать количество ссылок, включив вызов **авистреамрелеасе** для каждого использования функции [**авифилежетстреам**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream), [**авифилекреатестреам**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream), **авистреамаддреф** или **авистреамопенфромфиле** .</span><span class="sxs-lookup"><span data-stu-id="f853b-116">Your applications should balance the reference count by including a call to **AVIStreamRelease** for each use of the [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream), [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream), **AVIStreamAddRef**, or **AVIStreamOpenFromFile** function.</span></span> <span data-ttu-id="f853b-117">При освобождении потока, открытого с помощью **авистреамопенфромфиле**, авифиле закрывает файл, содержащий поток.</span><span class="sxs-lookup"><span data-stu-id="f853b-117">When you release a stream that has been opened by using **AVIStreamOpenFromFile**, AVIFile closes the file containing the stream.</span></span> <span data-ttu-id="f853b-118">Если приложение освобождает файл с открытыми потоками данных, Авифиле не закрывает потоки до тех пор, пока не будут освобождены все потоки.</span><span class="sxs-lookup"><span data-stu-id="f853b-118">If your application releases a file that has open data streams, AVIFile will not close the streams until all of the streams are released.</span></span>

 

 




