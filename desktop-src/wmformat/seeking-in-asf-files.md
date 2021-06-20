---
title: Поиск в файлах ASF (пакет SDK для Windows Media Format 11)
description: Узнайте, как средство чтения WM ASF может выполнять очень точную повременное Поиск содержимого на основе Windows Media с временным индексом в пакете SDK Windows Media Format 11.
ms.assetid: a1717cb4-9f41-4148-b088-a6517be7da9b
keywords:
- Windows Media Format SDK, поиск в файлах ASF
- Пакет SDK для Windows Media Format, DirectShow
- Расширенный системный формат (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- Расширенный формат систем (ASF), Поиск
- ASF (Расширенный системный формат), Поиск
- DirectShow, поиск в файлах ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 807631861cdc820457360058f22fca380fca29ea
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409887"
---
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a><span data-ttu-id="44255-110">Поиск в файлах ASF (пакет SDK для Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="44255-110">Seeking in ASF Files (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="44255-111">[Средство чтения WM ASF](wm-asf-reader-filter.md)через его интерфейс **имедиасикинг** может выполнять очень точное временное Поиск содержимого на основе Windows Media с временным индексом.</span><span class="sxs-lookup"><span data-stu-id="44255-111">The [WM ASF Reader](wm-asf-reader-filter.md), through its **IMediaSeeking** interface, can perform very accurate temporal seeking on Windows Media–based content that has a temporal index.</span></span> <span data-ttu-id="44255-112">(Все индексируемые фреймы содержимого также содержат временный индекс). Гарантируется, что поиск в точно-ориентированном поиске не поддерживается напрямую в модуле чтения WM ASF, но существует способ сделать это, если требуется эта функция.</span><span class="sxs-lookup"><span data-stu-id="44255-112">(All frame-indexed content also contains a temporal index.) Guaranteed frame-accurate seeking is not directly supported in the WM ASF Reader, but there is a way to do it if you require this functionality.</span></span> <span data-ttu-id="44255-113">Во-первых, используйте пакет SDK для формата Windows Media, чтобы создать экземпляр синхронного объекта Reader, открыть файл, получить метку времени, связанную с указанным кадром, а затем использовать интерфейс DirectShow **имедиасикинг** для поиска в это время.</span><span class="sxs-lookup"><span data-stu-id="44255-113">First, use the Windows Media Format SDK directly to create an instance of the synchronous reader object, open the file, obtain the time stamp associated with a specified frame, and then use the DirectShow **IMediaSeeking** interface to seek to that time.</span></span> <span data-ttu-id="44255-114">Интерфейс DirectShow **ивидеофраместеп** не поддерживает точное Поиск содержимого на основе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="44255-114">The DirectShow **IVideoFrameStep** interface does not support frame-accurate seeking of Windows Media–based content.</span></span> <span data-ttu-id="44255-115">Пример Дссикфм в пакете SDK для формата Windows Media демонстрирует, как выполнять поиск с точностью в виде кадров с помощью средства чтения WM ASF.</span><span class="sxs-lookup"><span data-stu-id="44255-115">The DSSeekFm sample in the Windows Media Format SDK demonstrates how to perform frame-accurate seeking using the WM ASF Reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44255-116">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="44255-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44255-117">**Фильтр чтения WM ASF**</span><span class="sxs-lookup"><span data-stu-id="44255-117">**WM ASF Reader Filter**</span></span>](wm-asf-reader-filter.md)
</dt> </dl>

 

 




