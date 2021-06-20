---
description: Узнайте, как читатель WM ASF может выполнять очень точную повременное Поиск содержимого на основе Windows Media с временным индексом в DirectShow.
ms.assetid: da0d687b-f571-4623-9705-e697ba8bc04e
title: Поиск в файлах ASF (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ffc570536463b86a88e1f26be338bd748c790c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405587"
---
# <a name="seeking-in-asf-files-directshow"></a><span data-ttu-id="dd3ed-103">Поиск в файлах ASF (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="dd3ed-103">Seeking in ASF Files (DirectShow)</span></span>

<span data-ttu-id="dd3ed-104">[Средство чтения WM ASF](wm-asf-reader-filter.md)через его интерфейс [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) может выполнять очень точное временное Поиск содержимого на основе Windows Media с временным индексом.</span><span class="sxs-lookup"><span data-stu-id="dd3ed-104">The [WM ASF Reader](wm-asf-reader-filter.md), through its [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, can perform very accurate temporal seeking on Windows Media–based content that has a temporal index.</span></span> <span data-ttu-id="dd3ed-105">(Все индексируемые фреймы содержимого также содержат временный индекс). Гарантируется, что поиск в точно-ориентированном поиске не поддерживается напрямую в модуле чтения WM ASF, но существует способ сделать это, если требуется эта функция.</span><span class="sxs-lookup"><span data-stu-id="dd3ed-105">(All frame-indexed content also contains a temporal index.) Guaranteed frame-accurate seeking is not directly supported in the WM ASF Reader, but there is a way to do it if you require this functionality.</span></span> <span data-ttu-id="dd3ed-106">Во-первых, используйте пакет SDK для формата Windows Media, чтобы создать экземпляр синхронного объекта Reader, открыть файл, получить метку времени, связанную с указанным кадром, а затем использовать интерфейс DirectShow **имедиасикинг** для поиска в это время.</span><span class="sxs-lookup"><span data-stu-id="dd3ed-106">First, use the Windows Media Format SDK directly to create an instance of the synchronous reader object, open the file, obtain the time stamp associated with a specified frame, and then use the DirectShow **IMediaSeeking** interface to seek to that time.</span></span> <span data-ttu-id="dd3ed-107">Интерфейс [**ивидеофраместеп**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) не поддерживает точное Поиск содержимого на основе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dd3ed-107">The [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface does not support frame-accurate seeking of Windows Media–based content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd3ed-108">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="dd3ed-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd3ed-109">Чтение файлов ASF в DirectShow</span><span class="sxs-lookup"><span data-stu-id="dd3ed-109">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



